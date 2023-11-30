# DEVOPS-BATCH-19
##### Daily Task - Day 6 - Ardi Solehuddin

-  Jelaskan apa itu web server dan jelaskan bagaimana cara kerjanya
-  Buatlah reverse proxy sederhana menggunakan nginx
-  Buatlah -+ 3 buah vm (1 nginx, 2 aplikasi) untuk mengimplementasikan loadbalancing applikasi yang ada di nomer 2

## Web Server
web server adalah perangkat lunak yang memberi layanan berupa data. Web server bertugas untuk menerima permintaan HTTPS atau HTTP dari pengguna internet. Setelah itu, web server akan menyediakan respons atas permintaan tersebut dalam bentuk halaman web.

#### Cara Kerja Web Server
Ketika terdapat pengguna atau client yang membutuhkan data maka permintaan atau request tersebut akan diteruskan ke server database melalui web server, kemudian web server menerima balasan dari database dan akan menerukan data tersebut ke pengguna lagu berbentuk halaman pada website. 

## Reverse Proxy
Reverse proxy adalah sebuah server yang bertindak sebagai perantara antara klien dan server tujuan. Ketika klien melakukan permintaan, reverse proxy akan menerima permintaan tersebut dan akan mengirimkannya ke server tujuan. Kemudian, server tujuan akan memberikan respons ke reverse proxy, dan reverse proxy akan meneruskannya kembali ke klien.

### Konfigurasi Proxy Server
#### 1. Buat terlebih dahulu directory pada folder nginx dengan perintah 

    cd /etc/nginx
  <br/>
    
    sudo mkdir akuma 

  ![cd nginx](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/42aac019-6c71-475d-a79b-b724cff92952)

  ![sudo mkdir akuma](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/60343432-f11d-4ddf-978d-50b29e568481)

#### 2. Masuk ke dalam direktori yang sudah dibuat kemudian buat file dengan nama my.reverse-proy.conf

    cd akuma
    sudo nano my.reverse-proxy.conf

  ![sudo nano reverse](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/0d8d82aa-6ecd-43e3-a7f6-d0500796c2c7)

Selanjutnya masukan konfigurasi

    server { 
    server_name akuma.xyz; 
  
    location / { 
             proxy_pass http://127.0.0.1:3000;
    }
    }

  ![my reverse](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6ba81081-3dba-4dd9-967f-c0e8f3bc3338)

Kemudian simpah konfigurasi tersebut.

#### 3. Selanutnya keluar dari direktori akuma dan masuk ke dalam file nginx.conf

    cd ..
  
  ![back to before](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/574d1829-ca38-4d56-a61e-3b739868c7ac)

    sudo nano nginx.conf

  ![sudo nginx conf](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/80221b12-756e-43d4-a63a-4c747a7350e4)

Pergi ke bagian include kemudian masukan lokasi dari direktori yang berisi konfigurasi reverse proxy 

  ![sudo nginx conf](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e36f5c12-fb85-4a71-a7b2-135f48c4d65c)

Kemudian lakukan pengecekan konfigurasi apakah sudah aman atau belum dengan perintah

    sudo nginx -t

  ![sudo nginx -t](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9ff1d8f4-d8a8-4fb7-ba86-566dd5635e8d)

Jika tidak terdapat error, rertart nginx agar konfigurasi yang dibuat bisa berjalan dengan perintah. 

    sudo systemctl restart nginx

  ![sudo restart](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e99cc898-d8e6-4b1a-ac60-717af1edd77f)


















## Load Balancing
