# DEVOPS-BATCH19-STAGE2
#### Weekly Task - Week 2 - Ardi Solehuddin

Pada minggu ini saya mengerjakan bagaimana melakukan monitoring menggunakan grafhana serta bagaimana cara menggunakan IAC ansible. Terdapat tugas harian yang akan dikerjakan secara berkala yaitu apa saja yang harus dikerjakan setiap selesai kelas serta melakukan riset lebih mendalam terhadap hal yang dikerjakan. Adapun tugas tugas yang diberikan dibagi setiap harinya, antara lain :

#### Hari Pertama
1. Setup node-exporter, prometheus dan Grafana menggunakan docker

2. install node-exporter di appserver & gateway

3. Reverse Proxy
    - Bebas menggunakan nginx native / docker
    - Domain
      - exporter-$name.studentdumbways.my.id (node exporter)
      - prom-$name.studentdumbways.my.id (prometheus)
      - monitoring-$name.studentdumbways.my.id (grafana)
    - SSL Cloufflare on / certbot SSL biasa / wildcard SSL diperbolehkan
4. Dengan Grafana, buatlah :
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

#### Hari Kedua
1. [Local]
    - Buat konfigurasi Ansible & sebisa mungkin maksimalkan penggunaan ansbile untuk melakukan semua setup.

2. [ansible]
<br/>Buatlah ansible untuk :
    - Membuat user baru, gunakan login ssh key & password
    - Instalasi Docker
    - Deploy application frontend yang sudah kalian gunakan sebelumnya menggunakan ansible.
    - Instalasi Monitoring Server (node exporter, prometheus, grafana)
    - Setup reverse-proxy
    - Generated SSL certificate

