# DEVOPS-BATCH-19
##### Daily Task - Day 1 - Ardi Solehuddin

-  Fundamental Devops
-  Step by step instalasi ubuntu server

## Devops Fundamental
DevOps merupakan gabungan dari **Development** dan **Operations** di mana ini adalah suatu prinsip yang digunakan untuk memudahkan dalam pengembangan suatu aplikasi karena semua prosesnya dapat terintegrasi dengan bantuan tools-tools yang tersedia dalam mencapai efektifitas serta efesiensi dalam perencanaan, pembangunan, pengembangan serta pengoperasian suatu aplikasi.

Adapun tujuan dari adanya DevOps ini adalah :
1. Untuk meningkatkan frekuensi deployment
2. Mengurangi kemungkinan gagal pada perilisan terbaru
3. Mengurangi waktu perbaikan ketika terdapat trouble

Terdapat 8 tahapan yang umum dalam proses DevOps antara lain **plan, code, build, test, release, deploy, operate,** dan **monitor**.

Salah satu yang dibutuhkan oleh seorang Devops adalah kemampuan mengoperasikan linux, selanjutanya adalah apa saja yang dibutuhkan untuk melakukan instalasi linux serta langkah-langkah dalam melakukan instalasi linux menggunakan aplikasi **Virtual Machine VMware**.

