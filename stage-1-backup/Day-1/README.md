# DEVOPS-BATCH-19
##### Daily Task - Day 1 - Ardi Solehuddin

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

  ![1](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/f0371b25-4f4b-40d3-8da0-0cb3f9be4742)

2. Jika sudah diklik nantinya akan muncul tab baru seperti di gambar, kemudian pilih pada bagian **use ISO image** karena kita akan melakukan instalasi menggunakan iso, kemudian browse lalu cari di mana tempat kita menaruh ISO ubuntu server yang telah didownload sebelumnya.

  ![4](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/c85d6501-f187-48b4-a633-2be00db5227a)

3. Selanjutnya pilih sistem operasi yang akan diinstall pada VMware, karena kita akan menginstall ubuntu server di mana termasuk dalam sistem operasi linux, pilih linux kemudian next.

  ![5](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/8492cc6b-69b7-4eeb-b7d3-8e655b0131e8)

4. Kemudian pilih di mana instalan ubuntu server akan disimpan dengan klik browse, jika tidak ingin mengubah bisa langsung klik next.

  ![6](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/d5fd9fe1-71d7-4539-bced-e0a4189cb666)

5. Selanjutnya tentukan ukuran disk yang akan digunakan, pada kasus ini saya menggunakan peyimpanan sebesar 10GB dengan opsi **Split Virtual Disk Into Multiple Files.**

  ![7](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/b90c6a9f-442e-45d4-a3e2-8cf3b0cd6fca)


6. Setelah selesai menentukan ukuran disk, selanjutnya adalah kita melakukan setting custom hardware untuk server yang akan digunakan, klik **Customize Hardware**.

  ![8](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/2509e787-7bc7-4509-b3a3-b07adc555448)

7. Setelah muncul tab hardware, terdapat beberapa settingan yang dapat kita ubah, pada kasus ini kita cukup mengubah Memory, Processors, dan Network Adapter dengan ketentuan :

   **Memory : 2GB**
    
   **Processors : 1 Core**
    
   **Network Adapter : Bridge**

  ![9](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/bc54d694-8b42-4341-b890-203eb5d96fd8)

8. Jika sudah, maka tampilan selanjutnya yang sudah kita setting akan seperti berikut. Keterangan dari hardware setting itu sendiri antara lain:

   **Memory** : Berfungsi enyimpanan atau memory yang akan akan digunakan oleh Virtual Machine

   **Processors** : Fungsi dari Processors pada virtual machine adalah untuk melakukan proses data serta kontrol sistem. 

   **Network Adapter** : Berfungsi agar virtual machine dapat terhubungan ke internet atau jaringan 

   Adapun pada bagian Network Adapter penjelasannya yaitu : 

   Jika kita menggunakan **Network Adapter NAT**, maka nantinya IP yang kita dapatkan akan sesuai dengan IP yang sudah disediakan oleh VMware itu sendiri.

   Sedangkan jika kita menggunakan **Network Adapter bridge**, nantinya IP yang didapat akan sesuai dengan IP yang terdapat pada lokal device karena bridge ini sendiri meneruskan jaringan untuk mendapatkan ip dari device jaringan secara langsung.

  ![10](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/463ee649-0f19-4253-9159-82d4b935db8d)

9. Jika settingan sudah sesuai, klik finish

10. Kemudian pada tampilan selanjutnya akan muncul GNU GRUB, pilih **Try or Install Ubuntu Server.**

  ![11](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/24fc9f3f-446f-475b-93ca-5e40db9f7996)

11. Selanjutnya proses instalasi, tunggu hingga proses selesai.

  ![12](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/873c3da6-6d9e-4fad-b069-0562aa6b46e1)

12. Pada tampilan berikutnya pilih bahasa yang akan digunakan, pilih **English**.

  ![13](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/42ad0b5f-7f94-45b7-bc11-d87f5b5330ba)

13. Selanjutnya muncul tampilan untuk disarankan melakukan update installer pada aplikasi atau paket yang terdapat update. Jika ingin melakukan update pilih **Update to the new installer**, namun kali ini untuk mempercepat waktu saya memilih skip dengan pilih **Continue without saving**.

  ![14](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/1dc9e83c-4570-422b-8d19-89ecf16c8cdf)

14. Kemudian akan tampil pilihan untuk konfigurasi keyboard, sesuaikan dengan keyboard masing masing atau jika ingin menggunakan default, cukup pilih layout dan variant keyboard **English (US).**

  ![15](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/797ec4fb-ce89-41df-9a34-eafc6697ea74)

15. Kemudian pilih tipe instalasi yang diinginkan, cukup pilih Ubuntu Server kemudian done.

  ![16](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/efd17db0-a7ab-4e67-b577-cf5414f0c301)

