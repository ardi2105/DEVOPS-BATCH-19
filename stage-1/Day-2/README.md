# DEVOPS-BATCH-19
##### Daily Task - Day 2 - Ardi Solehuddin
-   Penjelasan Basic Network, IP Private & IP Public, dan IP Static & IP Dinamis(DHCP).
-   Apa itu linux Shell? (docs command line)

## Computer Networking
Jaringan komputer adalah terhubungnya 2 komputer atau lebih sehingga komputer tersebut bisa saling terhubung agar dapat bertukar informasi & data serta bisa berbagi sumber daya atau resource satu sama lain. Jaringan komputer dapat terhubung baik melalui kabel ataupun tanpa kabel (*wireless*)  
### IP Address
IP Address (Internet Protocol Address) adalah alamat komputer yang digunakan dalam jaringan agar dapat terhubung dengan komputer lain sehingga bisa berbagi data atau informasi. IP Address dapat diibaratkan sebagai alamat rumah di mana dibutuhkan ketika terdapat seseorang yang ingin mengirim suatu paket.  

#### IP Private & IP Public
IP Address terbagi menjadi dua jenis yaitu IP Pivate dengan IP  Public yang masing-masing memiliki perbedaan, antara lain :  
- IP Private adalah IP Address yang hanya bisa digunakan secara lokal, sering digunakan dalam jaringan LAN di mana komputer yang terhubung dan memiliki IP dapat saling berkomunikasi, namun tidak dapat untuk terhubung ke jaringan di luar LAN tersebut, contohnya tidak dapat terhubung ke internet.
- IP Public adalah IP Address yang umumnya diberikan oleh Internet Service Provider (Penyedia Jasa Internet) di mana IP ini digunakan untuk dapat terhubung ke jaringan yang lebih luas yang cakupannya seluruh dunia. Dengan memiliki IP public, suatu komputer bisa terhubung ke jaringan yang lebih luas melalui internet.

