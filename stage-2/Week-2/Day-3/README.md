# DEVOPS-BATCH19-STAGE2
#### Daily Task - Day 3 - Ardi Solehuddin

- Menjelaskan langkah-langkah melakukan rebuild server [BiznetGio](biznetgio.com), dan ubah menggunakan os ubuntu22
- Setelah server sudah selesai ter rebuild, buatlah suatu user baru dengan nama **team kalian** lalu implementasikan penggunaan ssh dengan menggunakan **PASSWORD ONLY** tanpa SSH-KEY.
- Membuat bash script untuk melakukan installasi docker. 
- Deploy aplikasi Web Server, Frontend, Backend, serta Database on top `docker compose`
- Membuat suatu docker compose yang berisi beberapa service:
    - Web Server
    - Frontend
    - Backend
    - Database
- Membuat suatu custom network dengan nama **team**, lalu pasang ke setiap service yang kalian miliki.
- Deploy database menggunakan mysql dengan versi terbaru, dan pasang volume di bagian database.
- Building image frontend dan backend dengan dockerized image sekecil mungkin dan sesuaikan configuration dari backend ke database maupun frontend ke backend sebelum di build menjadi docker images.
- Web Server konfigurasi reverse-proxy menggunakan nginx on top docker.
    - **SSL CLOUDFLARE OFF!!!**
    - Gunakan docker volume untuk membuat reverse proxy
    - SSL sebisa mungkin gunakan wildcard
    - Untuk DNS bisa sesuaikan seperti contoh di bawah ini
      - Frontend team1.studentdumbways.my.id
      - Backend api.team1.studentdumbways.my.id
- Push image ke docker registry.
- Aplikasi dapat berjalan dengan sesuai seperti melakukan login/register.

## Requirements
- Server : BiznetGio NeoLite XS 2.2 (2CPU, 2GB RAM, 60 Disk Storage)
- Docker
- Frontend Apps : NPM & NVM 14.x Version, [wayshub-frontend clone](https://github.com/dumbwaysdev/wayshub-frontend)
- Backend Apps : NPM & NVM 14.x Version, [wayshub-backend clone](https://github.com/dumbwaysdev/wayshub-backend)
- [Docker Registry](https://hub.docker.com/)
- Webserver : Nginx
- DNS : Cloudflare

## Langkah Pengerjaan
1. [Rebuild Server Serta Install Docker dan aplikasi](docker-task.md)