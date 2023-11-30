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

   ![nvm install](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/943dd44b-21b0-4e80-b1c4-96335f7f6647)

Periksa versi node dan npm dengan perintah

    node -v
    npm -v

#### 3. Inisiasi project
Masukan printah npm init untuk menginisiasi project, ketika ini dijalankan akan terdapat file baru bernama package.json di mana file ini nantinya akan berisi informasi apa package yang digunakan oleh aplikasi yang dibuat.

    npm init -y

   ![node init](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/9c517fc7-43af-4999-b46b-7703667d8361)


## PM2 & Implementation

