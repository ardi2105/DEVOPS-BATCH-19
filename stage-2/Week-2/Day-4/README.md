# DEVOPS-BATCH19-STAGE2
#### Daily Task - Day 4 - Ardi Solehuddin

- Jelasakan langkah-langkah melakukan rebuild server BiznetGio, dan ubah menggunakan os ubuntu22
- Installasi Jenkins on top Docker or native
- Setup SSH-KEY di local server jenkins kalian, agar dapat 
- login ke dalam server menggunakan SSH-KEY 
- Reverse Proxy Jenkins
  - gunakan domain ex. pipeline-team4.studentdumbways.my.id
  - reverse proxy sesuaikan dengan ketentuan yang ada di dalam Jenkins documentation
- Membuat beberapa Job untuk aplikasi: 
    - Job Frontend
    - Job Backend
    - Script CICD flow pengupdate an aplikasi mencakup
        - Pull dari repository
        - Dockerize/Build aplikasi kita
        - Test application
        - Deploy aplikasi on top Docker
        - Push ke Docker Hub
- Auto trigger setiap ada perubahan di SCM
- Job notification ke discord

## Requirements
- Server : BiznetGio NeoLite XS 2.2 (2CPU, 2GB RAM, 60 Disk Storage)
- Docker
- Jenkins
- Frontend Apps : NPM & NVM 14.x Version, [wayshub-frontend clone](https://github.com/dumbwaysdev/wayshub-frontend)
- Backend Apps : NPM & NVM 14.x Version, [wayshub-backend clone](https://github.com/dumbwaysdev/wayshub-backend)
- [Docker Registry](https://hub.docker.com/)
- Webserver : Nginx
- DNS : Cloudflare

## Langkah Pengerjaan
1. [Langkah-Langkah Pengerjaan Jenkins](jenkins-task.md)
