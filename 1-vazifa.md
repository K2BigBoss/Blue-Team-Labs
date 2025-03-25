**1. Tarmoq va Tizimga Ulanish Holatini Tekshirish**   
📌 **Nmap (Network Mapper)** – Tarmoqni skanerlash. Bu vosita tarmoqdagi ochiq portlar, xizmatlar va zaifliklarni aniqlashda qo‘llaniladi.  
```
nmap -sV -O [IP-manzil yoki subnet]
nmap --script vuln [IP-manzil]
nmap -p- [IP-manzil]
```   
Ochiq portlar va xizmatlarni topish.
Eskirgan xizmatlar va ularning zaifliklarini aniqlash.   

📌 **Netstat** – Tizimda ishlayotgan tarmoq ulanishlarini ko‘rish  
Windows yoki Linux tizimda qaysi portlar ochiq va qaysi jarayonlar ulanish hosil qilayotganini aniqlash.  

➤ Asosiy buyruqlar:     
Barcha faol ulanishlarni ko‘rish:   
```netstat -an```
Jarayonlar bilan birga ko‘rish:   
```
netstat -anb (Windows)
netstat -tulnp (Linux)
```
✅ Foydasi:   

Tizimda noma'lum yoki zararli ulanishlarni aniqlash.  

Shubhali IP manzillarga ketayotgan traffikni tekshirish.  

**🔍 2. Loglar va Hodisalarni Tahlil Qilish**
📌 **Sysmon** – Ilg‘or jarayon va tarmoq monitoring vositasi
Sysmon Windows tizimida jarayonlar, tarmoq aloqalari va boshqa muhim voqealarni qayd qiladi.

➤ Sysmon’ni o‘rnatish va sozlash:
Sysmon’ni yuklab olish va o‘rnatish:

sysmon.exe -accepteula -i sysmonconfig.xml
Sysmon loglarini ko‘rish:

Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational"
✅ Foydasi:

Process Creation (Event ID 1): Yangi jarayonlar kuzatuvi.

Network Connection (Event ID 3): Tarmoqda chiqadigan va keladigan trafikni tekshirish.

DLL yuklash (Event ID 7): Buzilgan jarayonlarni aniqlash.

📌 **Windows Event Log** – Windows tizim loglarini tahlil qilish    
Windows tizimida yuz berayotgan hodisalarni tahlil qilish uchun ishlatiladi.  

➤ Loglarni ko‘rish:
```wevtutil qe Security /f:Text /c:10```
Bu buyruq oxirgi 10 ta xavfsizlik hodisasini chiqaradi.

➤ Muhim loglar:
4624 – Muvaffaqiyatli login.

4625 – Muvaffaqiyatsiz login.

4688 – Yangi jarayon yaratildi.

4720 – Yangi foydalanuvchi yaratildi.

✅ Foydasi:

Xavfsizlik buzilishini aniqlash.

Kerakli va shubhali harakatlarni kuzatish.

🔥 3. Zaifliklarni Tekshirish va Tahlil Qilish
📌 Lynis – Linux va Unix tizimlarida audit qilish
Lynis – Linux tizimlarida zaifliklarni aniqlash va tahlil qilish uchun vosita.

➤ O‘rnatish va ishga tushirish:
```
sudo apt install lynis
sudo lynis audit system
```
✅ Foydasi:

Tizimdagi noto‘g‘ri sozlamalar va zaifliklarni aniqlash.

Parol siyosatini tekshirish.

📌 Windows uchun Auditpol – Audit siyosatini ko‘rish va o‘zgartirish
Windows tizimida auditni boshqarish uchun ishlatiladi.

➤ Auditni yoqish va tekshirish:  
Auditni ko‘rish:  
```
auditpol /get /category:*
```
Login hodisalarini yoqish:
```
auditpol /set /category:"Logon/Logoff" /success:enable /failure:enable
```
✅ Foydasi:

Xavfsizlikni buzadigan jarayonlarni aniqlash.

Login va foydalanuvchi faoliyatini kuzatish.

🧱 4. Himoya Choralarini Ko‘rish
📌 Firewalld (Linux) yoki Windows Firewall
Faol ulanishlarni cheklash va xavfsiz ulanish siyosatini o‘rnatish.

➤ Linux:
```
sudo firewall-cmd --list-all
sudo firewall-cmd --add-service=ssh --permanent
sudo firewall-cmd --reload
```
➤ Windows:
```netsh advfirewall set allprofiles state on```
✅ Foydasi:

Tarmoqdagi nojoiz ulanishlarni bloklash.

Hujumlarni oldini olish.

📡 5. Monitoring va Xabardorlik
📌 SIEM (Security Information and Event Management)
SIEM tizimlari loglarni to‘plash, normalash va tahdidlarni aniqlashda foydalaniladi. Mashhur SIEM vositalari:

Splunk

ELK Stack (Elasticsearch, Logstash, Kibana)

Graylog

✅ Foydasi:

Real-time tahlil va tahdidlarni aniqlash.

Keng qamrovli xavfsizlik hisobotlarini tuzish.

📊 6. Blue Team Strategiyasi uchun Muhim Amallar
Tarmoqni skanerlash – Nmap, Netstat.

Loglarni kuzatish va tahlil qilish – Sysmon, Windows Event Viewer.

Zaifliklarni aniqlash – Lynis, Windows Auditpol.

Himoya siyosatini kuchaytirish – Firewall sozlamalarini tekshirish.
