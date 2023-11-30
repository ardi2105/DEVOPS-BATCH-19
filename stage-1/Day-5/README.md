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

## PM2 & Implementation

