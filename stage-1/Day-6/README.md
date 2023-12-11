# DEVOPS-BATCH-19
##### Daily Task - Day 6 - Ardi Solehuddin

-  Jelaskan apa itu web server dan jelaskan bagaimana cara kerjanya
-  Buatlah reverse proxy sederhana menggunakan nginx
-  Buatlah -+ 3 buah vm (1 nginx, 2 aplikasi) untuk mengimplementasikan loadbalancing applikasi yang ada di nomer 2

## Web Server
web server adalah perangkat lunak yang memberi layanan berupa data. Web server bertugas untuk menerima permintaan HTTPS atau HTTP dari pengguna internet. Setelah itu, web server akan menyediakan respons atas permintaan tersebut dalam bentuk halaman web.

#### Cara Kerja Web Server
Ketika terdapat pengguna atau client yang membutuhkan data maka permintaan atau request tersebut akan diteruskan ke server database melalui web server, kemudian web server menerima balasan dari database dan akan meneruskan data tersebut ke pengguna lagi berbentuk halaman pada website. 

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

#### 4. Selanjutnya adalah membuat virtual host pada lokal server yang berada di dalam file `/etc/hosts`.

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
Load balancing merupakan proses pendistribusian traffic atau lalu lintas jaringan secara efisien ke dalam sekelompok server, atau yang lebih dikenal dengan server pool atau server farm. Load balancing ini berguna agar salah satu server dari website yang mendapatkan banyak lalu linta kunjungan tidak mengalami kelebihan beban.

### Konfigurasi Load Balancing
Sebelumnya saya sudah membuat tiga buah virtual server bernama akuma, voxy dan zero. Server akuma nantinya akan bertindak sebagai load balancer dan server voxy dengan server zero akan berjalan sebagai server dari aplikasi.

   ![multipass](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/f058123a-e0d9-4310-9c6a-6345388dbfc7)

   ![zero](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/4264a76c-2256-45b4-aa90-6ed472b582c0)

   ![voxy](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/90622205-a109-4414-bf66-110cc920c315)

#### 1. Langkah pertama masuk ke dalam file konfigurasi file proxy yang sudah dibuat sebelumnya pada server akuma dengan perintah:

        sudo nano /etc/nginx/akuma/my.reverse-proxy.conf

   ![sudo nano myreverse](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/30fba49c-e33b-4631-9add-c33ae408c8bb)

Kemudian masukan konfigurasi ke dalam file tersebut 

   ![upstream](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/aacdaf4d-11f2-4a26-b516-665ce3039a95)

        upstream domain {
            server 10.182.205.169:3000;
            server 10.182.205.76:3000;
            server 10.182.205.185:3000;
        }
        server {
            server_name akuma.xyz;

            location / {
                 proxy_pass http://127.0.0.1:3000;
                }
            }

Masukan IP ketiga server pada bagian upstream diikuti oleh port yang digunakan oleh aplikasi.

#### 2. Check dan restart nginx jika sudah tidak ada error setelah melakkukan konfigurasi.

    sudo nginx -t
<br/>

    sudo systemctl restart nginx

   ![sudo nginx   restart](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ba2cf152-d01f-448a-9c15-a6da810d4911)

#### 3. Jalankan aplikasi pada kedua server yaitu server voxy dan zero dengan perintah :
    npm start

   ![zero start](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/d54e67c4-8a9d-46f2-bfa7-603d646b25b5)

   ![voxy start](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/1bfc7ee1-53cc-4008-b964-ffdaa17e2a71)

#### 4. Periksa apakah aplikasi berhasil berjalan

   ![akuma success](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/69e872f1-6c22-435f-b65a-807bf05865c9)

Jika aplikasi dapat berjalan, lakukan pengujian load balancing dengan mematikan salah satu server, pada kasus ini server voxy dimatikan

   ![voxy died](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/8e2f1cd7-667b-477a-b685-8bec1982b136)

Kemudian lakukan pengecekan kembali apakah web tetap berjalan

   ![akuma success](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/554b4c53-a031-42ec-bbd7-ab9a06ebf030)

Dapat dilihat bahwa aplikasi web tetap berjalan menandakan bahwa load balance berhasil.
   
