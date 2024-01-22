## Rebuild Server Serta Install Docker Dan Aplikasi
Berikut adalah dokumentasi langkah langkah bagaimana melakukan rebuild VM di Biznetgio serta instalasi aplikasi-aplikasi yang dibutuhkan untuk melakukan deploy aplikasi wayshub-frontend menggunakan docker.

1. Login terlebih dahulu ke dalam website Biznetgio lalu rebuild server.
![Alt text](Docker-and-Docker-Compose/rebuild-server-1.png)

2. Melaukan rebuild dengan system operasi ubuntu versi 22.04
![Alt text](Docker-and-Docker-Compose/rebuild-server-2.png)

3. Membuat user baru pada server yaitu user team1 untuk di dalamnya melakukan instalasi docker
![Alt text](Docker-and-Docker-Compose/make-user.png)

4. Melakukan setting ssh password agar user yang baru dibuat dapat login menggunakan password.  
![Alt text](Docker-and-Docker-Compose/setting-ssh-password-2.png)
![Alt text](Docker-and-Docker-Compose/setting-ssh-password-4.png)

5. Melakukan install docker dengan membuat script.  
![Alt text](Docker-and-Docker-Compose/docker-install-1.png)
![Alt text](Docker-and-Docker-Compose/docker-install-2.png)
![Alt text](Docker-and-Docker-Compose/docker-install-3.png)

6. Melakukan git clone baik aplikasi frontend ataupun backend.
![Alt text](Docker-and-Docker-Compose/git-clone.png)

7. Setting api pada frontend agar dapat terhubung ke backend.
![Alt text](Docker-and-Docker-Compose/setting-api-fe-1.png)
![Alt text](Docker-and-Docker-Compose/setting-api-fe-2.png) 

8. Membuat dockerfile di dalam folder wayshub frontend agar aplikasi dapat dijalankan menggunakan docker compose.
![Alt text](Docker-and-Docker-Compose/dockerfile-fe.png) 

9. Melakukan setting backend agar nantinya backend dapat terhubung ke database.
![Alt text](Docker-and-Docker-Compose/setting-backend-be-1.png) 
![Alt text](Docker-and-Docker-Compose/setting-backend-be-2.png) 

10. Membuat dockerfile di dalame folder wayshub backend agar aplikasi dapat berjalan menggunakan docker compose. 
![Alt text](Docker-and-Docker-Compose/dockerfile-be.png) 

11. Membuat docker network agar setiap aplikasi yang berjalan pada docker compose berjalan pada network yang sama yaitu pada network team1. 
![Alt text](Docker-and-Docker-Compose/creat-docker-network.png) 

12. Membuat docker compose file yang isinya berupa script atau perintah untuk melakukan instalasi database, aplikasi frontend, backend serta instalasi web server. 
![Alt text](Docker-and-Docker-Compose/docker-compose-1.png) 
![Alt text](Docker-and-Docker-Compose/docker-compose-2.png) 

13. Running docker database terlebih dahulu agar nantinya database dapat terhubung.
![Alt text](Docker-and-Docker-Compose/running-docker-db.png) 

14. Membuat reverse proxy agar aplikasi yang berjalan dapat diakses menggunakan domain menggunakan web server nginx.
![Alt text](Docker-and-Docker-Compose/make-reverse-proxy.png) 
![Alt text](Docker-and-Docker-Compose/make-reverse-proxy-2.png) 

15. Copy file ssl certbot yang sudah digenerate sebelumnya menggunakan ssl cloudflare wildcard sesuai dengan directory yang dibuat menggunakan docker compose.
![Alt text](Docker-and-Docker-Compose/copy-ssl-cloudflare.png) 

16. Melakukan docker compose up agar semua aplikasi dapat berjalan.  
![Alt text](Docker-and-Docker-Compose/docker-compose-up.png)

17. Selanjutnya adalah docker push di mana natinya image yang telah terbuat agar dimasukan ke dalam docker registry.
![Alt text](Docker-and-Docker-Compose/docker-push.png) 

18. Aplikasi dapat berjalan serta dapat melakukan login ke dalam aplikasi.
![Alt text](Docker-and-Docker-Compose/registration.png) 
![Alt text](Docker-and-Docker-Compose/Login.png) 

