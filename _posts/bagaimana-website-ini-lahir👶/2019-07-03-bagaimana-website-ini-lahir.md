---
title: Bagaimana website ini lahir👶
date: 2019-07-03 11:58:47 +07:00
modified:
tags: [tutorial, teknologi]
description: Membuat website statis dengan bantuan framework Jekyll.
image: "/bagaimana-website-ini-lahir/jekyll.png"
---


Website ini dibuat menggunakan Jekyll yang merupakan salah satu generator situs open source, dan menggunakan tema sederhana yang di ambil dari situs <a href="http://jekyllthemes.org/">jekyllthemes.org</a>.

<hr>

Semua layanan gratis, kode sumber situs di tempatkan di repositori github saya dan integrasi dengan layanan vercel, situs ini menggunakan halaman github untuk hosting.

<hr>

#### Mari Kita Lakukan
Jadi sebelum kita membuat website, Anda memerlukan beberapa alat seperti

- [JekyllThemes](http://jekyllthemes.org) (template)
- [Github](https://github.com/) account
- [Vercel](https://vercel.com/) (login dengan akun github)

Hal yang pertama anda harus lakukan adalah mencari template di situs <a href="http://jekyllthemes.org">jekyllthemes.org</a>, jika anda sudah melakukan nya anda harus mengunjungi halaman github pembuat template tersebut.

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/search-template.png" alt="Cari template">
<figcaption>1. Cari template</figcaption>
</figure>

Kunjungi halaman github pembuat template
<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/fork-template.png" alt="Klik Fork">
<figcaption>2. Klik Fork</figcaption>
</figure>

Anda harus menekan tombol fork di sebelah kanan atas, ini dilakukan untuk menyimpan source code di repositori github anda.

Selanjutnya silahkan kunjungi halaman dashboard <a href="https://vercel.com">vercel.com</a> lalu login menggunakan akun github anda sendiri.

Buat projek baru di sini:
<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/new-project.png" alt="Projek Baru">
<figcaption>3. Tekan tombol new project</figcaption>
</figure>

Setelah anda menekan tombol new project, <a href="https://vercel.com">vercel.com</a> akan mengarahkan anda ke halaman import repositori git nya

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/import-git.png" alt="import repositori yang sebelumnya sudah di fork">
<figcaption>4. import repositori</figcaption>
</figure>

Anda harus mencari repositori anda yang sudah di fork ke github anda sebelumnya, lalu tekan tombol import.

Anda akan di arahkan ke halaman selanjutnya yaitu halaman konfigurasi projek

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/deploy.png" alt="deploy">
<figcaption>5. Deploy projek </figcaption>
</figure>


Silahkan anda tekan tombol Deploy untuk menyelesaikan konfigurasi projek anda di <a href="https://vercel.com">vercel.com</a>

Beberapa tema akan menyebabkan error saat <a href="https://vercel.com">vercel.com</a> mem-proses konfigurasi projek anda karena beberapa kendala tertentu, silahkan anda cari template atau tema yang baru lalu lakukan ulang seperti cara sebelumnya.

<hr>

#### Setting DNS Manager

Menyetting DNS Manager, ini dilakukan agar situs anda tidak hanya bisa di buka di halaman github anda sendiri ataupun layanan vercel, Saat ini saya memakai layanan <a href="https://jagoanhosting.com">jagoanhosting.com</a> untuk melakukan nya

<figure>
<img src="https://raw.githubusercontent.com/africode7/rtd/master/_posts/bagaimana-website-ini-lahir%F0%9F%91%B6/new-dns.png" alt="DNS Manager">
<figcaption>6. Setting DNS </figcaption>
</figure>

Silahkan anda lakukan perubahan seperti ini
- Tambahnkan hostname (subdomain)
- Ganti type menjadi CNAME
- Masukan addres CNAME Vercel (<a href="cname.vercel-dns.com">cname.vercel-dns.com</a>)

Silahkan anda simpan DNS tersebut dan boom... anda sekarang sudah bisa membuat website seperti ini.

Terakhir untuk tulisan ini, terimakasih sudah membaca, _penulis menerima kritik dan saran._ 
