![17](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/7fad046a-9ed5-4f69-81e9-bd9a6a3d29da)# Install Ubuntu 
Berikut adalah langkah langkah bagaimana melakukan instalasi Ubuntu server menggunakan aplikasi virtual machine VMware. Silahkah download serta install tolls yang dibutuhkan yaitu VMware serta ISO Ubuntu server yang bisa didownload melalui website, pada saat dokumentasi ini dibuat, VMware yang digunakan adalah VMWare player versi 17 serta ISO ubuntu-22.04.3-live-server-amd64.

1. Langkah pertama silahkan buka VMware yang telah diinstal, selanjutnya langsung saja klik pada pilihan Create a New Vritual Machine.

  ![1](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/f0371b25-4f4b-40d3-8da0-0cb3f9be4742)

2. Jika sudah diklik nantinya akan muncul tab baru seperti di gambar, kemudian pilih pada bagian use ISO image karena kita akan melakukan instalasi menggunakan iso, kemudian browse lalu cari di mana tempat kita menaruh ISO ubuntu server yang telah didownload sebelumnya.

  ![4](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/c85d6501-f187-48b4-a633-2be00db5227a)

3. Selanjutnya pilih sistem operasi yang akan diinstall pada VMware, karena kita akan menginstall ubuntu server di mana termasuk dalam sistem opearasi linux, pilih linux kemudian next.

  ![5](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/8492cc6b-69b7-4eeb-b7d3-8e655b0131e8)

4. Kemudian pilih di mana instalan ubuntu server akan disimpan dengan klik browse, jika tidak ingin mengubah bisa langsung klik next.

  ![6](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/d5fd9fe1-71d7-4539-bced-e0a4189cb666)

5. Selanjutnya tentukan ukuran disk yang akan digunakan, pada kasus ini saya menggunakan peyimpanan sebesar 10GB dengan opsi Split Virtual Disk Into Multiple Files.

  ![7](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/b90c6a9f-442e-45d4-a3e2-8cf3b0cd6fca)


6. Setelah selesai menentukan ukuran disk, selanjutnya adalah kita melakukan setting custom hardware untuk server yang akan digunakan, klik Customize Hardware.

  ![8](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/2509e787-7bc7-4509-b3a3-b07adc555448)

7. Setelah muncul tab hardware, terdapat beberapa settingan yang dapat kita ubah, pada kasus ini kita cukup mengubah Memory, Processors, dan Network Adapter dengan ketentuan :
Memory : 2GB
Processors : 1 Core
Network Adapter : Bridge

  ![9](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/bc54d694-8b42-4341-b890-203eb5d96fd8)

8. Jika sudah, maka tampilan selanjutnya yang sudah kita setting akan seperti berikut. Keterangan dari hardware setting itu sendiri antara lain:
Memory : Penyimpanan yang akan 
Processors : 
Network Adapter : 

Adapun pada bagian Network Adapter penjelasannya yaitu : 

Jika kita menggunakan Network Adapter NAT, maka nantinya IP yang kita dapatkan akan sesuai dengan IP yang sudah disediakan oleh VMware itu sendiri.

Sedangkan jika kita menggunakan Network Adapter bridge, nantinya IP yang didapat akan sesuai dengan IP yang terdapat pada lokal device karena bridge ini sendir meneruskan jaringan untuk mendapatkan ip dari device jaringan lokal secara langsung.

  ![10](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/463ee649-0f19-4253-9159-82d4b935db8d)

9. Jika settingan sudah sesuai, klik finish

10. Kemudian pada tampilan selanjutnya akan muncul GNU GRUB, pilih Try or Install Ubuntu Server.

  ![11](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/24fc9f3f-446f-475b-93ca-5e40db9f7996)

11. Selanjutnya proses instalasi, tunggu hingga proses selesai.

  ![12](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/873c3da6-6d9e-4fad-b069-0562aa6b46e1)

12. Pada tampilan berikutnya pilih bahasa yang akan digunakan, pilih Bahasa inggris.

  ![13](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/42ad0b5f-7f94-45b7-bc11-d87f5b5330ba)

13. Selanjutnya muncul tampilan untuk disarankan melakukan update installer pada aplikasi atau paket yang terdapat update. Jika ingin melakukan update pilih Update to the new installer, namun kali ini untuk mempercepat waktu saya memilih skip dengan pilih Continue without saving.

  ![14](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/1dc9e83c-4570-422b-8d19-89ecf16c8cdf)

14. Kemudian akan tampil piliha untuk konfigurasi keyboard, sesuaikan dengan keyboard masing masing atau jika ingin menggunakan default, cukup pilih layout dan variant keyboard English (US).

  ![15](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/797ec4fb-ce89-41df-9a34-eafc6697ea74)

15. Kemudian pilih tipe instalasi yang diinginkan, cukup pilih Ubuntu Server kemudian done.

  ![16](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/efd17db0-a7ab-4e67-b577-cf5414f0c301)

16. Selanjutnya kita akan melakukan setting jaringan di mana secara default, linux akan menggunakan IP DHCP, agar mempermudah dalam mengakses Ubuntu Server baiknya kita ubah menggunakan IP Static, pada bagian ens33 eth, tekan spasi kemudian pilih Edit IPv4.

  ![17](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/7cc69c8a-9b50-4bd9-aa02-a5df80ab9fb3)

17. Selanjutnya Pilih Manual

  ![18](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/8d166af8-b8ac-4965-aeb2-680cdbe3302f)

18. Isikan pada bagian subnet dengan IP Network diikuti oleh subnet/prefix, Adress sesuai dengan IP yang didapatkan DHCP sebelumny, Gateway sesuai dengan IP dari router serta name servers bisa menggunakan DNS google. 

  ![21](https://github.com/ardi2105/Dumbways-Task-Devops19/assets/151701736/7a56a8d2-0b5a-4ef0-b570-64c1085e8c1b)

