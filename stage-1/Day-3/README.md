# DEVOPS-BATCH-19
##### Daily Task - Day 3 - Ardi Solehuddin
- Jelaskan apa itu VCS GIT menurut kalian (gambarkan menurut kalian flow dari git ini seperti apa)
- Dokumentasi beberapa  command dari git (ex git reset, git rebase)

## Vesion Control System
Version Control System adalah perangkat lunak atau sistem yang digunakan untuk membantu melacak dan mengelola perubahan pada sebuah source code secara terus menerus sehingga perubahan yang terjadi tercatat ke dalam database yang nantinya ketika seseorang ingin menggunakan versi source code sebelumnya, pengguna masih bisa menarik/roll back source code tersebut.  

### GIT
Salah satu Version Control System yang umum adalah GIT yaitu tools yang memiliki keunggulan Distributed Version Control System di mana kode tidak hanya berada di satu tempat penyimpanan. Setiap perubahan pada source code di GIT akan terdapat salinan riwayat apa saja yang diubah, dikurangi atau ditambah. 

### Alur GIT
Alur GIT dalam prosesnya adalah di mana ketika developer sudah terhubung atau terintegrasi dengan GITHUB serta telah membuat repository GITHUB yang terhubung dengan database lokal, developer tersebut memiliki beberapa proses untuk bisa memasukan file source code ke GITHUB. Ketika seorang developer telah selesai melakukan pembuatan atau modifikasi kode, developer memiliki file tersebut di penyimpanan lokal, selanjutnya developer tersebut perlu mendeklarasikan file tersebut ke GIT dengan melakukan staged di mana menandai file yang sudah siap untuk disimpan ke database GIT. Selama di stage file belum masuk ke dalam database GIT, untuk memasukannya harus menggunakan perintah commit di mana ketika commit sudah dilakukan maka file kode sudah masuk ke dalam database GIT, selanjutnya file tersebut tinggal dimasukan ke dalam repository yang ada di website github menggunakan perintah git push.


