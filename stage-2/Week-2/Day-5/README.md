# DEVOPS-BATCH19-STAGE2
#### Daily Task - Day 5 - Ardi Solehuddin

- Buat akun di gitlab.com
- Push SCM dari local-server ke gitlab
- Membuat beberapa Job menggunakan gitlabci untuk aplikasi:
    - Job Frontend
    - Job Backend
    - Script CICD atur flow pengupdate an aplikasi mencakup
        - Pull dari repository
        - Dockerize/Build aplikasi kita
        - push image ke docker hub
        - Test application
        - pull new image
        - Deploy application

## Requirements
- Server : BiznetGio NeoLite XS 2.2 (2CPU, 2GB RAM, 60 Disk Storage)
- Frontend Apps : NPM & NVM 14.x Version, [wayshub-frontend clone](https://github.com/dumbwaysdev/wayshub-frontend)
- Backend Apps : NPM & NVM 14.x Version, [wayshub-backend clone](https://github.com/dumbwaysdev/wayshub-backend)
- Docker
- GitLab
- [Docker Registry](https://hub.docker.com/)
- Webserver : Nginx
- DNS : Cloudflare

## Langkah Pengerjaan
1. [Langkah-Langkah Pengerjaan GitLab](gitlab-task.md)