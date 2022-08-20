---
title: Pengungkapan Source Code Melalui Git Yang Terbuka
date: 2022-08-18 11:58:47 +07:00
modified:
tags: [exploit, hacking, tutorial, leaked]
description: Pengungkapan Source Code Melalui Git Yang Terbuka
image: "/pengungkapan-source-code-melalui-git-yang-terbuka/git.png"
---

Tulisan ini saya buat sebagai bentuk dokumentasi atau write up untuk diri saya sendiri, pengungkapan source code melalui git yang terbuka.

#### Apa Itu Folder .git?
.git adalah folder yang berisi semua informasi yang diperlukan untuk proyek Anda di kontrol versi dan semua informasi tentang komit, alamat repositori jarak jauh, dll. Semuanya ada di folder ini. Ini juga berisi log yang menyimpan riwayat komit Anda sehingga Anda dapat memutar kembali ke riwayat.

#### Mengapa Git Digunakan Dalam Web Development?
Git sebagian besar digunakan saat Anda membuat situs web di komputer dan menggunakan Git untuk mendorong salinan file tersebut ke server web. Jika sesuatu terjadi pada komputer Anda, Anda masih memiliki salinan lengkap di server web. Anda kemudian dapat mengonfigurasi repositori server web ini untuk mendorong perubahan langsung ke situs web Anda. Ini memberikan keuntungan bagi pengembang dan memberi mereka kemudahan pengembangan

#### Langkah Untuk Melakukan Pengungkapan Source Code
Pertama, anda harus menginstall **git dumper**, git dumper adalah sebuah alat yang mampu mengambil source code di dalam folder git dan menyalin nya ke komputer anda.

1) Install Git Dumper

```bash
$ git clone https://github.com/arthaud/git-dumper
```

2) Tentukan Website

Disini saya akan menggunakan website <a href="https://gismenara.lomboktengahkab.go.id/">https://gismenara.lomboktengahkab.go.id</a> silahkan anda cari folder git di website nya, seperti <a href="https://gismenara.lomboktengahkab.go.id/.git/">https://gismenara.lomboktengahkab.go.id/.git/</a> beberapa website akan menampilkan 403 Forbidden dan ada yang akan terbuka, jika anda menemukan 403 Forbidden jangan khawatir karena sebenernya folder .git nya masih ada.

3) Install Module

```bash
$ pip install -r requirements.txt
```
Module ini di gunakan untuk pelengkap atau syarat untuk menjalankan alatnya.

4) Jalankan Alatnya

```bash
$ python3 git_dumper.py site folder_output
```
Contoh:
```bash
$ python3 git_dumper.py https://gismenara.lomboktengahkab.go.id/.git leaked_source
```

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/pengungkapan-source-code-melalui-git-yang-terbuka/1.png" alt="1. Jalankan Alatnya">
<figcaption>1. Jalankan Alatnya</figcaption>
</figure>

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/pengungkapan-source-code-melalui-git-yang-terbuka/2.png" alt="Tunggu Hingga Selesai">
<figcaption>2. Tunggu Hingga Selesai</figcaption>
</figure>

Setelah itu, silahkan anda cek hasil nya di dalam folder yang anda sudah buat sebelumnya, sebagai contoh sebelumnya saya memberi nama folder **leaked_source**

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/pengungkapan-source-code-melalui-git-yang-terbuka/3.png" alt="Cek Hasilnya di dalam folder">
<figcaption>3. Cek Hasilnya Di Dalam Folder</figcaption>
</figure>

Tulisan ini saya buat hanya untuk dokumentasi atau write up untuk diri saya sendiri, tentu nya untuk edukasi, terima kasih sudah melihat tulisan ini.

_Penulis menerima kritik dan saran._
