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
#### 1. Buat terlebih dahulu directory pada folder nginx dengan perintah. 

    cd /etc/nginx
  <br/>
    
    sudo mkdir akuma 

  ![cd nginx](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/42aac019-6c71-475d-a79b-b724cff92952)

  ![sudo mkdir akuma](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/60343432-f11d-4ddf-978d-50b29e568481)

#### 2. Masuk ke dalam direktori yang sudah dibuat kemudian buat file dengan nama my.reverse-proy.conf.

    cd akuma
    sudo nano my.reverse-proxy.conf

  ![sudo nano reverse](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/0d8d82aa-6ecd-43e3-a7f6-d0500796c2c7)

Selanjutnya masukan konfigurasi.

    server { 
    server_name akuma.xyz; 
  
    location / { 
             proxy_pass http://127.0.0.1:3000;
    }
    }

  ![my reverse](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6ba81081-3dba-4dd9-967f-c0e8f3bc3338)

Kemudian simpah konfigurasi tersebut.

#### 3. Selanutnya keluar dari direktori akuma dan masuk ke dalam file nginx.conf.

    cd ..
  
  ![back to before](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/574d1829-ca38-4d56-a61e-3b739868c7ac)

    sudo nano nginx.conf

  ![sudo nginx conf](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/80221b12-756e-43d4-a63a-4c747a7350e4)

Pergi ke bagian include kemudian masukan lokasi dari direktori yang berisi konfigurasi reverse proxy.

  ![sudo nginx conf](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e36f5c12-fb85-4a71-a7b2-135f48c4d65c)

Kemudian lakukan pengecekan konfigurasi apakah sudah aman atau belum dengan perintah.

    sudo nginx -t

  ![sudo nginx -t](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9ff1d8f4-d8a8-4fb7-ba86-566dd5635e8d)

Jika tidak terdapat error, rertart nginx agar konfigurasi yang dibuat bisa berjalan dengan perintah. 

    sudo systemctl restart nginx

  ![sudo restart](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e99cc898-d8e6-4b1a-ac60-717af1edd77f)

#### 4. Selanutnya adalah membuat virtual host pada lokal server yang berada di dalam file `/etc/hosts`.

    sudo nano /etc/hosts

   ![sudo etchost](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6797dd82-851a-4c0c-b87b-556acb051825)

Selanjutnya masukan IP Server disertai nama domain yang diinginkan.

   ![etc host](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/230adb72-2ff6-44a3-873c-d4f26b58503c)

Lakukan pengecekan pada web browser.

   ![bad gateway](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/796e0025-004b-4850-aef8-77495fd2170a)

Hasilnya adalah bad gateway karena belum adanya aplikasi yang berjalan pada server. Oleh karena itu kita akan mencoba menajalanlan aplikasi bernama dumbsound yang akan didownload melalui git dengan perintah berikut.

    git clone https://github.com/RizqyAlvindra/dumbsound.git

   ![git clone](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/1ed31d65-9f83-421a-a63f-3bdaf2229e60)

Masuk ke dalam direktori dumbsound kemudian jalankan perintah `npm install` untuk melakukan instalasi package package yang dibutuhkan oleh aplikasi.

    cd dumbsound/
<br/>

    npm install

   ![npm install](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/17e0eb35-55f8-4e2b-b1f6-53ad8dcf9a12)

#### 5. Langkah selanjutnya jalankan aplikasi dengan perintah `npm start`.

    npm start

   ![npmstart](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/36daff87-59c6-4c36-9122-4baee3004637)
 
   ![npmstart1](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9e8823c3-9264-4a2f-8b48-fbdf25c0719f)

Jika sudah lakukan pengecekan lagi pada browser dengan memasukan domain yang telah dibuat.

   ![resultpage](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3bfc9238-1b72-45a0-9df6-8b1c24ea19a1)

Aplikasi tersebut juga bisa dijalankan menggunakan `pm2` yang sudah kita install sebelumnya sehingga aplikasi bisa berjalan di background.

   ![pm2start](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ea60e3d7-6fac-4248-9e0c-a31febfb2ae5)







## Load Balancing
