# Jarkom-Modul-1-F10-2023
Laporan resmi praktikum modul 1 wireshark &amp; crimping mata kuliah jaringan komputer <br />
Kelompok: F14 <br />
Nama anggota 1: Ali Hasyimi Assegaf <br />
NRP anggota 1: 5025211131 <br />
Nama anggota 2: Jevon Tama Aristo Manurung <br />
NRP anggota 2: 5025221142 <br />
Nama anggota 3: Dany Dary <br />
NRP anggota 3: 5025211237 <br />

## 1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
Pada permasalahan ini hal yang pertama aku coba lakukan ialah mencari pada bagian info dan aku menemukan bagian yang kemungkinan merupakan perintah untuk mengunggah suatu file<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/6a42cfc5-1f35-40d0-8924-54239fb707e8)<br />
Setelah ditemukan kita bisa melihat sequence number (raw) dan acknowledge number (raw) pada paket tersebut<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/68fadb78-ccc4-445c-b40d-e9c1a84cf5be)
<br />
Setelah itu kita dapat menemukan sequence number (raw) dan acknowledge number (raw) pada paket response<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/13aed85c-e92d-4217-9da7-412137e0b0af)<br />

## 2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
Filter dengan kueri http. Kemudian mem-follow http stream. Informasi web server dapat ditemukan pada kolom Server.<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/f53fa2ff-64c1-4df2-a9f4-583585405858)<br />

## 3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
Filter adengan kueri "(ip.src == 239.255.255.250 or ip.dst == 239.255.255.250) && udp.port == 3702"
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/ac187d89-cafe-487c-ae87-191daef59078)
<br />

Kita tinggal menghitung jumlah paket yang tercapture dan meliha protokol layer trasport apa yang digunakan.

## 4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?
Cek paket nomor 130, nilai checksum ada di bawah dropdown layer transport <br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/a10da933-c0db-4f7e-96aa-847d1100a35a)<br />

## 5. Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
Cek satu-persatu dari paket yang tertangkap. Ditemukan email yang isinya dapat dibaca di paket nomor 22. Email berisi password terenkripsi beserta instruksi memecahkannya, yaitu menggunakan Base64.<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/d5e3f14a-2f8d-4a44-a7ea-677c07009d2e)<br />
Setelah di encode menggunakan base64 didapatkah password "5implePas5word". Buka file zip dan dapatkan “nc 10.21.78.111 11111”.
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/d4c30384-406c-4ff2-9e6e-67ee1d27b6b8)<br />
Total paket 60, Smtp port 25, ip public 74.53.140.153.
