## Deploy Aplikasi, Konfigurasi Database & Migrasi Database 
Berikut adalah dokumentasi langkah langkah bagaimana melakukan Deploy aplikasi backend pada vm yang telah dibuat di BiznetGio mulai dari pembuatan user baru untuk menaruh berkas aplikasi hingga aplikasi dapat diakses secara publik.

1. Setting database dengan melakukan pengamanan terlebih dahulu pada user root. Secara default password root pada mysql database kosong, maka perlu diberi password dengan menggunakan cara masuk ke dalam mysql root terlebih dahulu kemudian masukan perintah : 

    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Ardi@3311';

    ![Alt text](deploy-application/root-password.png)
    Exit, kemudian root akan mengharuskan login menggunakan password
    ![Alt text](deploy-application/login-root-pawd.png)

2. Membuat databases yang akan digunakan oleh aplikasi backend serta user baru yang akan diberikan akses ke 1 database tersebut.<br/>
Membuat database bernama wayshub   
![Alt text](deploy-application/create-databases.png)
Membuat user ardi dengan semua privileges terhadap database dan tables wayshub serta dapat diremote dari IP manapun ditandai dengan lambang %.  
![Alt text](deploy-application/create-user.png)
![Alt text](deploy-application/grant-privileges.png)
Dapat dilihat database yang muncul pada user ardi, terdapat database wayshub.
![Alt text](deploy-application/show-databases.png)
Ubah config bind address agar dapat melakukan remote pada `sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf`
![Alt text](deploy-application/setting-mysqld.cnf.png)
![Alt text](deploy-application/setting-mysqld.cnf-1.png)
Berhasil melakukan remote mysql user ardi dari server voxy.
![Alt text](deploy-application/remote-mysql.png)

3. Cloning aplikasi wayshub-frontend dengan git clone.
![Alt text](deploy-application/git-clone-backend.png)
![Alt text](deploy-application/git-clone-backend-1.png)
Lakukan npm install untuk melakukan instalasi package atau dependensi yang dibutuhkan oleh aplikasi.
![Alt text](deploy-application/npm-install.png)
Setting `config.json` pada direktori config dengan mengarahkan pada database yang sudah dibuat sebelumnya
![Alt text](deploy-application/config.json.png)
![Alt text](deploy-application/config.json-1.png)
Lakukan `db:migrate` untuk melakukan migrasi dari backend ke database
![Alt text](deploy-application/db-migrate.png)
![Alt text](deploy-application/db-migrate-1.png)

4. Melakukan running application menggunakan `pm2 init simple`
![Alt text](deploy-application/pm2-init-simple.png)
![Alt text](deploy-application/sudo-nano-ecosystem.png)
![Alt text](deploy-application/sudo-nano-ecosystem-1.png)
![Alt text](deploy-application/pm2-start.png)
![Alt text](deploy-application/running-backend.png)

5. Membuat proxy server untuk aplikasi backend dan mendaftarkan dns menggunakan cloudflare serta melakukan setting api.js pada frontend agar terhubung ke database.
 ![Alt text](deploy-application/proxy-server-backend.png)
 ![Alt text](deploy-application/restart-nginx.png)
 ![Alt text](deploy-application/config-api.js.png)
 ![Alt text](deploy-application/config-api.js-1.png)
 ![Alt text](deploy-application/cloudflare-backend.png)
 ![Alt text](deploy-application/backend-running-domain.png)

6. Melakukan generate certicate ssl menggunakan letsencrypt.
![Alt text](deploy-application/sudo-nano-voxy.ini.png)
![Alt text](deploy-application/sudo-nano-voxy.ini-1.png)
![Alt text](deploy-application/sudo-chmod-voxy.ini.png)
![Alt text](deploy-application/sudo-certbot.png)
![Alt text](deploy-application/ssl-certbot.png)

7. Melakukan running application serta melakukan pengujian terhubung atau tidaknya aplikasi 
![Alt text](deploy-application/start-backend.png)
![Alt text](deploy-application/start-frontend.png)
![Alt text](deploy-application/regis-success.png)
![Alt text](deploy-application/database-in.png)