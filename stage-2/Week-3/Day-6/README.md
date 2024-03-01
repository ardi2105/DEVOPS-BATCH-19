# DEVOPS-BATCH19-STAGE2
#### Daily Task - Day 6 - Ardi Solehuddin

#### Hari Keenam
- Setup node-exporter, prometheus dan Grafana menggunakan docker
- install node-exporter di appserver & gateway
- Reverse Proxy
    - Bebas menggunakan nginx native / docker
    - Domain
      - exporter-$name.studentdumbways.my.id (node exporter)
      - prom-$name.studentdumbways.my.id (prometheus)
      - monitoring-$name.studentdumbways.my.id (grafana)
    - SSL Cloufflare on / certbot SSL biasa / wildcard SSL diperbolehkan
- Dengan Grafana, buatlah :
    -  Dashboard untuk monitor resource server (CPU, RAM & Disk Usage)  buatlah se freestyle kalian.
    -  Buat dokumentasi tentang rumus `promql` yang kalian gunakan
    -  Buat alerting dengan Contact Point pilihan kalian (discord, telegram, slack dkk)
    -  Untuk alert :
         - Boleh menggunakan alert manager / alert rule dari grafana
         - Ketentuan alerting yang harus dibuat
           - CPU Usage over 20%
           - RAM Usage over 75%
    -  Monitoring specific container
	 - deploy application frontend di app-server
         - monitoring frontend container

## Requirements
- Server : 
  - BiznetGio NeoLite XS 1.1 (1CPU, 1GB RAM, 60 Disk Storage)
  - BiznetGio NeoLite XS 2.2 (2CPU, 2GB RAM, 60 Disk Storage)
- Node-Exporter, Prometheus dan Grafana
- Docker
- Webserver : Nginx
- DNS : Cloudflare

## Langkah Pengerjaan
1. [Langkah Pengerjaan Monitoring](monitoring.md)