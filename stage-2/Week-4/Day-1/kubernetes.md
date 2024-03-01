##  Membuat Cluster Menggunakan Kubernetes

### Kubernetes
Kubernetes adalah platform open-source yang digunakan untuk otomatisasi, penyebaran, skalabilitas, dan operasi aplikasi kontainer di lingkungan yang luas. Dikembangkan oleh Google dan dirilis pada tahun 2014, Kubernetes telah menjadi salah satu alat utama dalam manajemen kontainer dalam infrastruktur modern. Kubernetes menyediakan fleksibilitas yang tinggi dan kemampuan otomatisasi yang kuat untuk menjalankan, mengelola, dan mengelola aplikasi dalam skala besar. Dengan fitur-fitur seperti penyebaran rolling, otomatisasi skalabilitas, deteksi kegagalan, dan manajemen konfigurasi yang terintegrasi, Kubernetes telah menjadi standar industri untuk orkestrasi kontainer dan manajemen aplikasi di lingkungan cloud dan on-premises.

### Langkah Pengerjaan
Berikut adalah dokumentasi langkah langkah bagaimana membuat suatu cluster dengan kubernets, melakukan uninstall ingress traefik, install ingress serta melakukan deploy aplikasi.

- Membuat sebuah cluster menggunakan k3s yang berisikan 2 node as a master and worker.
- Install ingress nginx using manifest
- Deploy aplikasi nginx lalu membuat suatu ingress yang mengarah ke aplikasi nginx.
- Setup persistent volume on k3s config
- Deploy aplikasi mongodb database on top kubernetes, menggunakan statefull.set dan juga pasangkan pvc ke dalamnya
- Membuat database di mongodb dan isi dummy data

1. Pertama buat sebuah node atau server yang masing masing berperan sebagai master dan worker/slave
![Alt text](images/cluster-kubernets.png) 

1. Unistal atau disable ingress traefik bawaan kubernets dengan membuat file config.yaml di didirectory `/etc/rancher/k3s# pwd` yang akan secara otomats berjalan melakukan disable traefik.
![Alt text](images/disable-traefik.png) 

1. Melakukan install ingress nginx dengan membuat script ingress-nginx.yaml pada directory `/var/lib/rancher/k3s/server/manifests` yang akan secara otomatis juga melakukan install
![Alt text](images/install-ingress-nginx.png) 

1. Lakukan remote kubernetes agar dapat membuat script atau melakukan konfigurasi melalui local dengan membuat directory `.kube` dan memasukan isi file config kubernetes yang berada pada direktori `/etc/rancher/k3s/k3s.yaml` yang kemudia ubah localhost menjadi server kubernets yang akan diremote. 
![Alt text](images/remote-kubernets.png) 

1. Melakukan instalasi nginx menggunakan vscode
![Alt text](images/install-nginx.png) 
![Alt text](images/install-nginx-1.png) 

1. Melakukan installasi mongodb menggunakan vscode
![Alt text](images/install-mongodb.png) 
![Alt text](images/install-mongodb-1.png) 

1. Dapat dilihat bahwa mongodb sudah berhasil berjalan pada kubernetes.
![Alt text](images/mongodb-created.png)