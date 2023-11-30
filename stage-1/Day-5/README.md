# DEVOPS-BATCH-19
##### Daily Task - Day 5 - Ardi Solehuddin

- Jelaskan apa itu aplikasi menurut kamu
- buatlah simple application dengan menggunakan bahasa berikut ini:
  - Go
  - Python3
  - NodeJS
- Challenge, research tentang penggunaan pm2 & implementasikan ke simple application kalian

## Aplikasi
Aplikasi adalah sebuah program atau perangkat lunak komputer yang digunakan oleh pengguna untuk melakukan suatu pekerjaan atau proses. 
## Simple Application

### Node.JS
Node.js adalah runtime environment untuk JavaScript yang bersifat open-source dan cross-platform. Dengan Node.js kita dapat menjalankan kode JavaScript di mana pun, tidak hanya terbatas pada lingkungan browser.

#### 1. Instalasi Node.JS
Instalasi node.js bisa menggunakan `curl` atau `wget` untuk melakukan download nvm (Node Version Manager) yang digunakan agar pengguna bisa menggunakan lebih dari satu versi Node.js tanpa harus menghapus versi sebelumnya.

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

   ![install nvm](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/dbb7178f-21ab-4878-a39d-8caecebf8cb2)

#### 2. Install versi nvm
install nvm versi 18 dengan perintah 

    nvm install 18

Untuk menggunakan nvm versi 18 gunakan perintah 

    nvm use 18

Periksa versi node dan npm dengan perintah

    node -v
    npm -v

   ![nvm install](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/943dd44b-21b0-4e80-b1c4-96335f7f6647)

Jika sudah tampil semua versi dari node dan npm berarti instalasi nodeJS telah berhasil.

#### 3. Inisiasi project
Masukan printah npm init untuk menginisiasi project, ketika ini dijalankan akan terdapat file baru bernama package.json di mana file ini nantinya akan berisi informasi apa package yang digunakan oleh aplikasi yang dibuat.

    npm init -y

   ![node init](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9c517fc7-43af-4999-b46b-7703667d8361)

#### 4. Install Framework Express.JS
**Express.JS** merupakan salah satu framework dari **NodeJS** yang dapat membantu dalam pengembangan aplikasi back end. Nantinya informasi tentang framework express.js ini akan secara otomatis muncul di **package.json** yang dibuat pada inisiasi sebelumnya, sehingga ketika pengguna lain ingin menggunakan aplikasi, mereka tinggal melakukan download package manager yang dibutuhkan yang informasinya terdapat pada package.json. Untuk instalasi menggunakan perintah 

    npm install express --save

  ![npm express](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/b4af368a-8ff5-4e0c-8bd6-35c5d216b9eb)

   ![cat package](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/3506728b-1f48-4633-bdcd-b9da21042d13)

Dapat dilihat bahwa informasi tentang framework express sudah muncul pada file **package.json**

#### 5. Buat file NodeJS
Buat sebuah file dengan perintah

    nano index.js
<br/>
    
    const express = require("express");
    const app = express();
    const port = 3000;

    app.get("/", (req, res) => {
      res.send("Hello World!");
    });

    app.listen(port, () => {
      console.log(`Example app listening on port ${port}`);
    });

   ![nano index js](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/2e9001a8-a066-4339-8be7-7f734b026e17)

Jika sudah keluar serta save script, kemudian jalankan aplikasi dengan perintah berikut

    node index.js

   ![node index](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ef160a04-378c-44ac-962d-45b717c24dac)

Bisa dicek bahwa aplikasi sudah berjalan dengan pada web.

   ![Hello-World](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/678d4f85-b5ee-43cb-9591-aaaed89ae15f)

Untuk menghentikan aplikasi cukup klik `ctrl+c`


### python3 
Python merupakan bahasa pemrograman yang banyak digunakan oleh developer karena efisien dan mudah dipelajari serta dapat dijalankan di berbagai platform. Python biasanya secara default sudah terinstall pada sistem operasi linux, untuk melakukan pengecekan bisa menggunakan perintah 

    python3 -V

   ![python3 version](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/ed9d86c9-bbeb-4141-b242-d5a25c85a6cd)

#### 1. Install Packet Manager
Jika nodeJs menggunakan npm sebagai package managernya, maka untuk python menggunakan pip, install pip dengan perintah 

    sudo apt install python3-pip

   ![install pip](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/964130c4-d1a4-48e3-8787-91dc946145e2)

dilanjutkan dengan instalasi flask dengan perintah 

    pip install flask

  ![install flask](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/44202b19-2fbc-42b4-9a07-19f5923d7e97)

Jika sudah kita bisa membuat sebuah aplikasi sederhana python3. Untuk membuat perintah buat terlebih dahulu script dalam file bernama index.py dengan perintah

    nano index.py
<br/>

    from flask import Flask
    app = Flask(__name__)
    @app.route("/")
    def helloworld():
      return "Hello World"
    if __name__ == "__main__":
      app.run(host='10.182.205.169')
      
> note karena saya menggunakan virtual machine, maka dari itu saya menambahkan IP Adress virtual machine agar aplikasi dapat berjalan, IP Adress dapat disesuaikan. 

   ![nano index](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/f25868a5-917a-4c0d-b68e-76d2aae8fd6c)

Jika sudah save script yang sudah dibuat dan keluar dari nano, kemudian jalankan aplikasi dengan perintah berikut

    python3 index.py

   ![running python](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/5dedd425-0d11-4736-9906-6fb06fd9d138)

   ![run python web](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/46a7d6ab-2926-4bba-8be9-60335a12eff8)

Bisa dicek bahwa aplikasi sudah berjalan dengan pada web dengan memasukan IP beserte Port.

## PM2 & Implementation

