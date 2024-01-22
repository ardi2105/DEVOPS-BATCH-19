## Rebuild Server Serta Install Jenkins On Top Docker Dan Automasi Aplikasi
Berikut adalah dokumentasi langkah langkah bagaimana melakukan rebuild VM di Biznetgio serta instalasi jenkins on top docker serta membuat pipeline pada jenkins untuk menjalankan aplikasi-aplikasi yang dibutuhkan.

1. Langkah pertama buat docker compose untuk melakukan instalasi jenkins dan nginx untuk web server.
![Alt text](jenkins/docker-compose.yaml.png) 

2. Selanjutnya buat direktori certbot yang nantinya digunakan untuk generate certificate ssl wildcard.
![Alt text](jenkins/mkdir-reverse-proxy.png) 

3. Membuat reverse proxy untuk jenkins agar dapat diakses menggunakan domain.
![Alt text](jenkins/reverse-proxy.conf.png) 

4. Melakukan install java agar jenkins dapat berjalan.  
![Alt text](jenkins/install-java-jenkins.png)

5. Selanjutnya yaitu melakukan instalasi jenkins dengan menggunakan perintah `docker compose up` kemudian enable serta cek status jenkins.
![Alt text](jenkins/jenkins-status.png) 

6. Selanjutnya adalah memasukan password ketika pertama kali melakukan instalasi jenkins agar dapat terhubung dengan jenkins web.
![Alt text](jenkins/jenkins-password.png) 

7. Lakukan instalasi plugin jenkins yang dibutuhkan
![Alt text](jenkins/jenkins-plugin-install.png) 

8. Membuat jenkins folder untuk di dalamnya berisi pipeline jobs frontend dan backend. 
![Alt text](jenkins/folder-wayshub.png)   

10. Reverse proxy untuk aplikasi frontend dan backend. 
![Alt text](jenkins/reverse-proxy-jenkins.png) 

11. Membuat file jenkinsfile untuk aplikasi frontend.
![Alt text](jenkins/jenkinsfile-fe.png) 

12. Install plugin ssh agent dan setting terlebih dahulu agar jenkins dapat terhubung ke repository github di mana repository untuk aplikasi frontend dan backend.
![Alt text](jenkins/ssh-agent.png)
![Alt text](jenkins/ssh-credentials.png) 

12. Membuat file jenkinsfile untuk aplikasi frontend.
![Alt text](jenkins/Jenkinsfile-backend.png) 

13. Selanjutnya yaitu membuat jenkins pipeline untuk backend agar aplikasi dapat berjalan secara otomatis.  
![Alt text](jenkins/pipeline-backend-1.png) !

15. Setting jenkins pipeline agar dapat terhubung ke repository. 
![Alt text](jenkins/pipeline-backend-2.png) 

16. Running job aplikasi backend dan dapat proses pipeline untuk aplikasi backend berjalan dengan lancar. 
![Alt text](jenkins/backend-build.png) 

17. Membuat sebuah pipeline fronteng pada jenkins.
![Alt text](jenkins/pipeline-frontend-1.png) 

18. Melakukan setting pipeline agar dapat terhububung ke repository.
![Alt text](jenkins/pipeline-frontend-2.png) 

19. Lakukan build dan dapat dilihat proses pipeline jenkins untuk aplikasi frontend dapat berjalan dengan lancar.
![Alt text](jenkins/frontend-build.png) 

21. Install plugin discord notifer agar ketika terdapat perubahan pada aplikasi atau adanya commit atau trigger job, maka akan menampilkan notifikasi.
![Alt text](jenkins/discord-notif.png)
![Alt text](jenkins/notif-discord.png) 

24. Melakukan pengecekan berjalannya aplikasi.
![Alt text](jenkins/aplikasi-run.png)