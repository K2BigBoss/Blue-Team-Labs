**Endpoint Security Monitoring**  
**Sysinternals**  
Sysinternals vositalari Windows-ga asoslangan 70 dan ortiq vositalarning to'plamidir. Asboblarning har biri quyidagi toifalardan biriga kiradi:  
 - File and Disk Utilities  
 - Networking Utilities  
 - Process Utilities  
 - Security Utilities  
 - System Information  
 - Miscellaneous  

Endpointni tekshirish uchun eng ko'p ishlatiladigan ikkita Sysinternals vositalari:  
 - **TCPView** - Networking Utility vositasi.
 - **Process Explorer** - Process Utility vositasi.


**TCPView** — bu Microsoft Sysinternals tomonidan ishlab chiqilgan tarmoq monitoring utilitasi bo‘lib, Windows tizimidagi faol TCP va UDP ulanishlarini real vaqtda kuzatib boradi. U har bir ulanish haqida quyidagi ma’lumotlarni ko‘rsatadi:    
 - Process Name (which application is using the connection)
 - Local & Remote Addresses (IP and port details)
 - Connection State (e.g., LISTENING, ESTABLISHED, CLOSED)
 - Sent & Received Data Rates 

(https://learn.microsoft.com/en-us/sysinternals/downloads/tcpview)

**Process Explorer** — bu Microsoft Sysinternals tomonidan ishlab chiqilgan kengaytirilgan vazifa menejeri va tizim monitoring vositasi. U ishlayotgan jarayonlar, tizim resurslaridan foydalanish va faol dasturlar haqida batafsil ma’lumot taqdim etadi.  

Process Explorer-ning Asosiy Xususiyatlari:  
 - **Real-vaqt rejimida jarayonlarni kuzatish** – ishlayotgan barcha jarayonlarning CPU, xotira va disk yuklamasini ko‘rsatadi
 - **Jarayon ierarxiyasi** – jarayonlarning ota-bola aloqalarini vizual tarzda tasvirlaydi
 - **DLL va Handle tahlili** – jarayon tomonidan ishlatilayotgan fayllar, registr kalitlari va DLL kutubxonalarini ko‘rsatadi
 - **Virus va zararli dasturlarni aniqlash** – shubhali yoki zararli jarayonlarni tekshirishga yordam beradi
 - **Jarayonni majburan to‘xtatish** – tizim javob bermayotgan yoki zararli jarayonlarni o‘chirish imkonini beradi

(https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer)

**Windows Event Logs**  
                                                 C:\Windows\System32\winevt\Logs  

Windows tizimida ushbu voqea jurnallariga kirishning uchta asosiy usuli mavjud:  
 - **Event Viewer** (GUI-based application)  
 - **Wevtutil.exe** (command-line tool)  
 - **Get-WinEvent** (PowerShell cmdlet)  


**Sysmon (System Monitor)** – bu Windows tizim xizmati va qurilma drayveri bo‘lib, tizim faoliyati haqida batafsil ma’lumotlarni taqdim etadi. U jarayonlar yaratilishi, tarmoq ulanishlari va fayllarga kiritilgan o‘zgarishlarni kuzatib boradi. Sysmon Sysinternals Suite tarkibiga kiradi va asosan xavfsizlik monitoringi, hodisalarga javob berish va tahdidlarni aniqlash uchun ishlatiladi. Sysmon hodisalarni Windows Event Log’ga yozib boradi, bu esa administratorlar va kiberxavfsizlik mutaxassislariga shubhali faoliyatni kuzatish va ilg‘or tahdidlarni aniqlash imkonini beradi.  

https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon  

**OSQuery** – bu Facebook tomonidan ishlab chiqilgan ochiq kodli vosita bo‘lib, foydalanuvchilarga operatsion tizim ma’lumotlarini SQL-ga o‘xshash so‘rovlar yordamida so‘rash va kuzatish imkonini beradi. U tizim ma’lumotlarini tuzilgan va samarali usulda yig‘ish uchun ishlatiladi, jumladan, ishlayotgan jarayonlar, tarmoq ulanishlari, foydalanuvchi faolligi va tizim konfiguratsiyasi kabi ma’lumotlarni olish imkonini beradi.  

https://osquery.io/downloads   

C:\Program Files\osquery\ papkasida osqueryi.exe faylini qo‘lda ishga tushirish mumkin.  

osquery> select pid,name,path from processes where name='lsass.exe';  

**﻿Wazuh** ochiq manbali, erkin foydalanish mumkin bo'lgan va keng qamrovli EDR yechimi bo'lib, xavfsizlik muhandislari uni barcha miqyosdagi muhitda qo'llashlari mumkin.  

**Core Windows Processes**
Task Manager -> Processes
 - **Type** - Har bir jarayon 3 toifadan 1 tasiga kiradi (Apps, Background process, or Windows process).
 - **Publisher** - bu ustunni dastur/fayl muallifining nomi.
 - **PID** - Bu jarayon identifikatori raqami. Windows har safar dastur ishga tushganda noyob jarayon identifikatorini tayinlaydi. Agar bitta dasturda bir nechta ishlaydigan jarayonlar bo'lsa, ularning har biri o'ziga xos jarayon identifikatoriga (PID) ega bo'ladi.
 - **Process name** - bu jarayonning fayl nomi (Taskmrg.exe).
 - **Command line** - jarayonni boshlash uchun ishlatiladigan to'liq buyruq.  
- **CPU** - jarayon foydalanadigan protsessor miqdori.
- **Memory** - jarayon tomonidan ishlatiladigan jismoniy ishchi xotira miqdori.

**Ushbu jarayonlar haqida ko'proq ma'lumot olish uchun qo'shimcha ustunlar qo'shing. Qo'shish uchun yaxshi ustunlar Image path name va Command line.**  

**Albatta, siz xohlagancha ko'p ustun qo'shishingiz mumkin, ammo joriy vazifangizga mos keladigan ustunlarni qo'shish tavsiya etiladi.**   

Task Manager Parent-Child jarayoni ko'rinishini ko'rsatmaydi. Bu yerda Process Hacker va Process Explorer kabi boshqa yordamchi dasturlar yordamga keladi.    

**Process Hacker**  
https://sourceforge.net/projects/systeminformer/   

**Process Explorer**   
https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer  


