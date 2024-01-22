##  Sourcer Code Management Menggunakan GitLabci
Berikut adalah dokumentasi langkah langkah bagaimana melakukan rebuild VM di Biznetgio serta instalasi jenkins on top docker serta membuat pipeline pada jenkins untuk menjalankan aplikasi-aplikasi yang dibutuhkan.

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
![Alt text](gitlab/login-gitlab.png) 

2. Masukan aplikasi ke dalam repository GitLab serta dapat diremote oleh server 
![Alt text](gitlab/repository-gitlab.png) 

3. Menambahkan SSH key agar server dapat terhubung ke repository gitlab.
![Alt text](gitlab/ssh-key.png) 

4. Masuk ke dalam setting CICD untuk menambahkan SSH Private key yang berguna agar gitlab dapat terhubung ke server.
![Alt text](gitlab/ci-cd.png) 
![Alt text](gitlab/ssh-private-key.png) 

6. Membuat script gitlab untuk backend dan frontend
![Alt text](<gitlab/script-.gitlab- be.png>) 
![Alt text](gitlab/script-.gitlab-fe.png) 

8. Lakukan build untuk menajalankan Gitlabci pipeline
![Alt text](gitlab/build.png) 
![Alt text](gitlab/pipeline.png)