---
title: Memakai VPN Pada Ubuntu
date: 2022-06-04 11:58:47 +07:00
modified:
tags: [tutorial, hacking]
description: Bagaimana Memakai Virtual Private Network pada Ubuntu.
image: "/memakai-vpn-pada-ubuntu/thumb.png"
---

Virtual Private Network atau VPN adalah layanan yang memungkinkan pengguna untuk mengakses situs secara pribadi melalui server jaringan lain. Dengan kata lain, VPN menghubungkan komputer atau telepon genggam ke perangkat lain di tempat yang berbeda sehingga kamu bisa mengakses internet menggunakan koneksinya.


#### Menjalankan VPN  Di Linux - Ubuntu

Pertama anda harus install golang-go, openvpn (autovpn bergantung padanya) dan git (untuk clone autovpn repository dari github). Dalam debian, ubuntu atau linux mint, anda dapat menginstal paket-paket ini menggunakan perintah berikut:

```bash
root@afri~# sudo apt install golang-go openvpn git
```

Lanjut, clone repository autovpn dari github
```bash
root@afri~# git clone https://github.com/vysecurity/autovpn
root@afri~# cd autovpn
root@afri~# go build autovpn.go
```

Dan terakhir, instal executable yang dihasilkan - menggunakan perintah di bawah ini, executable autovpn diinstal di /usr/local/bin/:
```bash
root@afri~# sudo install autovpn /usr/local/bin/
```

Autovpn sangat mudah digunakan - yang harus Anda lakukan adalah menjalankannya dan otomatis akan menghubungkan Anda ke VPN. Secara default (tanpa menentukan kode negara), ini terhubung ke server US acak:

```bash
root@afri~# autovpn
```

Jika Anda ingin menggunakan VPN dari negara lain, tambahkan kode negara, seperti ini (perintah di bawah ini adalah contoh untuk terhubung ke server VPN gratis dari Jepang):

```bash
root@afri~# autovpn JP
```

Cek IP anda di <a href="https://www.vpngate.net/en/">VpnGate</a> dan untuk melihat informasi lengkap lain tentang VPN ini.