## Install Ubuntu Requirements
Sebelum melakukan instalasi silahkah download serta install tools yang dibutuhkan yaitu [VMware Workstation Player](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html) serta [ISO Ubuntu-Server](https://ubuntu.com/download/server) yang bisa didownload melalui website. Pada saat dokumentasi ini dibuat, VMware yang digunakan adalah VMWare player versi 17 serta ISO ubuntu-22.04.3-live-server-amd64.

## Install Ubuntu Server
Berikut adalah langkah langkah bagaimana melakukan instalasi Ubuntu server menggunakan aplikasi virtual machine VMware Workstation Player. 

1. Langkah pertama silahkan buka VMware yang telah diinstal, selanjutnya langsung saja klik pada pilihan **Create a New Vritual Machine**.

  ![1](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9f3fc9ac-bba5-4016-9d26-cfbbf7d11a5e)

2. Jika sudah diklik nantinya akan muncul tab baru seperti di gambar, kemudian pilih pada bagian **use ISO image** karena kita akan melakukan instalasi menggunakan iso, kemudian browse lalu cari di mana tempat kita menaruh ISO ubuntu server yang telah didownload sebelumnya.

  ![4](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3fbc4764-41a0-4d68-a088-be3c19742f23)

3. Selanjutnya pilih sistem operasi yang akan diinstall pada VMware, karena kita akan menginstall ubuntu server di mana termasuk dalam sistem operasi linux, pilih linux kemudian next.

  ![5](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/2686c57c-483b-4048-b1a8-995ab95d44ed)

4. Kemudian pilih di mana instalan ubuntu server akan disimpan dengan klik browse, jika tidak ingin mengubah bisa langsung klik next.

  ![6](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/4e12b70d-f427-4132-8232-55114fe29629)

5. Selanjutnya tentukan ukuran disk yang akan digunakan, pada kasus ini saya menggunakan peyimpanan sebesar 10GB dengan opsi **Split Virtual Disk Into Multiple Files.**

 ![7](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b3c6f1b1-3267-4ad8-97fc-40472617e8c5)

6. Setelah selesai menentukan ukuran disk, selanjutnya adalah kita melakukan setting custom hardware untuk server yang akan digunakan, klik **Customize Hardware**.

  ![8](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/a971d1e3-3474-4cee-a18e-df35a2f46d23)

7. Setelah muncul tab hardware, terdapat beberapa settingan yang dapat kita ubah, pada kasus ini kita cukup mengubah Memory, Processors, dan Network Adapter dengan ketentuan :

   **Memory : 2GB**
    
   **Processors : 1 Core**
    
   **Network Adapter : Bridge**

  ![9](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ff2457b3-cfd8-4917-b845-624a36ebabac)

8. Jika sudah, maka tampilan selanjutnya yang sudah kita setting akan seperti berikut. Keterangan dari hardware setting itu sendiri antara lain:

   **Memory** : Berfungsi enyimpanan atau memory yang akan akan digunakan oleh Virtual Machine

   **Processors** : Fungsi dari Processors pada virtual machine adalah untuk melakukan proses data serta kontrol sistem. 

   **Network Adapter** : Berfungsi agar virtual machine dapat terhubungan ke internet atau jaringan 

   Adapun pada bagian Network Adapter penjelasannya yaitu : 

   Jika kita menggunakan **Network Adapter NAT**, maka nantinya IP yang kita dapatkan akan sesuai dengan IP yang sudah disediakan oleh VMware itu sendiri.

   Sedangkan jika kita menggunakan **Network Adapter bridge**, nantinya IP yang didapat akan sesuai dengan IP yang terdapat pada lokal device karena bridge ini sendiri meneruskan jaringan untuk mendapatkan ip dari device jaringan secara langsung.

  ![10](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9f930b3a-80bb-4a25-83e3-e83427c3c83b)

9. Jika settingan sudah sesuai, klik finish

10. Kemudian pada tampilan selanjutnya akan muncul GNU GRUB, pilih **Try or Install Ubuntu Server.**

  ![11](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/deee63b9-2a71-4014-aa4d-02aba9f0d00b)

11. Selanjutnya proses instalasi, tunggu hingga proses selesai.

  ![12](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/5bf07d4e-45fb-48c3-9a38-e70d4ec91138)

12. Pada tampilan berikutnya pilih bahasa yang akan digunakan, pilih **English**.

  ![13](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6cb3f741-5917-4deb-9f22-bf177b4b5fcc)

13. Selanjutnya muncul tampilan untuk disarankan melakukan update installer pada aplikasi atau paket yang terdapat update. Jika ingin melakukan update pilih **Update to the new installer**, namun kali ini untuk mempercepat waktu saya memilih skip dengan pilih **Continue without saving**.

  ![14](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/dd6f71dd-c274-4450-a788-1fb4b243db8b)

14. Kemudian akan tampil pilihan untuk konfigurasi keyboard, sesuaikan dengan keyboard masing masing atau jika ingin menggunakan default, cukup pilih layout dan variant keyboard **English (US).**

  ![15](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/d6ace8aa-c4cd-4646-88da-26a671539bd0)

15. Kemudian pilih tipe instalasi yang diinginkan, cukup pilih Ubuntu Server kemudian done.

  ![16](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6fb9586f-e94e-4358-9126-18a60776031b)

16. Selanjutnya kita akan melakukan setting jaringan di mana secara default, linux akan menggunakan **IP DHCP** dimana bersifat tidak tetap yaitu IP yang didapat dari server jaringan dapat berubah sesuai dengan jangka waktu **DHCP Lease**, maka dari itu agar mempermudah dalam mengakses Ubuntu Server baiknya kita ubah menggunakan **IP Static** di mana IP Ini akan selalu sama sesuai dengan ip yang didaftarkan. Pada bagian **ens33 eth**, tekan spasi kemudian pilih **Edit IPv4.**

  ![17](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/8c0a7878-c47e-44e2-84f1-f7a9af601539)

17. Selanjutnya Pilih Manual

  ![18](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/0a48e1fb-54b1-4d65-a108-b74336538c94)

18. Isikan pada bagian subnet dengan IP Network diikuti oleh subnet/prefix, Adress sesuai dengan IP yang didapatkan DHCP sebelumnya (bisa dilihat pada tanda panah), Gateway sesuai dengan IP dari router (gateway pada umumnya menggunakan ip paling pertama) serta name servers bisa menggunakan DNS google yaitu 8.8.8.8. 

  ![21](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/1132d061-2b1d-47bb-8f2b-23a559ffa896)
  ![22](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/8911d0b8-5170-4974-964e-5037607a7422)

Jika sudah, dapat dilihat settingan DCHP sudah berubah menjadi static.

19. Pada bagian proxy address dan mirror address dapat diskip.
  
  ![23](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/49d7441f-9ff9-4b1a-9376-11ccc3b3eb83)
  ![24](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/1b6c13bd-e7e8-4efd-92c4-2dd2baf03a9f)

20. Pada menu **guided storage configuration**, pilih **custome storage layout** untuk membuat dua buah partisi.

  ![25](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/922125ab-dce3-4922-a485-4b67abcffed3)

21. Selanjutnya muncul tampilan seperti berikut, pada menu setting pada available devices, pilih **free spaces** lalu **add GPT partition.** 

  ![26](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/118fb451-5b68-4519-9d08-e01f2a5297bb)

22. Buat dua partisi untuk penyimpanan *ROOT* atau penyimpanan utama untuk menyimpan instalasi sistem serta penyimpanan *SWAP* untuk penyimpanan cadangan. Isi pada bagian SWAP cukup 1GB dan sisanya yaitu 8.997G untuk penyimpanan ROOT. 
  
  ![27](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/32e640f6-fb4d-41fe-a781-a583a2e5b65f)
  ![root](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/465e6339-71dd-40b7-bc98-45be6786aa17)
  ![28](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3f848bc1-9089-434f-8caf-ec5846f1ae8f)

23. Jika sudah bisa dilihat hasilnya dan lanjut klik done lalu continue.

  ![29](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/741f70b1-b79a-4ce1-b828-6e148e1438b7)

24. Pada tampilan selanjutnya pengaturan profile, isi sesuai dengan nama serta password yang diinginkan, jika sudah klik done.

  ![30](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ba86105e-3565-4194-92f2-63bc8e6a2553)

25. Skip pada bagian upgrade to pro karena kita belum membutuhkannya. 

  ![31](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/0b5d50a6-a4a2-43c0-b305-317cdb879300)

26. Selanjutnya SSH Setup, enable pada bagian **install OpenSSH Server** agar server ubuntu dapat diremote.

  ![32](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ff40c06e-1278-44a5-b6b0-da758179bb1e)

27. Skip pada bagian **featured server snaps**, klik done

  ![33](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/e22811a1-585f-45d5-8d50-e43e97175b6a)

28. Tunggu hingga proses instalasi selesai, jika sudah langsung saja klik **Reboot Now**

  ![35](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/2b2e26a5-588c-42b6-9e86-ca40298f2154)

29. Jika sudah reboot, maka akan langsung diarahkan ke login ubuntu, masukan username dan password yang telah dibuat sebelumnya, jika berhasil maka tampilan berikutnya akan seperti berikut.

  ![36](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b6a9e022-e1fb-4ee2-a07e-585e73f866bc)

30. Selanjutnya lakukan pengecekan apakah server dapat terhubung ke internet dengan melakukan ping ke google.

  ![37](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/22220cc4-6501-4952-ae09-55c09ba528f6)

31. Lakukan juga pengecekan apakah server ubuntu bisa diremote menggunakan SSH dengan terminal linux kita dengan perintah (ssh *(username@ipaddressserver)*). Jika terdapat pertanyaan *Are you sure you want to continue connecting* ketik yes, jika berhasil maka username kita akan berubah seperti pada gambar yang sebelumnya **ardi@pc** menjadi **ardi@ubuntu**. 

  ![40](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/f8c5dffa-1762-4ac2-9aa1-77a35143be17)

Proses dalam melakukan instalasi server ubuntu sudah selesai.
