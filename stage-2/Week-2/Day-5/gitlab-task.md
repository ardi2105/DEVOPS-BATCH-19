##  Sourcer Code Management Menggunakan GitLabci

### GitLab
GitLab adalah sebuah platform kolaborasi untuk pengembangan perangkat lunak yang menggunakan sistem kontrol versi Git. Ini adalah alat yang memungkinkan tim pengembang untuk bekerja sama dalam proyek perangkat lunak, mengelola kode sumber, dan melacak perubahan yang dibuat pada kode tersebut. Berikut adalah beberapa fitur dan komponen utama dari GitLab:
1. Repository Management
2. Issue Tracking
3. Continuous Integration (CI) / Continuous Deployment (CD)
4. Code Review

### Langkah Pengerjaan
Berikut adalah dokumentasi langkah langkah bagaimana membuat pipeline pada gitlab untuk menjalankan aplikasi-aplikasi yang dibutuhkan dan membuat suatu automation menggunakan gitlab sehingga ketika terdapat perubahan pada source code akan secara otomatis mentrigger gitlab pipeline.

- Buat akun di gitlab.com
- Push SCM dari local-server ke gitlab
- Membuat beberapa Job menggunakan gitlabci untuk aplikasi:
    - Job Frontend
    - Job Backend
    - Script CICD atur flow pengupdate an aplikasi mencakup
        - Pull dari repository
        - Dockerize/Build aplikasi kita
        - push image ke docker hub
        - Test application
        - pull new image
        - Deploy application

1. Login ke gitlab menggunakan email atau dapat membuat akun baru.
![Alt text](images/login-gitlab.png) 

1. Masukan aplikasi ke dalam repository GitLab serta dapat diremote oleh server 
![Alt text](images/repository-gitlab.png) 

1. Menambahkan SSH key agar server dapat terhubung ke repository gitlab.
![Alt text](images/ssh-key.png) 

1. Masuk ke dalam setting CICD untuk menambahkan SSH Private key yang berguna agar gitlab dapat terhubung ke server.
![Alt text](images/ci-cd.png) 
![Alt text](images/ssh-private-key.png) 

1. Membuat script gitlab untuk backend dan frontend
![Alt text](<images/script-.gitlab- be.png>) 
![Alt text](images/script-.gitlab-fe.png) 

1. Lakukan build untuk menajalankan Gitlabci pipeline
![Alt text](images/build.png) 
![Alt text](images/pipeline.png)