16. Selanjutnya kita akan melakukan setting jaringan di mana secara default, linux akan menggunakan **IP DHCP** dimana bersifat tidak tetap yaitu IP yang didapat dari server jaringan dapat berubah sesuai dengan jangka waktu **DHCP Lease**, maka dari itu agar mempermudah dalam mengakses Ubuntu Server baiknya kita ubah menggunakan **IP Static** di mana IP Ini akan selalu sama sesuai dengan ip yang didaftarkan. Pada bagian **ens33 eth**, tekan spasi kemudian pilih **Edit IPv4.**

  ![17](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/7cc69c8a-9b50-4bd9-aa02-a5df80ab9fb3)

17. Selanjutnya Pilih Manual

  ![18](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/8d166af8-b8ac-4965-aeb2-680cdbe3302f)

18. Isikan pada bagian subnet dengan IP Network diikuti oleh subnet/prefix, Adress sesuai dengan IP yang didapatkan DHCP sebelumnya (bisa dilihat pada tanda panah), Gateway sesuai dengan IP dari router (gateway pada umumnya menggunakan ip paling pertama) serta name servers bisa menggunakan DNS google yaitu 8.8.8.8. 

  ![21](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3a587e2c-b95e-418e-a9af-34a86a278028)
  ![22](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/538251b4-e1fb-4f88-8a96-9ed36db2f684)

Jika sudah, dapat dilihat settingan DCHP sudah berubah menjadi static.

19. Pada bagian proxy address dan mirror address dapat diskip.
  ![23](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/eca6597a-31fd-4a43-bb5a-7cd87bd1a4bc)
  ![24](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/f70c82c6-bd15-4f45-a39f-49dce49f13d7)

20. Pada menu **guided storage configuration**, pilih **custome storage layout** untuk membuat dua buah partisi.

  ![25](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/7f67e08e-ff58-41f7-b2ff-8c8c08b0f6aa)

21. Selanjutnya muncul tampilan seperti berikut, pada menu setting pada available devices, pilih **free spaces** lalu **add GPT partition.** 

  ![26](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/5af196db-9210-44ba-adce-f50b6e678bfa)

22. Buat dua partisi untuk penyimpanan *ROOT* atau penyimpanan utama untuk menyimpan instalasi sistem serta penyimpanan *SWAP* untuk penyimpanan cadangan. Isi pada bagian SWAP cukup 1GB dan sisanya yaitu 8.997G untuk penyimpanan ROOT. 
  
  ![27](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/97165e19-27ed-4361-be24-906ad8cadbcf)
  ![root](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/6289bd77-9087-4c45-9e4e-809874ffc611)
  ![28](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/a7836d5d-0ad5-470a-928a-294614de6edd)

23. Jika sudah bisa dilihat hasilnya dan lanjut klik done lalu continue.

  ![29](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/216703d2-3084-405a-be5a-d325a579af3a)

24. Pada tampilan selanjutnya pengaturan profile, isi sesuai dengan nama serta password yang diinginkan, jika sudah klik done.

  ![30](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/fb32854e-b195-4a6b-8895-c4563318e378)

25. Skip pada bagian upgrade to pro karena kita belum membutuhkannya. 

  ![31](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/7e6651d5-9145-4048-a089-18b3b056cef6)

26. Selanjutnya SSH Setup, enable pada bagian **install OpenSSH Server** agar server ubuntu dapat diremote.

  ![32](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b61b1490-b6f6-4015-8a57-172e24b45333)

27. Skip pada bagian **featured server snaps**, klik done

  ![33](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/7a0c2e55-42f1-4a86-8f28-fa02aca5f4fb)

28. Tunggu hingga proses instalasi selesai, jika sudah langsung saja klik **Reboot Now**

  ![35](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ac2fbb8f-6157-4a17-b179-fd48a544cbd8)

29. Jika sudah reboot, maka akan langsung diarahkan ke login ubuntu, masukan username dan password yang telah dibuat sebelumnya, jika berhasil maka tampilan berikutnya akan seperti berikut.

  ![36](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b8ac8b60-328a-47f1-a97e-ebc7422b1850)

30. Selanjutnya lakukan pengecekan apakah server dapat terhubung ke internet dengan melakukan ping ke google.

  ![37](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/25184a42-6afe-43bf-9a19-34c4e31d70e3)

31. Lakukan juga pengecekan apakah server ubuntu bisa diremote menggunakan SSH dengan terminal linux kita dengan perintah (ssh *(username@ipaddressserver)*). Jika terdapat pertanyaan *Are you sure you want to continue connecting* ketik yes, jika berhasil maka username kita akan berubah seperti pada gambar yang sebelumnya **ardi@pc** menjadi **ardi@ubuntu**. 

  ![40](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/d87b9b19-fb4b-4fb8-9e34-2d988b015ff0)


Proses dalam melakukan instalasi server ubuntu sudah selesai.
