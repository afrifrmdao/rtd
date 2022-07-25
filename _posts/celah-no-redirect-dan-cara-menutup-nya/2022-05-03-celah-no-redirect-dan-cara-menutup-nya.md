---
title: Celah no redirect dan cara menutup nya
date: 2022-05-03 11:58:47 +07:00
modified:
tags: [exploit, hacking, tutorial, programming]
description: Celah No Redirect Dan Cara Menutupnya.
image: "/celah-no-redirect-dan-cara-menutup-nya/thumb.png"
---


Celah **No Redirect** merupakan celah yang sangat berbahaya, celah ini memungkin kan hacker bisa memasuki halaman dashboard admin tanpa melakukan login.

#### Contoh Kasus
Seorang hacker akan mengunjungi halaman login admin yang terdapat pada URL <a href="#">https://site.com/admin/login.php</a>, hacker tersebut mencoba mencari halaman dashboard admin yang ber alamat kan di <a href="#">https://site.com/admin/dashboard.php</a>, namun hacker tersebut mendapatkan hasil 404 Not Found (file tidak di temukan) atau halaman dashboard tidak di temukan, hacker tersebut lanjut mencoba ke halaman <a href="#">https://site.com/admin/index.php</a>, namun saat mencoba pada alamat itu, hacker tersebut malah di arahkan otomatis ke halaman <a href="#">https://site.com/admin/login.php</a> yang berarti hacker tersebut di minta login terlebih dahulu sebelum memasuki dashboard admin.

Mungkin di alamat <a href="#">https://site.com/admin/index.php</a> terdapat halaman dashboard admin, ini terjadi karena ketika alamat itu di akses, website tersebut otomatis mengarahkan ke halaman admin login bukan menunjukan halaman 404 Not Found seperti pada alamat <a href="#">https://site.com/admin/dashboard.php</a>.

#### Mengecek Celah No Redirect Dengan cURL
Anda bisa memastikan celah No Redirect dengan menggunakan cURL pada terminal anda, perintah cURL ini berfungsi untuk melihat source code pada halaman tersebut:

```bash
$ curl -v https://site.com/[dashboard]
```

karena halaman dashboard admin saat ini di contoh kan pada alamat <a href="#">https://site.com/admin/index.php</a> maka saya akan mengetik kan perintah cURL seperti ini

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/celah-no-redirect-dan-cara-menutup-nya/terminalcurl.png" alt="curl dashboard">
<figcaption>1. curl -v https://site.com/dashboard</figcaption>
</figure>

Jika anda sudah mengetik kan perintah cURL seperti di atas dan anda menemukan source code yang mengarah pada ciri ciri halaman dashboard admin, berarti **website tersebut memiliki celah No Redirect**.

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/celah-no-redirect-dan-cara-menutup-nya/curl-logout.png" alt="log out source code">
<figcaption>2. setelah mengetik kan perinah cURL</figcaption>
</figure>

Setiap halaman dashboard pasti memiliki tombol log out yang akan mengarahkan user untuk meninggalkan halaman dashboard, jika anda menemukan hal yang sama seperti saya, besar kemungkinan memang website tersebut memiliki celah No Redirect.

#### Cara Menutup Celah No Redirect

Anda hanya perlu memasukan code **die()** atau **exit()** pada akhir bagian code redirect.

Source code saat masih mempunyai celah **No Redirect**:
```bash
if(!isset($_SESSION[user])) { 

}
```

Source code yang sudah aman dari **No Redirect**:
```bash
if(!isset($_SESSION[user])) { 
    exit()
}
```

Terakhir untuk tulisan kali ini, terimakasih sudah membaca, _penulis menerima kritik dan saran._
