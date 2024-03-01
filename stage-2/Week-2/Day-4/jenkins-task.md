## Rebuild Server Serta Install Jenkins On Top Docker Dan Automasi Aplikasi

### Jenkins 
Jenkins adalah sebuah perangkat lunak open-source yang digunakan untuk otomatisasi proses pengembangan perangkat lunak. Ini adalah salah satu alat yang paling umum digunakan dalam praktik Continuous Integration (CI) dan Continuous Deployment (CD), di mana perubahan kode yang dilakukan oleh para pengembang diperiksa secara otomatis dan diintegrasikan ke dalam proyek perangkat lunak secara berkala.

### Langkah Pengerjaan
Berikut adalah dokumentasi langkah langkah bagaimana melakukan rebuild VM di Biznetgio serta instalasi jenkins on top docker serta membuat pipeline pada jenkins untuk menjalankan aplikasi-aplikasi yang dibutuhkan.

1. Langkah pertama buat docker compose untuk melakukan instalasi jenkins dan nginx untuk web server.
![Alt text](images/docker-compose.yaml.png) 

2. Selanjutnya buat direktori certbot yang nantinya digunakan untuk generate certificate ssl wildcard.
![Alt text](images/mkdir-reverse-proxy.png) 

3. Membuat reverse proxy untuk jenkins agar dapat diakses menggunakan domain.
![Alt text](images/reverse-proxy.conf.png) 

4. Melakukan install java agar jenkins dapat berjalan.  
![Alt text](images/install-java-jenkins.png)

5. Selanjutnya yaitu melakukan instalasi jenkins dengan menggunakan perintah `docker compose up` kemudian enable serta cek status jenkins.
![Alt text](images/jenkins-status.png) 

6. Selanjutnya adalah memasukan password ketika pertama kali melakukan instalasi jenkins agar dapat terhubung dengan jenkins web.
![Alt text](images/jenkins-password.png) 

7. Lakukan instalasi plugin jenkins yang dibutuhkan
![Alt text](images/jenkins-plugin-install.png) 

8. Membuat jenkins folder untuk di dalamnya berisi pipeline jobs frontend dan backend. 
![Alt text](images/folder-wayshub.png)   

10. Reverse proxy untuk aplikasi frontend dan backend. 
![Alt text](images/reverse-proxy-jenkins.png) 

11. Membuat file jenkinsfile untuk aplikasi frontend.
![Alt text](images/jenkinsfile-fe.png) 

12. Install plugin ssh agent dan setting terlebih dahulu agar jenkins dapat terhubung ke repository github di mana repository untuk aplikasi frontend dan backend.
![Alt text](images/ssh-agent.png)
![Alt text](images/ssh-credentials.png) 

12. Membuat file jenkinsfile untuk aplikasi frontend.
![Alt text](images/Jenkinsfile-backend.png) 

13. Selanjutnya yaitu membuat jenkins pipeline untuk backend agar aplikasi dapat berjalan secara otomatis.  
![Alt text](images/pipeline-backend-1.png) !

15. Setting jenkins pipeline agar dapat terhubung ke repository. 
![Alt text](images/pipeline-backend-2.png) 

16. Running job aplikasi backend dan dapat proses pipeline untuk aplikasi backend berjalan dengan lancar. 
![Alt text](images/backend-build.png) 

17. Membuat sebuah pipeline fronteng pada jenkins.
![Alt text](images/pipeline-frontend-1.png) 

18. Melakukan setting pipeline agar dapat terhububung ke repository.
![Alt text](images/pipeline-frontend-2.png) 

19. Lakukan build dan dapat dilihat proses pipeline jenkins untuk aplikasi frontend dapat berjalan dengan lancar.
![Alt text](images/frontend-build.png) 

21. Install plugin discord notifer agar ketika terdapat perubahan pada aplikasi atau adanya commit atau trigger job, maka akan menampilkan notifikasi.
![Alt text](images/discord-notif.png)
![Alt text](images/notif-discord.png) 

24. Melakukan pengecekan berjalannya aplikasi.
![Alt text](images/aplikasi-run.png)