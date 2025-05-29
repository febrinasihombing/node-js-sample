# My Node.js Project

## Deskripsi
Aplikasi Node.js sederhana berdasarkan [heroku/node-js-sample](https://github.com/heroku/node-js-sample), di-deploy ke AWS EC2 untuk keperluan mata kuliah SISKA.

## Prasyarat
- Node.js v16 atau lebih tinggi
- AWS CLI (opsional, untuk manajemen EC2)
- Git
- SSH client (untuk akses EC2)

## Instalasi Lokal
1. Clone repositori: `git clone https://github.com/<username>/node-js-sample.git`
2. Masuk ke direktori: `cd node-js-sample`
3. Install dependensi: `npm install`
4. Jalankan aplikasi: `npm start`
5. Buka di browser: `http://localhost:5000`

## Deployment ke AWS EC2
1. Buat instansi EC2 dengan AMI (misalnya, Amazon Linux 2).
2. Konfigurasi SSH: `ssh -i <path-to-key>.pem ec2-user@<ec2-public-ip>`
3. Salin kode ke EC2: `scp -i <path-to-key>.pem -r ./node-js-sample ec2-user@<ec2-public-ip>:/home/ec2-user/`
4. Install Node.js di EC2, lalu jalankan `npm install` dan `npm start`.
5. Buka aplikasi di `http://<ec2-public-ip>:5000`.

## Status
- [x] Aplikasi berjalan di lokal
- [ ] Menyelesaikan koneksi SSH ke EC2
- [ ] Deploy aplikasi ke EC2