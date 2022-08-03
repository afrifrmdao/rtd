---
title: XAMPP Pada Ubuntu
date: 2022-06-04 12:58:47 +07:00
modified:
tags: [tutorial, technology]
description: Penjelasan Mengenai Seputar XAMPP.
image: "/xampp-pada-ubuntu/xampp.png"
---

XAMPP adalah perangkat lunak bebas yang mendukung banyak sistem operasi (windows, macOS dan linux), merupakan kompilasi dari beberapa program. Fungsinya adalah sebagai server yang berdiri sendiri, yang terdiri atas program Apache HTTP Server, MYSQL Dataase, dan penerjemah bahasa dengan bahasa pemrograman PHP dan Perl (localhost).

#### Instalasi XAMPP Pada Linux (Ubuntu)

Pertama, anda harus menginstal file installer **XAMPP** di <a href="https://www.apachefriends.org/download.html">apachefriends.org</a>, jika sudah buka terminal linux

Anda dapat mengganti lokasi directory pada terminal anda, jika file installer anda berada di dalam folder **Downloads**

```bash
root@afri~# cd Downloads
```

 Jika tidak maka anda tidak perlu mengganti lokasi directory pada terminal anda. Selanjutnya anda harus mengganti permissions file installer xampp dengan menggunakan perintah:

```bash
root@afri:~/Downloads# chmod 755 xampp-linux-*-installer.run
```

(**GANTI NAMA FILE INSTALLER SESUAI VERSI YANG ANDA DOWNLOAD**)

Jalankan Installer XAMPP dengan perintah
```bash
root@afri:~/Downloads# sudo ./xampp-linux-*-installer.run
```

XAMPP sekarang sudah terinstal di **/opt/lampp** directory.


#### Menjalankan XAMPP 

Untuk menjalankan XAMPP, cukup tuliskan baris perintah sedeherana ini pada terminal anda:

```bash
root@afri:~# sudo /opt/lampp/lampp start
```

Anda sekarang akan melihat sesuatu seperti ini di layar terminal anda:

```bash
Starting XAMPP for Linux 8.0.6-0...

LAMPP: Starting Apache...

LAMPP: Starting MySQL...

LAMPP started.

Ready. Apache and MySQL are running.
```

**(Ketik kan http://localhost pada browser favorit anda untuk memastikan bahwa server sudah berjalan dengan baik pada browser anda)**

Perhatikan bahwa ada alat grafis yang dapat anda gunakan untuk mengelola server anda dengan mudah, anda dapat memulai alat ini dengan perintah berikut:

```bash
root@afri:~# cd /opt/lampp
root@afri:~/opt/lampp# sudo ./manager-linux.run (atau manager-linux-x64.run)
```

#### Menghentikan XAMPP

Untuk menghentikan XAMPP, anda bisa menuliskan baris perintah seperti ini:

```bash
root@afri:~# sudo /opt/lampp/lampp stop
```

Anda sekarang akan melihat sesuatu seperti ini di layar terminal anda:

```bash
Stopping XAMPP for Linux 8.0.6-0...

LAMPP: Stopping Apache...

LAMPP: Stopping MySQL...

LAMPP stopped.
...

LAMPP: Stopping Apache...

LAMPP: Stopping MySQL...

LAMPP stopped.

```

Anda bisa memastikan status server apache anda dengan menuliskan perintah pada terminal anda:

```bash
root@afri~# sudo systemctl status apache2
```

#### Menghentikan Paksa Server Apache

Jika anda mengalami beberapa error saat mencoba mematikan XAMPP anda, anda bisa mencoba untuk menghentikan paksa server apache yang sedang berjalan, anda cukup menuliskan perintah ini pada terminal anda:

```bash
root@afri~# sudo killall apache2
```

Terakhir untuk tulisan kali ini, terimakasih sudah membaca, _penulis menerima kritik dan saran._



