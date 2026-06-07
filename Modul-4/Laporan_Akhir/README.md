# Laporan Akhir

## 1. Topologi Jaringan
<img width="1057" height="854" alt="Screenshot 2026-06-04 183507" src="https://github.com/user-attachments/assets/684b9b50-2e58-415f-b6ce-339314824622" />


## 2. Tabel IP Address
<img width="741" height="864" alt="Screenshot 2026-06-07 120003" src="https://github.com/user-attachments/assets/8e582605-cc5b-45f2-abe9-541dad79555f" />

<img width="632" height="842" alt="Screenshot 2026-06-07 120025" src="https://github.com/user-attachments/assets/c20104c9-72d9-42c0-a275-f3a283b1b6a1" />

<img width="1053" height="606" alt="Screenshot 2026-06-07 120052" src="https://github.com/user-attachments/assets/1c65d64e-8788-4569-a670-90aef253f82f" />

## 3. Konfigurasi Tiap Perangkat
<img width="992" height="870" alt="Screenshot 2026-06-07 120137" src="https://github.com/user-attachments/assets/3bce9b06-b14c-4ad5-8587-babf93812033" />

<img width="862" height="871" alt="Screenshot 2026-06-07 120201" src="https://github.com/user-attachments/assets/ccc3ad44-ef23-4c81-8d84-c90d6b6fabf2" />

<img width="896" height="818" alt="Screenshot 2026-06-07 120222" src="https://github.com/user-attachments/assets/f47e7f95-ffc8-4dee-8cf2-c1ef50b0191d" />

<img width="1263" height="875" alt="Screenshot 2026-06-07 120239" src="https://github.com/user-attachments/assets/0f65395a-ad0d-4c12-8f91-6befdcd9ac24" />


## 4. Hasil Pengujian

Hasil pengujian terdapat pada file LA yang ada di folder Laporan_Akhir Modul-4

## 5. Analisis dan Kesimpulan
Pada praktikum ini, dilakukan konfigurasi jaringan menggunakan beberapa perangkat yaitu MikroTik sebagai router ISP, FortiGate sebagai firewall utama, Cisco Router sebagai router internal, serta beberapa client pada jaringan LAN, WAN, dan DMZ.

Dari hasil konfigurasi yang dilakukan, jaringan berhasil dibagi menjadi beberapa segment, yaitu WAN, LAN, dan DMZ dengan subnet yang berbeda. MikroTik berhasil memberikan akses ke jaringan luar (internet simulation) dan terhubung dengan FortiGate melalui jaringan transit 10.10.10.0/30.

FortiGate berfungsi sebagai firewall utama yang mengatur kebijakan komunikasi antar jaringan menggunakan firewall policy. LAN dapat mengakses WAN melalui NAT, sedangkan akses ke DMZ dikontrol menggunakan policy khusus. Selain itu, dilakukan juga konfigurasi VIP (Virtual IP) untuk memungkinkan akses layanan web di DMZ melalui alamat publik.

Hasil pengujian menunjukkan bahwa routing antar jaringan sudah berjalan dengan baik. Client LAN dapat mengakses internet, client WAN dapat mengakses layanan DMZ melalui port forwarding, namun akses langsung dari WAN ke LAN maupun DMZ tanpa aturan firewall berhasil diblokir sesuai dengan kebijakan keamanan yang diterapkan.

Pada sisi troubleshooting, ditemukan beberapa kendala seperti tidak dapatnya ping dari WAN ke FortiGate yang disebabkan oleh konflik konfigurasi VIP dengan IP interface FortiGate. Setelah dilakukan perbaikan konfigurasi, komunikasi antar perangkat kembali normal.

### Kesimpulan
Berdasarkan hasil praktikum ini dapat disimpulkan bahwa:

1. Segmentasi jaringan menggunakan LAN, WAN, dan DMZ berhasil diimplementasikan dengan baik.
2. MikroTik, FortiGate, dan Cisco Router dapat dikonfigurasi untuk mendukung routing antar jaringan.
3. NAT berhasil digunakan untuk memungkinkan akses internet dari jaringan internal.
4. Firewall FortiGate berhasil mengontrol lalu lintas antar jaringan sesuai kebijakan keamanan.
5. VIP (Port Forwarding) memungkinkan akses layanan DMZ dari jaringan eksternal.
6. Konfigurasi yang tidak tepat (seperti konflik IP pada VIP) dapat menyebabkan gangguan komunikasi jaringan.

Secara keseluruhan, praktikum ini berhasil menunjukkan implementasi konsep routing, NAT, firewall, dan segmentasi jaringan dalam lingkungan simulasi.




