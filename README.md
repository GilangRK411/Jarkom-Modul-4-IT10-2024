# Jarkom-Modul-4-IT10-2024


# Anggota Kelompok
| Nama | NRP |
| ---------------------- | ---------- |
| Khansa Adia Rahma      | 5027221071 |
| Gilang Raya Kurnaiwan   | 5027221045 |

Soal Jarkom Modul 4 2024

- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.

- Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau sebaliknya
  
- Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN.
  
- Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
  
- Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan
  
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.
 
- Seluruh node yang ada pada topologi harus dapat TERKONEKSI satu sama lain dan dapat melakukan PING ke node lainnya yang ada di topologi


# Prefix IP
Prefux IP yang diguanakan kelompok kami ```192.238```

# CIDR

CIDR adalah singkatan dari "Classless Inter-Domain Routing" yang merupakan sebuah metode untuk mengalokasikan dan mengelola alamat IP dalam jaringan komputer. Metode ini memungkinkan untuk pengelompokan alamat IP secara lebih efisien daripada metode yang lain yang menggunakan kelas seperti Class A, B, dan C. Dengan CIDR, alamat IP dipecah menjadi blok-blok yang lebih kecil yang disebut sebagai "CIDR blocks". Setiap blok CIDR terdiri dari alamat IP bersama dengan angka yang menunjukkan jumlah bit dari alamat IP yang digunakan untuk menyatakan jaringan, biasanya ditunjukkan dalam notasi seperti "alamat IP/prefix_length". Misalnya, "192.238.1.0/24" menunjukkan bahwa 24 bit pertama dari alamat IP tersebut digunakan untuk menunjukkan jaringan, sementara sisanya digunakan untuk mengidentifikasi host dalam jaringan tersebut. Ini memungkinkan fleksibilitas yang lebih besar dalam penentuan ukuran jaringan dan alokasi alamat IP.

# Tolopogi GNS CIDR

Berikut adalah Topologi Pohon CIDR

![image](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/70e0fd70-b2aa-4398-b529-ad85d5166231)

# Penggabungan Subnnet CIDR

Berikut adalah Penggabungan Subnnet

![image](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/db7371c0-1e7b-4f3c-9e27-ae29017fa070)

![image](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/a147b139-04da-472b-bdf9-725c5fc8dd3c)

# Pembagian IP dari subnet CIDR

Berikut adalah Grouping, Pembagian IP dari subnet CIDR dan Tree nya

Grouping

![Group 1](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/ca75f282-f424-4bb6-bd25-b76dcd788281)

Tree

Setelah di lakukan grouping data data yang ada dioalah dengna menggunakan teknik tree, dengan menyusun dari class paling tinggi ke paling rendah, dengan class yang paling rendah yang nantinya akan diambil misal subnet A1,A2, etc.

![IT10 CIDR drawio](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/6f47716b-219b-422d-9c53-70555c3fd875)

Lalu dilakukan Pembagian IP sesuai dengan hasil yang di dapat pada proses tree

![image](https://github.com/GilangRK411/Jarkom-Modul-4-IT10-2024/assets/143797853/12091bec-6d16-4887-bc97-876cc826b946)

# Konfigurasi IP CIDR

Node Jawa

```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
    address 192.238.148.1
    netmask 255.255.255.0

auto eth2
iface eth2 inet static
    address 192.240.0.1
    netmask 255.255.255.0

auto eth3
iface eth3 inet static
    address 192.238.68.1
    netmask 255.255.255.0
```

Node Sumatra

```
auto eth0
iface eth0 inet static
    address 192.238.136.2
    netmask 255.255.255.0
    gateway 192.238.136.1
```





