# DEVOPS-BATCH19-STAGE2
#### Weekly Task - Week 1 - Ardi Solehuddin

Pada minggu ini saya mengerjakan bagaimana melakukan deploy aplikasi frontend dan backend yang terhubung dengan database serta bagaimana aplikasi tersebut dapat diakses oleh publik melalui internet. Terdapat tugas harian yang akan dikerjakan secara berkala yaitu apa saja yang harus dikerjakan setiap selesai kelas serta melakukan riset lebih mendalam terhadap hal yang dikerjakan. Adapun tugas tugas yang diberikan dibagi setiap harinya, antara lain :

#### SERVER NAME

Server Untuk Frontend dan Web Server : gateway<br/> 
Server Untuk Backend dan Database : appserver

#### [Hari Pertama](Day-1/README.md)
1. Membuat VM di [BiznetGio](biznetgio.com) tipe _NeoLite XS 1.1_ dengan spesifikasi 1 CPU, 1 GB RAM, 60 GB Storage dengan OS Ubuntu 20.04/22.04.

2. Membuat user baru serta melakukan implementasi penggunaan SSH-KEY. 

3. Deploy aplikasi _wayshub-frontend_ menggunakan nodejs versi 14.x.

4. Membuat web server dengan nginx dan reverse proxy serta menggunakan domain yang sudah ditentukan menggunakan cloudflare.

#### [Hari Kedua](Day-2/README.md)
1. Membuat VM di [BiznetGio](biznetgio.com) tipe _NeoLite SS 2.2_ dengan spesifikasi 2 CPU, 2 GB RAM, 60 GB Storage dengan OS Ubuntu 20.04/22.04.

2. Membuat user baru serta melakukan implementasi penggunaan SSH-KEY. 

3. Melakukan deploy database _mysql_
    - Setup secure_installation
	- Add password for `root` user
	- Create new user for mysql
	- Create new database
	- Create privileges for new users so they can access the database you created
    - Remote database 

4. Deploy aplikasi Wayshub-Backend 
	- Clone wayshub backend application
	- Use Node Version 14
	- Dont forget to change configuration on `wayshub-backend/config/config.json` and then adjust it to your database.
	- Install sequelize-cli 
	- Running migration
	- Deploy apllication on Top PM2

5. Deploy aplikasi Wayshub-Frontend
	- Clone wayshub frontend application
	- Dont forget to change configuration on `wayshub-frontend/src/config/api.js` and then adjust it to your backend application.
	- Deploy apllication on Top PM2

6. Web Server
	- Frontend (ex. amanda.studentdumbways.my.id)
	- Backend (ex. api.amanda.studentdumbways.my.id)
	- SSL CLOUDFLARE OFF, use certbot for generate certificate. 