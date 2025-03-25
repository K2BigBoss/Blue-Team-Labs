**Beshinchi vazifa:** Tajovuzkorlar qo'lga kiritgan zararlangan kompyuterlarga buyruqlar yubormoqda. Ushbu buyruqlarni  aniqlab, 
hujumlarni bartaraf etish;   

1. **Tarmoqni Kuzatish va Trafikni Tahlil Qilish**
   - Wireshark Filtrlar:
     1. Shubhali IP manzillarni aniqlash:
     ```
     ip.addr == 192.168.1.100
     ```
     2. Buyruq yuborilayotgan portlarni tekshirish (Odatda 4444, 8080, 9001, 53 (DNS), 80 (HTTP), 443 (HTTPS) kabi portlar ishlatiladi):
     ```
     tcp.port == 4444
     tcp.port == 4444 || tcp.port == 8080
     ```
     3. HTTP orqali kelayotgan C2 buyruqlarini topish:
     ```
     http.request
     ```
     4. DNS Tunnelingni aniqlash, Base64 yoki PowerShell buyruqlarini qidirish, Shell jarayonlarini tekshirish:
     ```
     dns && dns.qry.name contains ".xyz"
     http contains "powershell" || http contains "base64"
     tcp contains "cmd.exe"
     ```
   - tcpdump
     1. Trafikni real vaqt rejimida ko'rish:
     ```
     sudo tcpdump -i eth0
     ```
     2. Ma'lum IP manzildan kelayotgan trafikni ushlash:
     ```
     sudo tcpdump -i eth0 host 192.168.1.100
     ```
     3. Port bo'yicha tarmoqni tekshirish:
     ```
     sudo tcpdump -i eth0 port 4444
     ```
     4. Trafikni faylga yozish:
     ```
     sudo tcpdump -i eth0 -w suspicious_traffic.pcap
     ```  

2. **Faol Jarayonlarni Tekshirish:**
  Hujumchilar odatda **nc (netcat)** yoki **powershell** orqali buyruq yuboradi.
 - Linux:
   1. Faol jarayonlarni ko'rish:
   ```
   ps aux
   ```
   2. Netcat yoki bash orqali ochiq shellni topish:
   ```
   lsof -i | grep LISTEN
   ```
 - Windows:
   1. PowerShell yordamida faol jarayonlarni tekshirish:
   ```
   Get-Process | Where-Object { $_.Name -like "*nc*" }
   ```
   2. Shubhali jarayonni to'xtatish:
   ```
   Stop-Process -Id [PID] -Force
   ```  

3. **Tarmoq Ulanishlarini Tekshirish** (Shubhali IP manzillarni aniqlash va monitoring qilish.)
 - Linux:
   1. Faol ulanishlar:
   ```
   netstat -anpt
   ```
   2. Yangi ulanishlarni tekshirish:
   ```
   ss -tulnp
   ```
 - Windows:
   1. CMD da ishlaydigan jarayonlarni tekshirish:
   ```
   netstat -anob
   ```
   2. PowerShell orqali aniqlash:
   ```
   Get-NetTCPConnection | Select-Object LocalAddress, RemoteAddress, RemotePort
   ```
