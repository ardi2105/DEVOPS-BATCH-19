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

## Dokumentasi GIT
### GIT Reset
GIT Reset adalah suatu cara untuk mengembalikan file yang telah di commit. Terdapat tiga jenis GIT Reset yaitu soft, mixed, dan hard.

1. GIT Reset --Soft

        git reset --soft <commit_number>

    GIT reset soft digunakan untuk kembali ke commit sebelumnya dengan membuat file kembali ke staged area dan tidak mengubah atau menghapus file yang ada di lokal, hanya menghapus history commit saja.<br/> 

    ![git reset](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/1291da34-d825-42c3-8ecd-d15488374265)
    ![reset soft](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/4e388c43-d2d1-4d22-9a74-21a19d2c2876)

2. GIT Reset --Mixed

       git reset --mixed <commit_number>

    GIT reset mixed untuk kembali ke commit sebelumnya serta membuat file dikeluarkan dari staged area atau masuk ke dalam untrack file dan tidak menghapus file lokal.

   ![reset mixed](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/f5ee4287-7e93-4d5f-a75c-f99409d377c0)
    ![hasil git mixed](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/8362f6b3-3817-4880-8177-c7431891ab12)

3. GIT Reset --Hard

        git reset --hard <commit_number>

    GIT reset hard akan mengembalikan file dari commit serta akan menghapus file dari staged area serta menghapus file yang berada di lokal. 

    ![git hard](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/bec0db6c-436a-4b67-ad0a-3f19a80e160e)

### GIT Revert
GIT Revert hampir mirip dengan GIT Reset di mana untuk kembali ke commit sebelumnya, perbedannya adalah git reset akan merubah commit history dengan menghapus commit, sedangkan git revert tidak merubah commit history melainkan akan kembali ke commit sebelumnya dengan membuat commit yang baru.

    git revert <commit_number>

   ![git revert berhasil](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/009f17d2-229a-4195-8cb9-c27a182f9539)
   ![Hasil revert](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/a0b512d8-b189-4a14-bad2-2cea710c8cb4)

   Dapat dilihat pada script yang sebelumnya diubah, ketika menggunakan git revert script kembali seperti semula.

### GIT Reflog
Git reflog menampilkan log history lebih detail dibandingkan dengan git log oneline serta dapat melacak setiap perubahan yang mempengaruhi lokasi referensi pada Git. Reflog disimpan hanya sebagai bagian dari repositori lokal dan tidak dibagikan dengan remote. reflog secara default tersimpan selama 90 hari.

    git reflog show

   ![git reflog](https://github.com/ardi2105/DEVOPS-BATCH-19/assets/151701736/75003ba2-e2e9-4de7-aa60-215d0ee1188d)
