# Catatan ETH based on kisi kisi

## Stateful inspection firewall ?
ini juga disebut sebagai *dynamic packet filtering*. ini adalah firewall dengan teknologi yang memonitor kondisi dari koneksi  yang aktif dan menggunakan informasinya untuk mengizinkan network packets melewati firewall
## Hubungan IPS,firewall,honeypot untuk DMZ
- Firewall meng-filter trafik yang masuk dan keluar dari DMZ.
- IPS meng-blokir trafik mencurigkan yang masuk dan keluar dari DMZ.
- Honeypot adalah system palso didalam DMZ untuk menarik penyerang.

DMZ adalah tempat internet mengakses frontend atau server dan service
## Time Based Blind Sql?
Teknik dimana penyerang mengirim payload yang membuat database memiliki delay.
## Teknik injection pada SQL injection Envasion
### Tujuan: menghindari WAF / filter. Teknik umum:
- URL-encoding / hex-encoding payload.
- Commenting (--, /**/) untuk memecah kata kunci.
- Case variation (sElEcT).
- String concatenation ('a'+'b') atau CHAR() untuk bypass filter.
- Whitespace obfuscation: /**/ atau tab/newline.
## IDS berbasis signature dengan teknik Fragmentation
Penyerang memecah payload berbahaya di berbagai pecahan IP/TCP supaya signatures tidak cocok kecuali IDS
## Alat Passive Operating System Fingerprinting  dengan TCP/IP
meng identifikasi target os secara passif menganalisa trafik jaringan tanpa mengirim probes. (contoh tools: p0f)
## Intrusion Prevention System (IPS) ?
system yang mendeteksi dan memblokir trafik yang berbahaya secara otomatis
## Firewall dengan IDS/IPS?
firewall untuk access control ditambah dengan ids/ips untuk deteksi dan pencegahan
## Blind SQL Injection (Injeksi SQL Buta) teknik timing-based atau boolean-based??
- boolean based: mengirim kondisi yang merubah kondisi (true/false) untuk mengambil data
- menggunakan db delay to mengambil hasil dari response time
dua2-nya blind karena tidak ada query output
## Error-based SQL Injection??
memaksa database untuk menghasilkan error yang memberikan data.
mitigasi: merubah detailed errors;
## Serangan Distributed Denial-of-Service (DDoS), serangan Denial-of-Service (DoS) ??
- DoS: sumber tunggal untuk satu target
- DDoS: sumber banyak (botnet)
## serangan DNS Amplification?
penyerang mengirim spoofed dns ke ip korban
## Teknik Firewall Evasion 
Fragmentation, tunneling, enkripsi/ssl, port hopping, portocol obfuscation, permitted protocols.
## List Scan pada Nmap
```-sL```
## Nmap FIN Scan 
```-sF```
## Cyber Kill Chain, fase Weaponization  
penyerang membuat payload(malware, exploit) untuk target. seperti memasukan payload ke dokumen
## fase Reconnaissance 
pengumpulan informasi (pasif atau aktif) seperti domain, subdomain, IPs, teknologi, dan personil
## Peretas Grey Hat (Topi Abu-abu) 
beroperasi diantara ethical dan malicious; seperti exploit sebuah sistem tanpa izin untuk menandai vulnerabilities, terkadang menginformasi kan kepada pemilik selanjutnya
## Black Hat
adalah hacker berbahaya yang mengeksploitasi sistem untuk keuntungan atau kerusakan
## White Hat
ethical hacker dengan izin untuk menguji dan mengamankan sistem
## Google Hacking Database (GHDB)
Collection of Google search queries (“dorks”) that locate sensitive info (backup files, exposed admin pages)
## Website Footprinting?
mengumpulkan informasi tentang web target seperti CMS, versi, direktori, file, subdomain. menggunakan teknik seperti crawling, robots.txt, sitemap, headers, banner grabbing, dorking.
## Alat Passive Footprinting
WHOIS, passive DNS, Google dorks, Shodan, p0f, archive.org, public registries, social media
## IDS?
Deteksi aktifitas berbahay menggunakan signature atau deteksi anomali
## Honeyd?
tool/framework untuk membuat virtual honeypots yang meniru hots dan service untuk menjebak penyerang
## Sql injection apa?
adalah injeksi SQL berbahaya melalui input dan membiarkan penyerang untuk mengeksekusi query
## Efek sql injection?
kebocoran data, modifikasi data, penghapusan data, bypass autentikasi, remote code execution, lateral movement
## Alat LOIC (Low Orbit Ion Cannon) ??
open source tool untuk DoS Floods
## Network Scanning?
mencari hosts, ports, service, dan os di dalam sebuah jaringan
## TCP Communication Flags, flag RST (Reset), flag ACK (Acknowledgement) 
ACK: menerima detail data; bagian dari tcp flow
RST: memutuskan koneksi
## Ethical Hacking 
hacking yang terotorisasi untuk menemukan dan memperbaiki vulnerabilities
## Cracker dan Hacker 
hacker: sebutan umum untuk seseorang dengan teknologi (bisa ethical bisa malicious)
cracker: sebutan untuk seseorang yang masuk ke sistem non-ethically
## Footprinting  
probing (port scans, banner grabbing, vuln scanning)
## Serangan Passive (Pasif)
pengumpulan informasi tanpa memodifikasi resource target
## Active footprinting
probing secara langsung (port scans, banner grabbing, vuln scanning)
## Passive footprinting

## CIA TRIAD + nonrepudiation
## 5 elemen utama dasar keamanan
- Confidentiality
- Integrity
- Availibility
- Authentication
- Authorization
## Cyber kill chain
Reconnaissance → Weaponization → Delivery → Exploitation → Installation → Command & Control → Actions on Objectives.
## Network discovery
mengidentifikasi hosts dan resource didalam jaringan
## Security auditing
Review sistem, konfigurasi, patching, policies, dan logs untuk menemukan kelemahan
