# DEVOPS-BATCH19-STAGE2
#### Daily Task - Day 2 - Ardi Solehuddin

- Membuat VM di [BiznetGio](biznetgio.com) tipe _NeoLite XS 1.1_ 
- Membuat user baru serta melakukan implementasi penggunaan SSH-KEY. 
- Deploy aplikasi _wayshub-frontend_ menggunakan nodejs versi 14.x.
- Membuat web server dengan nginx dan reverse proxy serta menggunakan domain yang sudah ditentukan menggunakan cloudflare.

- Membuat VM di [BiznetGio](biznetgio.com) tipe _NeoLite SS 2.2_ 
- Membuat user baru serta melakukan implementasi penggunaan SSH-KEY. 
- Melakukan deploy database _mysql_
    - Setup secure_installation
	- Add password for `root` user
	- Create new user for mysql
	- Create new database
	- Create privileges for new users so they can access the database you created
    - Remote database 
- Deploy aplikasi Wayshub-Backend 
	- Clone wayshub backend application
	- Use Node Version 14
	- Dont forget to change configuration on `wayshub-backend/config/config.json` and then adjust it to your database.
	- Install sequelize-cli 
	- Running migration
	- Deploy apllication on Top PM2

- Deploy aplikasi Wayshub-Frontend
	- Clone wayshub frontend application
	- Dont forget to change configuration on `wayshub-frontend/src/config/api.js` and then adjust it to your backend application.
	- Deploy apllication on Top PM2

- Web Server
	- Frontend (ex. amanda.studentdumbways.my.id)
	- Backend (ex. api.amanda.studentdumbways.my.id)
	- SSL CLOUDFLARE OFF, use certbot for generate certificate. 

## Requirements
- Server : BiznetGio NeoLite XS 1.1 (1CPU, 1GB RAM, 60 Disk Storage)
- Webserver : Nginx
- Frontend Apps : npm & nvm 14.x Version, [wayshub-frontend clone](https://github.com/dumbwaysdev/wayshub-frontend)
- Backend : npm & nvm 14.x Version [wayshub-backend](https://github.com/dumbwaysdev/wayshub-backend)
- Database : mysql
- Production Process Manager / pm2
- Sequelize-cli
- DNS : Cloudflare
- SSL : letsencrypt

## Langkah Pengerjaan 
1. [Setup Server](<1. setup-server.md>)
2. [Deploy Application](<2. deploy-application.md>)
