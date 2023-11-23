# DEVOPS-BATCH-19
##### Daily Task - Day 2 - Ardi Solehuddin
-   Penjelasan Basic Network, IP Private & IP Public, dan IP Static & IP Dinamis(DHCP).
-   Apa itu linux Shell? (docs command line)

## Computer Networking
Jaringan komputer adalah terhubungnya 2 komputer atau lebih sehingga komputer tersebut bisa saling terhubung, bertukar informasi & data serta bisa berbagi sumber daya atau resource satu sama lain. Jaringan komputer dapat terhubung baik melalui kabel ataupun tanpa kabel (*wireless*)  
### IP Address
IP Address (Internet Protocol Address) adalah alamat komputer yang terdapat dalam jaringan agar dapat terhubung dengan komputer lain sehingga bisa berbagi data atau informasi. IP Address dapat diibaratkan sebagai alamat rumah di mana dibutuhkan ketika terdapat seseorang yang ingin mengirim suatu paket.  

#### IP Private & IP Public
IP Address terbagi menjadi dua jenis yaitu IP Pivate dengan IP  Public yang masing-masing memiliki perbedaan, antara lain :  
- IP Private adalah IP Address yang hanya bisa digunakan secara lokal, sering digunakan dalam jaringan LAN di mana komputer yang terhubung dan memiliki IP dapat saling berkomunikasi, namun tidak dapat untuk terhubung ke jaringan di luar LAN tersebut, contohnya tidak dapat terhubung ke internet.
- IP Public adalah IP Address yang umumnya diberikan oleh Internet Service Provider (Penyedia Jasa Internet) di mana IP ini digunakan untuk dapat terhubung ke jaringan yang lebih luas yang cakupannya seluruh dunia. Dengan memiliki IP public, suatu komputer bisa terhubung ke jaringan yang lebih luas melalui internet.

#### IP Dinamis (DHCP) & IP DHCP
Terdapat dua cara dalam pembagian alamat IP ke komputer yaitu secara dinamis dan statis, perbedaannya adalah :
- IP Dinamis (DHCP = Dynamic Host Control Protocol) di mana IP yang diberikan kepada komputer berubah ubah sesuai dengan IP Pool yang dimiliki oleh suatu server jaringan. Jangka waktu yang diberikan paling umum adalah 3 hari, jadi ketika waktu peminjaman (*lease*) IP Address sudah habis maka IP yang diberikan ke komputer akan berubah.
- IP Static adalah IP yang diberikan ke komputer secara manual di mana pengguna harus memasukan IP yang tersedia di server jaringan. IP yang di daftarkan haruslah tersedia, tidak boleh sudah digunakan oleh pengguna lain atau akan menyebabkan bentrok/*ip conflict*.

## Linux Shell
Linux Shell merupakan alat atau program berbasis text/*Command Line Interface(CLI)* yang digunakan oleh seorang pengguna untuk mengoperasikan sistem operasi pada komputer terutama pada sistem operasi berbasis unix/linux. Sangat penting memahami untuk bisa melakukan konfigurasi atua manajemen pada server yang menggunakan CLI. 

Pada dokumentasi ini akan berhubungan dengan bagaimana cara menggunakan perintah-perintah dasar Linux shell serta bagaimana cara melihat serta setting IP di linux menggunakan terminal. 
 
## Perintah Perintah Pada Linux
Pada saat membuka terminal pada linux terdapat beberapa hal yang perlu diketahui seperti yang terdapat pada gambar di bawah. 

![Pengetahuan Dasar](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/530ed37b-c07a-4807-bdc6-21e8b8746022)

1. username : Tulisan di awal sebelum tanda @
2. Hostname/computer name : Tulisan setelah tanda @
3. Directory location : Tulisan setelah hostname
4. User biasa $ : Tulisan setelah directory location (bila tidak login sebagai root
5. Login sebagai root : ketik `su` atau `sudo su`
6. Root user (#) : Tulisan setelah directory location (bila login sebagai root)
7. Logout dari root user : `exit`

#### 1. ls
   Perintah ls atau list digunakan untuk melihat file atau direktori ketika berada di dalam suatu direktori, contoh

    ls -la

   ![ls -la](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e509486b-dbb2-4f95-a568-94dc0433505e)

   Perintah ls dapat digabungkan dengan perintah lanjutan untuk melihat list lebih detail.
