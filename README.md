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
## Teknik injection pada SQL injection evasion
- White space manipulation
  mereka biasanya tidak memasukan white space untuk mengibuli IPS
- 'C' Syntax Comment
  menggunakan C style comment contoh: /* */
  Contoh penggunaan: UNI/**/ON
- Encoding: HEX
- Encoding: BASE 64
- Encoding: Decimal
- Variations on a Theme
  Contoh Penggunaan: EXEC('SEL' + 'ECT US' + 'ER')
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
```-sL``` (Passive) mengirim FIN packets untuk menemukan port terbuka
## Nmap FIN Scan 
```-sF``` (Active Attack) hanya list target tidak ada packet yang terkirim
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
searching google
## Website Footprinting?
mengumpulkan informasi tentang web target seperti CMS, versi, direktori, file, subdomain. menggunakan teknik seperti crawling, robots.txt, sitemap, headers, banner grabbing, dorking.

- Proses dimana bot mengunjungi web untuk mendapatkan konten seperti menggunakan wget
- text file yang ada di site root
- biasanya file dengan ekstensi XML (Contoh: https://example.com/sitemap.xml) biasanya terisi file penting atau index konten
- Headers adalah metadata dari sebuah web menggunakan tools ```curl -I https://example.com```
- banner grabing teknik untuk membaca service banner (HTTP, SSH, SMTP, FTP) contoh: ```curl -I https://example.com``` <- untuk HTTP server header dan ```nc example.com 22``` <- untuk SSH banner
- dorking menggunakan advanced search operators untuk menemukan konten sensitif yang terindex oleh search engine
## Alat Passive Footprinting
WHOIS, passive DNS, Google dorks, Shodan, p0f, archive.org, public registries, social media.
### Fungsi:
- WHOIS: menemukan ownership, registration timeline, registrar, dan mungkin contact info
- passive DNS: untuk menemukan host sebelumnya
- Google Dorks: menemuka panel yang ter-ekspos, file konfigurasi, kredensial, atau dokumen sensitif
- shodan: search engine untuk internet-exposed devices dan services contoh(port:9200 country:"ID"
- p0f: tool untuk menemukan OS dan informasi dengan analisa trafik TCP/IP (fingerprinting)
- archive.org: web archive yang menyimpan snapshot histori sebuah website dan beberapa public files
- public registries: official public databases - meng verifikasi sertifikat SSL
- Social Media: mencari informasi
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
Mengumpulkan informasi umum yang tersedia secara publik
sedangkan **fingerprinting** untuk mencari informasi sistem, os, service, dan versi yang target gunakan.
## CIA TRIAD + nonrepudiation
## 5 elemen utama dasar keamanan
- Confidentiality
- Integrity
- Availibility
- Authentication
- Authorization
## Cyber kill chain
Reconnaissance → Weaponization → Delivery → Exploitation → Installation → Command & Control → Actions on Objectives
- Reconnaissance: Map the target like domains, subdommains, IPs, Services, employees, tech stack.
    Tools used: WHOIS, Passive DNS, Google Dorks, Shodan, archive.org, Social     Media, banner grabbing, nmap scans, p0f
- Weaponization: membangun payload (exploit + mekanisme delivery-nya)
- Delivery: Drop the weapon (phishing, malicious link, upload to web)
- Exploitation: meng eksekusi exploit untuk mendapat akses awal
- Installation: Install persistence
- Command & Control: Remote control channel. domain fronting, fast flux, legitimate services
- Actions on Objectives: Data exfiltration, lateral movement, privilege escalation, ransomware, sabotase 
## Network discovery
mengidentifikasi hosts dan resource didalam jaringan
## Security auditing
Review sistem, konfigurasi, patching, policies, dan logs untuk menemukan kelemahan
