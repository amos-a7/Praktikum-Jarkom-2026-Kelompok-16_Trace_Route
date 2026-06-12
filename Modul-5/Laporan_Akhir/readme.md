# Laporan Akhir

## 1. Topologi Jaringan
<img width="694" height="868" alt="1 1" src="https://github.com/user-attachments/assets/3498cf6f-6c64-4ed7-af9a-84c77a34f449" />




## 2. Tabel IP Address
<img width="900" height="1600" alt="WhatsApp Image 2026-06-07 at 09 46 27" src="https://github.com/user-attachments/assets/a3ef958a-7fea-48b2-a373-a00fe6622b07" />


## 3. Konfigurasi Tiap Perangkat
<img width="960" height="877" alt="1 2" src="https://github.com/user-attachments/assets/ee8f1764-42ca-4b6c-bec1-0bb90b1abef1" />
<img width="961" height="864" alt="1 3" src="https://github.com/user-attachments/assets/f441dd4f-ec43-4f9e-a61b-9956a0e3f23e" />
<img width="961" height="872" alt="2 2" src="https://github.com/user-attachments/assets/ba1d4089-e35f-4f10-a0dc-9dd6a6268b95" />
<img width="953" height="295" alt="3 1" src="https://github.com/user-attachments/assets/62b56a1b-ee65-4cf4-8992-d0c130121bcf" />
<img width="962" height="151" alt="3 2" src="https://github.com/user-attachments/assets/ee19edd3-862f-405a-873f-3855ddc61e45" />
<img width="958" height="268" alt="3 4" src="https://github.com/user-attachments/assets/59451fcd-3bad-471a-b53c-d94cea5688b5" />
<img width="916" height="240" alt="4 1" src="https://github.com/user-attachments/assets/af0da0db-e5c0-476b-a85b-83912d0cefb4" />
<img width="959" height="107" alt="4 2" src="https://github.com/user-attachments/assets/4922d834-2eb4-45d5-8444-cd8c65790eef" />
<img width="956" height="865" alt="5 1" src="https://github.com/user-attachments/assets/6db8f3b9-f547-4336-a8d1-7fab904df553" />
<img width="951" height="615" alt="5 2" src="https://github.com/user-attachments/assets/a92ba564-1873-4b3f-894b-d61b217f4b02" />
<img width="986" height="863" alt="5 3" src="https://github.com/user-attachments/assets/99b93548-0bd1-4dad-b956-72c2381dd22e" />


## 4. Hasil Pengujian

Hasil pengujian terdapat pada file LA yang ada di folder Laporan_Akhir Modul-5

## 5. Analisis dan Kesimpulan
## Analisis

Pada praktikum ini dilakukan implementasi jaringan perusahaan yang terdiri atas beberapa segmen jaringan menggunakan VLAN untuk memisahkan divisi Finance, IT, dan Server. Pemisahan VLAN bertujuan meningkatkan keamanan, memudahkan pengelolaan jaringan, serta mengurangi broadcast domain pada jaringan.

Inter-VLAN Routing diimplementasikan menggunakan metode Router-on-a-Stick pada Cisco Router dengan memanfaatkan subinterface GigabitEthernet0/1.10, GigabitEthernet0/1.20, dan GigabitEthernet0/1.60. Setiap subinterface dikonfigurasi dengan VLAN ID dan alamat IP yang sesuai sehingga perangkat pada VLAN yang berbeda dapat saling berkomunikasi melalui proses routing.

Untuk meningkatkan ketersediaan layanan gateway, digunakan protokol VRRP antara Cisco Router dan MikroTik. Dengan adanya VRRP, kedua perangkat dapat menyediakan gateway virtual yang sama bagi host pada masing-masing VLAN. Apabila salah satu perangkat mengalami gangguan, perangkat lain dapat mengambil alih fungsi gateway sehingga layanan jaringan tetap berjalan. Pada implementasi ini Cisco dikonfigurasi sebagai master pada VLAN tertentu dan MikroTik sebagai backup, sedangkan pada VLAN lain MikroTik berperan sebagai master sesuai kebutuhan desain jaringan.

FortiGate digunakan sebagai firewall sekaligus gateway menuju ISP. Konfigurasi static route dan firewall policy memungkinkan lalu lintas dari jaringan internal menuju internet dapat diteruskan dengan benar. Selain itu, NAT pada FortiGate memungkinkan alamat IP private dari jaringan internal diterjemahkan menjadi alamat IP yang dapat digunakan untuk mengakses jaringan publik.

Selama proses konfigurasi ditemukan beberapa kendala, seperti interface router yang masih berstatus administratively down, konfigurasi yang belum tersimpan sehingga hilang setelah perangkat direstart, serta masalah konektivitas akibat konfigurasi trunk dan VLAN yang belum sesuai. Permasalahan tersebut berhasil diatasi dengan melakukan verifikasi konfigurasi interface, routing, VRRP, serta memastikan setiap perangkat terhubung pada VLAN yang benar.

Berdasarkan hasil pengujian, host pada masing-masing VLAN berhasil memperoleh alamat IP yang sesuai, dapat berkomunikasi dengan gateway virtual VRRP, melakukan komunikasi antar VLAN, serta mengakses internet melalui FortiGate dan ISP. Hasil tersebut menunjukkan bahwa konfigurasi VLAN, routing, VRRP, dan firewall telah berfungsi sesuai dengan tujuan praktikum.


## Kesimpulan

1. VLAN berhasil diimplementasikan untuk memisahkan jaringan Finance, IT, dan Server sehingga setiap segmen jaringan memiliki broadcast domain yang terpisah.

2. Inter-VLAN Routing menggunakan metode Router-on-a-Stick pada Cisco Router berhasil memungkinkan komunikasi antar VLAN yang berbeda.

3. Protokol VRRP berhasil diterapkan pada Cisco Router dan MikroTik sehingga menyediakan mekanisme redundansi gateway dan meningkatkan ketersediaan layanan jaringan.

4. FortiGate berhasil dikonfigurasi sebagai firewall dan gateway menuju ISP dengan penerapan routing, NAT, dan firewall policy yang memungkinkan akses internet dari jaringan internal.

5. Pengujian konektivitas menunjukkan bahwa perangkat pada masing-masing VLAN dapat berkomunikasi dengan gateway, melakukan komunikasi antar jaringan, serta mengakses internet sesuai dengan konfigurasi yang telah dibuat.

6. Praktikum ini memberikan pemahaman mengenai implementasi VLAN, routing, VRRP, firewall, dan troubleshooting jaringan yang diperlukan dalam membangun infrastruktur jaringan perusahaan yang andal dan terstruktur.






