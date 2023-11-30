# DEVOPS-BATCH-19
##### Daily Task - Day 4 - Ardi Solehuddin

-  Jelaskan Apa Itu Teks Editor (Docs Shortcut)
-  Manipulation Teks (Docs Manipulation Teks)
-  Penjelasan Apa Itu Firewall, Fungsi Firewall, Kegunaan Firewall (Docs UFW)

## Teks Editor
Teks Editor adalah suatu program yang biasa digunakan untuk melakukan suatu editing file teks. Pada sistem operasi linux text editor ini berjalan di atas terminal dan biasa digunakan oleh server yang berbasis CLI.

### Jenis Jenis Teks Editor Linux
- **Nano<br/>**
  Teks editor nano berbasis konsol merupakan yang paling umum bagi pengguna linux, biasanya teks editor ini digunakan oleh pemula yang baru menggunakan linux karena penggunaannya yang cukup mudah. Penggunaannya cukup ketikan `nano (nama_file)` pada terminal linux.
- **VIM<br/>**
  Sama seperti nano yang merupakan teks editor berbasis VIM, pengguna untuk VIM ini lebih banyak digunakan oleh para sysadmin atau seorang yang sudah mahir karena penggunaan VIM yang cukup rumit. Penggunannya sama seperti nano cukup ketik `vim (nama_file)` pada terminal linux.
- **Emacs<br/>**
  Emac juga merupakan teks editor berbasis konsol yang memiliki keunggulan tersendiri. Emacs dapat dikombinasikan dengan macros untuk keperluan automasi. Untuk mengakses atau menggunakan emacs cukup ketikan `emacs` pada terminal, jika belum ada dapat diinstall dengan perinta `sudo apt install emacs`
- **Gedit<br/>**
  Pada Linux Dekstop GNOME, gedit merupakan teks editor berbasis GUI yang tampilannya mirip seperti notepad di windows sehingga lebih mudah untuk digunakan dibanding dengan teks editor sebelumnya yang berbasis konsol. Akses gedit menggunakan perintah `gedit (nama_file)`.
- **Geany<br/>**
  Selain Gedit yang merupakan teks editor berbasis GUI, terdapat juga geany yaitu editor yang berbasis GTK+ Toolkit yang penggunaan cocok untuk seorang programmer atau developer. Geany dapat digunakan dengan perintah `geany (nama_file)`.

### Nano
Pada pembahasan kali ini akan menjelaskan beberapa shortcut yang digunakan pada editor nano. 
#### 1. Membuka nano
Untuk membuka nano cukup ketik `nano` pada terminal jika ingin membuat file baru atau dengan mengetikan `nano (diikuti nama file)` jika ingin membuka suatu file.

   ![nano](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b4cf6884-5d00-4741-ba66-d6889629fc24)

   ![nano-editor](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e31e6ddc-7985-4ea1-87e5-4a6dbbdfeb56)

#### 2. Membuka Petunjuk penggunaan nano
Untuk melihat guide atau petunjuk penggunaan nano bisa menggunakan kombinasi `ctrl+g`.

   ![ctrl+g](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/81be1b7f-3ce7-4c24-a2c4-d15ed428fd30)

#### 3. Membuka file dari dalam nano
Untuk membuka file ketika sudah membuka nano bisa menggunakan kombinasi `ctrl+r` diikuti dengan kombinasi `ctrl+t` untuk melihat file yang ingin dibuka yang terdapat pada direktori.

   ![ctrl+r](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6198295f-f48d-4dd4-9dd1-67a10022351d)

   ![ctrl+t](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/91e22cf6-d24e-4b52-a967-d869795555c1)
 
#### 4. Melakukan Seleksi text
Untuk memilih suatu baris atau melakukan seleksi teks menggunakan kombinasi `alt+a` lalu arahkan kursor sesuai teks yang ingin diseleksi. Fungsi bisa digunakan bersamaan dengan fungsi lain seperti melakukan copy/cut dan paste, 

   ![ctrl+a](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/8e16908c-e212-4684-80e3-bc79dd94162f)

#### 5. Melakukan Copy & Paste
Untuk melakukan copy dapat menggunakan kombinasi `alt+6` pada teks yang telah diseleksi sebelumnya menggunakan perintah `alt+a`, selanjutnya untuk melakukan paste dapat menggunakan `ctrl+u`

   ![alt+6](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/a1b8c501-076b-4ab3-87ec-2e2335d24bfb)

   ![ctrl+u](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/7e773df1-b2d4-43f0-b9b3-72a054478482)

#### 6. Melakukan Cut & Paste
Cut & Paste dapat dilakukan dengan kombinasi `ctrl+k` untuk melakukan cut atau memotong teks yang telah diseleksi kemudia `ctrl+u` untuk paste teks yang telah dicut.

   ![ctrl+k](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/49a9cf32-332d-4bf3-89a4-2d1316dfcdee)

   ![ctrl+u cut](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ed2655d7-d2d6-4e16-aa1a-592d14396f2a)

#### 7. Melakukan Undo & Redo
Untuk melakukan undo pada teks editor nano dapat menggunakan kombinasi `alt+u` sedangkan redo menggunakan kombinasi `alt+e`

#### 8. Keluar dari Nano
Untuk keluar dari teks editor nano dapat menggunakan kombinasi `ctrl+x`, jika tidak ada perubahan di dalam isi nano maka nano akan langsung keluar, namun jika terdapat perubahan yang dibuat pada nano maka akan menampilan Save moidified buffer, jika ingin menyimpan perubahan setelah kombinasi `ctrl+x` dilanjut dengan ketik *y* atau *n* jika tidak ingin menyimpan. 

   ![ctrl+x](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/87bbfd6f-13b0-4f16-91d1-25415e6a41b2)
   
## Teks Manipulation

## Firewall
