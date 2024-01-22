# DEVOPS-BATCH19-STAGE2
#### Weekly Task - Week 2 - Ardi Solehuddin

Pada minggu ini saya mengerjakan bagaimana melakukan deploy aplikasi frontend dan backend menggunakan Docker, Jenkins serta Gitlabci hingga aplikasi tersebut dapat diakses oleh publik melalui internet serta dapat melakukan automation aplikasi. Terdapat tugas harian yang akan dikerjakan secara berkala yaitu apa saja yang harus dikerjakan setiap selesai kelas serta melakukan riset lebih mendalam terhadap hal yang dikerjakan. Adapun tugas tugas yang diberikan dibagi setiap harinya, antara lain :

#### [Hari Ketiga](Day-3/docker-task.md)
1. Menjelaskan langkah-langkah melakukan rebuild server BiznetGio, dan ubah menggunakan os ubuntu22

2. Setelah server sudah selesai ter rebuild, buatlah suatu user baru dengan nama **team kalian** lalu implementasikan penggunaan ssh dengan menggunakan **PASSWORD ONLY** tanpa SSH-KEY.

3. Membuat bash script untuk melakukan installasi docker. 

4. Deploy aplikasi Web Server, Frontend, Backend, serta Database on top `docker compose`

5. Membuat suatu docker compose yang berisi beberapa service:
    - Web Server
    - Frontend
    - Backend
    - Database

6. Membuat suatu custom network dengan nama **team kalian**, lalu pasang ke setiap service yang kalian miliki.

7. Deploy database menggunakan mysql dengan versi terbaru, dan pasang volume di bagian database.

8. Building image frontend dan backend dengan dockerized image sekecil mungkin dan sesuaikan configuration dari backend ke database maupun frontend ke backend sebelum di build menjadi docker images.

9. Web Server konfigurasi reverse-proxy menggunakan nginx on top docker.
    - **SSL CLOUDFLARE OFF!!!**
    - Gunakan docker volume untuk membuat reverse proxy
    - SSL sebisa mungkin gunakan wildcard
    - Untuk DNS bisa sesuaikan seperti contoh di bawah ini
      - Frontend team1.studentdumbways.my.id
      - Backend api.team1.studentdumbways.my.id

10. Push image ke docker registry.

11. Aplikasi dapat berjalan dengan sesuai seperti melakukan login/register.

#### [Hari Keempat](Day-4/jenkins-task.md)
1. Jelasakan langkah-langkah melakukan rebuild server BiznetGio, dan ubah menggunakan os ubuntu22

2. Installasi Jenkins on top Docker or native

3. Setup SSH-KEY di local server jenkins kalian, agar dapat 

4. login ke dalam server menggunakan SSH-KEY 

5. Reverse Proxy Jenkins
  - gunakan domain ex. pipeline-team4.studentdumbways.my.id
  - reverse proxy sesuaikan dengan ketentuan yang ada di dalam Jenkins documentation

6. Membuat beberapa Job untuk aplikasi: 
    - Job Frontend
    - Job Backend
    - Script CICD flow pengupdate an aplikasi mencakup
        - Pull dari repository
        - Dockerize/Build aplikasi kita
        - Test application
        - Deploy aplikasi on top Docker
        - Push ke Docker Hub

7. Auto trigger setiap ada perubahan di SCM

8. Job notification ke discord

#### [Hari Kelima](Day-5/gitlab-task.md)
1. Buat akun di gitlab.com

2. Push SCM dari local-server ke gitlab

3. Membuat beberapa Job menggunakan gitlabci untuk aplikasi:
    - Job Frontend
    - Job Backend
    - Script CICD atur flow pengupdate an aplikasi mencakup
        - Pull dari repository
        - Dockerize/Build aplikasi kita
        - push image ke docker hub
        - Test application
        - pull new image
        - Deploy application