**Requirements**
- 1 SSH keys max.
- SSH Config.
- Ubuntu 22.04 lts

**Instructions**
- Create new user `finaltask-$USER`
- Server login only with SSH key
- **Password login disabled**
- Create a working **SSH config** to log into servers
- Only use **1 SSH keys** for all purpose (Repository, CI/CD etc.)
- UFW enabled with only used ports allowed
- Change ssh port from (22) to (1234)

#### Langkah Pengerjaan
1. Membuat script dengan nama file `create-user.yml` untuk membuat user pada masing masing server menggunakan ansible script berikut:
   ```
    - hosts: biznet
    become: true
    tasks:

    - name: Remove the user 'finaltask-ardi'
      ansible.builtin.user:
        name: finaltask-ardi
        state: absent
        remove: yes

    - name: Update apt-get repo and cache
      apt: 
        update_cache: yes 
        force_apt_get: yes 
        cache_valid_time: 3600

    - name: Upgrade all apt packages
      apt: 
        upgrade: dist
        force_apt_get: yes

    - name: Create New User
      ansible.builtin.user:
        name: finaltask-ardi
        password: '$6$rb3rBrzECtfABArV$YubkI9f2PpKkOdK.VqXffMrY8Lj4Jbvp1lLDKd3EIelm.MhOO/dPtzQBIaJEwdOUuKKFjNczUkFozkoFJ.Q7D0'
        groups: sudo
        append: yes
        state: present
        shell: /bin/bash
        system: no 
        createhome: yes
        home: /home/finaltask-ardi
   ```
    Jalankan perintah
    ```
    ansible-playbook create-user.yaml 
    ``` 

2. Membuat script dengan nama file `ssh-key.yml`untuk melakukan setting pada ssh serta mengupload ssh key public dan private ke server sehingga dapat diakses tanpa menggunakan password. SSH key ini juga akan digunakan dalam melakukan akses repository.

   ```
    - hosts: biznet
    become: true
    tasks:

    - name: Create .ssh folder
      file:
        path: /home/finaltask-ardi/.ssh
        state: directory
        owner: finaltask-ardi
        group: finaltask-ardi
        mode: 0700
        
    - name: Upload SSH Public Key
      copy:
        src: /home/ardi/.ssh/id_rsa.pub
        dest: /home/finaltask-ardi/.ssh/authorized_keys
        owner: finaltask-ardi
        group: finaltask-ardi

    - name: Upload SSH Private Key
      copy:
        src: /home/ardi/.ssh/id_rsa
        dest: /home/finaltask-ardi/.ssh/
        owner: finaltask-ardi
        group: finaltask-ardi
        mode: 0400
    
    - name: Disable Password Authentication
      lineinfile:
        dest: '{{item}}'
        regexp: '^PasswordAuthentication'
        line: "PasswordAuthentication no"
        state: present
        backup: yes
      loop:
        - /etc/ssh/sshd_config
        - /etc/ssh/sshd_config.d/50-cloud-init.conf

    - name: restart ssh
      service:
        name: sshd
        state: restarted
   ```
    Jalankan perintah
    ```
    ansible-playbook ssh-key.yaml 
    ``` 

3. Membuat script dengan nama file `ufw-config.yml`untuk melakukan settingan pada ufw agar user yang dibuat hanya dapat diakses dengan port yang telah ditentukan:
   ```
    - hosts: servers
    become: true
    tasks:

      - name: Update SSH Port in sshd_config
        lineinfile:
          path: /etc/ssh/sshd_config
          regexp: '^Port '
          line: 'Port 1234'

      - name: restart sshd
        service:
          name: ssh
          state: restarted

      - name: Install UFW
        apt:
          name: ufw
          state: present

      - name: Allow SSH through UFW
        ufw:
          rule: allow
          name: OpenSSH

      - name: Allow additional ports if needed
        ufw:
          rule: allow
          port: "{{ item }}"
        loop:
          - 80
          - 443
          - 1234
          # Tambahkan port-port lainnya yang diperlukan

      - name: Enable UFW
        ufw:
          state: enabled

      - name: Reload UFW
        command: ufw reload
   ```
    Jalankan perintah
    ```
    ansible-playbook ufw-config.yaml 
    ``` 