#### IP Dinamis (DHCP) & IP DHCP
Terdapat dua cara dalam pembagian alamat IP ke komputer yaitu secara dinamis dan statis, perbedaannya adalah :
- IP Dinamis (DHCP = Dynamic Host Control Protocol) di mana IP yang diberikan kepada komputer berubah ubah sesuai dengan IP Pool yang dimiliki oleh suatu server jaringan. Jangka waktu yang diberikan paling umum adalah 3 hari, jadi ketika waktu peminjaman (*lease*) IP Address sudah habis maka IP yang diberikan ke komputer akan berubah.
- IP Static adalah IP yang diberikan ke komputer secara manual di mana pengguna harus memasukan IP yang tersedia di server jaringan. IP yang di daftarkan haruslah tersedia, tidak boleh sudah digunakan oleh pengguna lain atau akan menyebabkan bentrok/*ip conflict*.

## Linux Shell
Linux Shell merupakan alat atau program berbasis text/*Command Line Interface(CLI)* yang digunakan oleh seorang pengguna untuk mengoperasikan sistem operasi pada komputer terutama pada sistem operasi berbasis unix/linux. Sangat penting memahami linux shell untuk bisa melakukan konfigurasi atua manajemen pada server yang menggunakan CLI. 

Pada dokumentasi ini akan berhubungan dengan bagaimana cara menggunakan sebagian perintah-perintah dasar pada Linux shell. 
 
## Perintah Perintah Pada Linux
Pada saat membuka terminal pada linux terdapat beberapa hal yang perlu diketahui pada tampilan awal linux seperti yang terdapat pada gambar di bawah. 

![Pengetahuan Dasar](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/530ed37b-c07a-4807-bdc6-21e8b8746022)

1. username : Tulisan di awal sebelum tanda @
2. Hostname/computer name : Tulisan setelah tanda @
3. Directory location : Tulisan setelah hostname
4. User biasa $ : Tulisan setelah directory location (bila tidak login sebagai root
5. Root user (#) : Tulisan setelah directory location (bila login sebagai root)
6. Login sebagai root : ketik `su` atau `sudo su
8. Logout dari root user : `exit`

---
### Perintah Dasar Pada Linux

#### 1. ls
   Perintah ls atau list digunakan untuk melihat file atau direktori ketika berada di dalam suatu direktori, contoh `ls -la` digunakan untuk melihat list file secara menurun beserta file yang tersembunyi.  

    ls -la

   ![ls -la](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e509486b-dbb2-4f95-a568-94dc0433505e)

   Perintah ls dapat digabungkan dengan perintah lanjutan untuk melihat list lebih detail.
    
   1. `ls -a` atau –all<br/>
       Tidak mengabaikan entri file yang dimulai dengan tanda titik
   2. `ls -A` atau –almost-all<br/>
       Tidak menampilkan titik dan titik titik (..)(yang bukan file)
   3. `ls -l`<br/>
       Digunakan untuk menampilkan format daftar yang panjang
   4. `ls -g`<br/>
       Sama seperti -l. tapi tidak menampilkan owner hanya grupnya
   5. `ls --author`<br/>
       Digunakan bersama -l, fungsinya buat menampilkan author setiap file
   6. `ls -R`<br/>
       Menampilkan subdirektori beserta file di dalamnya
   7. `ls -h` atau –human-readable <br/>
       Digunakan bersama perintah -l atau -s, fungsinya untuk menampilkan ukuran file yang dapat dimengerti oleh manusia
   8. `ls -o`<br/>
       Fungsinya sama seperti -l, tapi tidak menampilkan daftar informasi grup, hanya owner
   9. `ls -s` atau –size<br/>
       Digunakan bersama -l, menampilkan ukuran dari setiap file, ditampilkan menurut blok<br/>
  10. `ls -S`<br/>
      Mengurutkan berdasarkan ukuran file, yang berukuran besar ditampilkan lebih awal
  11. `ls -t`<br/>
       Mengurutkan berdasarkan waktu dimodifikasi, yang terbaru ditampilkan lebih awal
  12. `ls -r`<br/>
       Mengurutkan berdasarkan ukuran lebih kecil dulu

#### 2. mkdir
   mkdir merupakan perintah untuk membuat sebuah direktori/folder. Contoh `mkdir -v ubuntu` makan folder ubuntu akan terbuat, dapat dilihat pada gambar di bawah. fungsi -v (verbose) untuk menampilkan keterangan pembuatan folder.

    mkdir -v nama-direktori

  ![mkdir](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/94d75bcb-7980-4778-8fce-0ebc596bc036)

   Perintah lain dalam penggunaan perintah mkdir : 

   1. **Menampilkan Keterangan Pembuatan Folder**<br/>
       `mkdir -v/--verbose folder`<br/>
      contoh> ardi@PC:~/Documents/Folder$ `mkdir -v Ardi`<br/>
   2. **Membuat Folder Sekaligus Membuat Subfolder Di Dalamnya**<br/>
       `mkdir -p/--parents folder folder`<br/>
      contoh> ardi@PC:~/Documents/Folder$ `mkdir -p Ardi/Ardi`<br/>
   3. **Membuat Folder Sekaligus Membuat Subfolder Di Dalamnya Dengan Menampilkan Keterangan**<br/>
       `mkdir -vp folder/folder`<br/>
      contoh> ardi@PC:~/Documents/Folder$ `mkdir -vp Ardi/Dua`
   4. **Membuat Lebih Dari Satu Folder**<br/>
       `mkdir folder folder`<br/>
      contoh> ardi@PC:~/Documents/Folder$ `mkdir -v Ardi1 Ardi2 Ardi3`
   5. **Membuat Lebih Dari Satu Folder Sekaligus Membuat Subfolder Di Dalamnya**<br/>
       `mkdir -p folder/folder folder/folder`<br/>
      contoh> ardi@PC:~/Documents/Folder$ `mkdir -pv Ardi1/dalam1 Ardi2/dalam2`
   6. **Penggunaan Kurung Kurawal Dalam Pembuatan Folder**<br/>
       Membuat folder sekaligus dengan nama depan yang sama<br/>
       contoh> ardi@PC:~/Documents/Folder$ `mkdir -v Ardi{1,2,3}`

#### 3. rm
   Perintah rm digunakan untuk menghapus sebuah file atau direktori.<br/>

    rm nama-file
    rmdir nama-folder
  
  > ![rmdir](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/84026bdb-46f8-4ff7-a370-335aabaa9f58)<br/>
  > Contoh menghapus folder.<br/>

  >![rmfile](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6ff919ef-cb05-4966-a0fe-03619e3b227b)<br/>
  > Contoh Menghapus File.<br/>
   Ketika menghapus folder terdapat dua kondisi
   1. Folder kosong		: `rmdir nama folder`
   2. Folder ada isi		: `rm -r nama folder`

#### 4. touch
   Perintah touch digunakan untuk membuat suatu file kosong.

    touch nama-file

   ![touch](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3d3f8956-3c6c-40d5-8f12-629056111f87)
   
#### 5. cd
   Perintah cd digunakan untuk masuk ke dalam suatu direktori atau file di dalam linux. Perintah cd. Contoh `cd ubuntu/` akan mengantar pengguna menuju direktori/folder ubuntu.
   
    cd ..

   ![cd](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/46fe5339-907d-431b-b6d7-3349a14514c8)

   Adapun perintah lain dalam penggunaan perintah cd antara lain :
   1. `cd /` <br/>
      Berpindah ke direktori root
   2. `cd (tab 2x)`<br/>
      Menampilkan direktori/folder yang dimungkinakn untuk diakses
   3. `cd atau cd ~`<br/>
      Bila digunakan tanpa argumen maka akan kembali ke home user
   4. `cd .`<br/>
      Tidak ke mana mana
   5. `cd ..` atau `cd ../` <br/>
      Naik satu tingkat ke parent direktori (setingkat di atasnya)
   6. `cd ../../`<br/>
       Naik dua tingkat direktori di atasnya
   7. `cd -` <br/>
       Kembali ke direktori yang sebelumnya diakses
   8. `cd ../(nama folder)`<br/>
       Menuju parent direktori lalu masuk ke folder yang ada di parent direktori tersebut
   9. `cd ~/(nama direktori yang ada di home user)`<br/>
       Berpindah ke direktori yang ada di home user
   10. `cd ~(nama user)`<br/>
       Untuk berpindah langsung ke dalam direktori user yang dipilih

#### 6. cp

   Perintah cp digunakan untuk mengcopy/menduplikasi sebuah file atau direktori baik dalam satu direktori atau ke direktori lain.

    cp nama-file nama-file-baru
    
![cp](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/4d652fc6-d68a-4090-b777-37ef43bce0c0)

   Perintah untuk mengcopy file dan folder

   **1. Mengcopy/Menduplikasi File <br/>**
      cp file folder_tujuan
      contoh > ardi@PC:~/Downloads$ `cp file.html ~/Documents` <br/>
      File akan tercopy dari Downloads ke Documents dengan syntax harus jelas di mana direktori Documents berada, karena berada di home harus ditambah symbol ~
   **2. Mengcopy/Menduplikasi Folder<br/>**
      cp -r folder folder-tujuan
      contoh> ardi@PC:~/Downloads$ cp -r Test/ ~/Documents/<br/>
      Folder akan tercopy dari Downloads ke Document, jika masih dalam satu folder, tidak harus pakai symbol ~ (home), contoh jika folder Test ingin di pindah ke dalam folder yang ada di folder Downloads 

#### 7. mv
   Perintah mv digunakan untuk memindahkan file/direktori dari satu direktori ke direktori lain. mv juga dapat digunakan untuk melakukan rename suatu file.

    mv nama-file/folder-lama nama-file/folder-baru

>  ![mv rename](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/364faf1d-6a82-4ee1-a63c-0cdb44dad37b)
> Contoh rename file.<br/>

>  ![mv cut](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ace42147-b03b-4098-a390-186d6bcc0d73)
> Contoh pindah file.<br/>
   

