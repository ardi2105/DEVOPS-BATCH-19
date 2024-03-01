## Rebuild Server Serta Install Docker Dan Aplikasi

### Docker
Docker adalah platform perangkat lunak yang memungkinkan Anda untuk mengemas, mengirim, dan menjalankan aplikasi dengan menggunakan teknologi kontainer. Konsep dasar di balik Docker adalah kontainer, yang memungkinkan pengembang untuk mengisolasi aplikasi bersama dengan semua dependensinya, termasuk perpustakaan, kode, alat, dan lingkungan runtime, ke dalam paket yang dapat dipindahkan secara mandiri. Berikut adalah beberapa komponen utama Docker:
1. Docker Engine
2. Docker Container
3. Docker Image
4. Dockerfile
5. Docker Registry

### Langkah Pengerjaan
Berikut adalah dokumentasi langkah langkah bagaimana melakukan rebuild VM di Biznetgio serta instalasi aplikasi-aplikasi yang dibutuhkan untuk melakukan deploy aplikasi wayshub-frontend menggunakan docker.

1. Login terlebih dahulu ke dalam website Biznetgio lalu rebuild server, jangan lupa untuk stop terlebih dahulu server berjalan yang akan direbuild.
![Alt text](docker-and-docker-compose/rebuild-server-1.png)

2. Melaukan rebuild dengan system operasi ubuntu versi 22.04
![Alt text](docker-and-docker-compose/rebuild-server-2.png)

3. Membuat user baru pada server yaitu user team1 untuk di dalamnya melakukan instalasi docker serta memasukan ke dalam group sudo.
![Alt text](docker-and-docker-compose/make-user.png)

4. Melakukan setting ssh password agar user yang baru dibuat dapat login menggunakan password.  
![Alt text](docker-and-docker-compose/setting-ssh-password-2.png)
    
    >[!NOTE]
    >Pada server ubuntu versi 22.04, terdapat settingan ssh tambahan yang harus diubah agar dapat diakses menggunakan password yaitu pada folder sshd_config.d.

    ![Alt text](docker-and-docker-compose/setting-ssh-password-4.png)

5. Melakukan install docker dengan membuat script dengan nama `docker_install.sh`.  
![Alt text](docker-and-docker-compose/docker-install-1.png)
Simpan script jika sudah selesai.
![Alt text](docker-and-docker-compose/docker-install-2.png)
Berikan mode execute agar script yang dibuat dapat dijalankan dengan menggunakan perintah 
    ```
    sudo chmod +x docker_install.sh
    ```
    ![Alt text](docker-and-docker-compose/docker-install-3.png)

6. Melakukan git clone baik aplikasi frontend ataupun backend.
![Alt text](docker-and-docker-compose/git-clone.png)

7. Setting api pada frontend agar dapat terhubung ke backend.
![Alt text](docker-and-docker-compose/setting-api-fe-1.png)
`baseURL` disesuaikan dengan backend yang sudah disetting, yaitu dimana backend nantinya akan berjalan pada domain `api.team1.studentdumbways.my.id`
![Alt text](docker-and-docker-compose/setting-api-fe-2.png)

8. Membuat dockerfile di dalam folder wayshub frontend agar aplikasi dapat dijalankan menggunakan docker compose.
![Alt text](docker-and-docker-compose/dockerfile-fe.png)

9. Melakukan setting backend agar nantinya backend dapat terhubung ke database.
![Alt text](docker-and-docker-compose/setting-backend-be-1.png)
Ubah script pada bagian deployment menyesuaikan database yang akan dijalankan atau database yang sudah berjalan.
![Alt text](docker-and-docker-compose/setting-backend-be-2.png) 

10. Membuat dockerfile di dalam folder wayshub backend agar aplikasi dapat berjalan menggunakan docker compose. 
![Alt text](docker-and-docker-compose/dockerfile-be.png) 

11. Membuat docker network agar setiap aplikasi yang berjalan pada docker compose berjalan pada network yang sama yaitu pada network team1 sehingga antar container dapat saling terhubung. 
![Alt text](docker-and-docker-compose/creat-docker-network.png) 

12. Membuat docker compose file yang isinya berupa script atau perintah untuk melakukan instalasi database, aplikasi frontend, backend serta instalasi web server. 
![Alt text](docker-and-docker-compose/docker-compose-1.png) 
![Alt text](docker-and-docker-compose/docker-compose-2.png) 

13. Running docker database terlebih dahulu agar nantinya backend dapat terhubung dan melakukan migrasi database, perintah yang digunakan:
    ```
    docker compose up -d database
    ```
    >[!NOTE]
    >Sesuaikan *(database)* dengan nama service yang digunakan pada docker compose.

    ![Alt text](docker-and-docker-compose/running-docker-db.png) 

14. Membuat reverse proxy agar aplikasi yang berjalan dapat diakses menggunakan domain menggunakan web server nginx. Pastikan agar script reverse proxy yang dibuat berada di dalam directory yang sesuai dengan volume yang dibuat pada docker compose file.
![Alt text](docker-and-docker-compose/make-reverse-proxy.png) 
![Alt text](docker-and-docker-compose/make-reverse-proxy-2.png) 

15. Copy file ssl certbot yang sudah digenerate sebelumnya menggunakan ssl cloudflare wildcard sesuai dengan directory yang dibuat menggunakan docker compose.
![Alt text](docker-and-docker-compose/copy-ssl-cloudflare.png)
    >[!NOTE]
    >Untuk melakukan setting cloudflare serta bagaimana cara melakukan generate SSL Certificate dapat dilihat pada tugas sebelumnya [Deploy Application](../../Week-1/Day-2/deploy-application.md) pada step ke 5.

16. Melakukan docker compose up agar semua aplikasi dapat berjalan.  
![Alt text](docker-and-docker-compose/docker-compose-up.png)

17. Selanjutnya adalah docker push di mana natinya image yang telah terbuat agar dimasukan ke dalam docker registry.
![Alt text](docker-and-docker-compose/docker-push.png) 

18. Aplikasi dapat berjalan serta dapat melakukan login ke dalam aplikasi.
![Alt text](docker-and-docker-compose/registration.png) 
![Alt text](docker-and-docker-compose/Login.png) 