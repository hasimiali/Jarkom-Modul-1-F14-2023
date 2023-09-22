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

## 6. Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

Pada soal ini terdapat 3 hal yang dapat diambil sebagai petunjuk untuk mencari jawaban.
1. Terdapat beberapa kata yang memuat huruf besar, yaitu "Seorang", "Udin", "Berteman", "SlameT", "Ia", "valoranT", "terdUga", "Sebuah", dan "Invalid". Sembilan kata itu apabila diambil dan disusun huruf besarnya terbentuk kata SUBSTITUSI.
2. kode invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". Pada kalimat ini, Tulisan "SOURCE ADDRESS 7812" menggunakan huruf besar. Hal ini menunjukkan bahwa kalimat tersebut memiliki pesan khusus.
3. "hasil pencarian hanya menampilkan a1 e5 u21". Dapat dilihat bahwa a1 e5 u21 merupakan pasangan huruf dan angka.
Dari petunjuk pertama dan ketiga, bisa diperkirakan bahwa kita harus melakukan substitusi pada suatu angka atau huruf sesuai dengan pasangan huruf dan urutan hurufnya. Pada petunju kedua, "SOURCE ADDRESS" dapat dikatakan sebagai ip address dari pengirim pada paket tersebut dan "7812" kemungkinan merupakan nomor dari sebuah paket. Ketika kita cek, paket ke 7812 memiliki ip address source yaitu "104.18.14.101". Kita perlu mengubah angka ke bentuk huruf. Angka-angka pada ip tersebut dapat dipisah-pisah menjadi "10 4 18 14 10 1" dan dapat disubtitusi menjadi "JDRNJA".<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/237a01ce-812c-42df-b6f6-4795da7b9732)<br />

## 7. Berapa jumlah packet yang menuju IP 184.87.193.88?
Filter kueri "ip.dst==184.87.193.88"
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/26500389-3d3b-470b-a7dc-a4f50f4583cb)<br />
Terdapat 6 paket.

## 8. Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
Filter kueri "tcp.dstport == 80 || udp.dstport == 80"<br />
![image](https://github.com/hasimiali/PBKK-latihan/assets/34941761/30161985-8c15-4b94-a34c-a0d66c41e63d)<br />

## 9. <img width="273" alt="Screenshot 2023-09-22 at 20 34 33" src="https://github.com/hasimiali/Jarkom-Modul-1-F14-2023/assets/114007555/3913476f-4282-46f4-b9b2-f5036c5b9898">

<img width="528" alt="Screenshot 2023-09-22 at 20 36 00" src="https://github.com/hasimiali/Jarkom-Modul-1-F14-2023/assets/114007555/91f3a295-a47f-47d2-8fd1-e121fd2d51d1">


ip.src == 10.51.40.1 && ip.dst != 10.39.55.34


