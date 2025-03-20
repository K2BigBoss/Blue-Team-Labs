**Windows Forensics** (Windows uchun kompyuter kriminalistikasi)  

**Windows Registry** - bu tizim konfiguratsiyasi ma'lumotlarini 
o'z ichiga olgan ma'lumotlar bazalari to'plami. Ushbu 
konfiguratsiya ma'lumotlari apparat, dasturiy ta'minot yoki 
foydalanuvchi ma'lumotlari haqida bo'lishi mumkin. Shuningdek, 
u yaqinda foydalanilgan fayllar, foydalanilgan dasturlar yoki 
tizimga ulangan qurilmalar haqidagi ma'lumotlarni o'z ichiga 
oladi.   
Har qanday Windows tizimidagi registrda quyidagi beshta 
asosiy kalit mavjud:  
**Win + R -> regedit**  
 - HKEY_CURRENT_USER
 - HKEY_USERS
 - HKEY_LOCAL_MACHINE
 - HKEY_CLASSES_ROOT
 - HKEY_CURRENT_CONFIG

**HKEY_CURRENT_USER** - Joriy tizimga kirgan foydalanuvchining 
konfiguratsiya ma’lumotlarini o‘z ichiga oladi. Bu yerda 
user's folders, screen colors va Control Panel sozlamalari
saqlanadi. Ushbu ma’lumotlar foydalanuvchi profili bilan 
bog‘langan bo‘ladi.  

**HKEY_USERS** - Kompyuterda hozir yuklangan barcha foydalanuvchi 
profillarini o‘z ichiga oladi. HKEY_CURRENT_USER ushbu 
kalitning ichki bo‘limi hisoblanadi.   

**HKEY_LOCAL_MACHINE** - Kompyuterning barcha foydalanuvchilarga tegishli konfiguratsiya ma’lumotlarini saqlaydi.  

**HKEY_CLASSES_ROOT** — bu **HKEY_LOCAL_MACHINE\Software** subkaliti hisoblanadi. Bu yerda saqlanadigan ma'lumotlar Windows Explorer orqali fayl ochilganda to‘g‘ri dastur ishga tushishini ta'minlaydi.  

 - Windows 2000 dan boshlab, ushbu ma'lumotlar **HKEY_LOCAL_MACHINE** va **HKEY_CURRENT_USER** kalitlari ostida saqlanadi. **HKEY_LOCAL_MACHINE\Software\Classes** kaliti mahalliy kompyuterning barcha foydalanuvchilariga tegishli standart sozlamalarni o‘z ichiga oladi. **HKEY_CURRENT_USER\Software\Classes** esa standart sozlamalarni o‘zgartirib, faqat interaktiv foydalanuvchiga tegishli sozlamalarni saqlaydi.  
 - **HKEY_CLASSES_ROOT** bu ikki manbadan ma'lumotlarni birlashtirilgan holda ko‘rsatadi. Bu kalit eski Windows versiyalari uchun yozilgan dasturlar uchun ham ushbu birlashtirilgan ko‘rinishni taqdim etadi. Agar interaktiv foydalanuvchi uchun sozlamalarni o‘zgartirish kerak bo‘lsa, **HKEY_CLASSES_ROOT** o‘rniga **HKEY_CURRENT_USER\Software\Classes** ostida o‘zgarish kiritish lozim.
 - Standart sozlamalarni o‘zgartirish uchun esa **HKEY_LOCAL_MACHINE\Software\Classes** ostida o‘zgarish kiritish kerak. Agar **HKEY_CLASSES_ROOT** ostida kalit yozilsa, tizim ushbu ma'lumotlarni **HKEY_LOCAL_MACHINE\Software\Classes** ostida saqlaydi.  
 - Agar **HKEY_CLASSES_ROOT** ostidagi mavjud kalitga qiymat yozilsa va ushbu kalit **HKEY_CURRENT_USER\Software\Classes** ostida mavjud bo‘lsa, tizim ma'lumotlarni **HKEY_LOCAL_MACHINE\Software\Classes** o‘rniga **HKEY_CURRENT_USER\Software\Classes** ostida saqlaydi.

**HKEY_CURRENT_CONFIG** mahalliy kompyuter tizim yuklanish vaqtida foydalanadigan apparat profili haqida ma'lumotlarni o‘z ichiga oladi.   
Agar sizda faqat disk tasviriga (disk image) kirish imkoni bo‘lsa, registry hive-larining qayerda joylashganligini bilishingiz kerak bo‘ladi.  
Ko‘pchilik hive-lar **C:\Windows\System32\Config** katalogida joylashgan bo‘lib, ular quyidagilardan iborat:  
 - **DEFAULT** (mounted on **HKEY_USERS\DEFAULT**)
 - **SAM** (mounted on **HKEY_LOCAL_MACHINE\SAM**)
 - **SECURITY** (mounted on **HKEY_LOCAL_MACHINE\Security**)
 - **SOFTWARE** (mounted on **HKEY_LOCAL_MACHINE\Software**)
 - **SYSTEM (mounted on HKEY_LOCAL_MACHINE\System**)  

**SAM (Security Account Manager)**: Foydalanuvchi hisoblarini, parol hashlarini va autentifikatsiya ma’lumotlarini saqlaydi.  

**SECURITY**: Lokal xavfsizlik siyosatlari va tizim xavfsizligi bilan bog‘liq ma’lumotlarni saqlaydi.  

**SYSTEM**: Kompyuterning apparat va yuklanish parametrlari haqida ma’lumot beradi.  

**SOFTWARE**: O‘rnatilgan dasturlar va tizimda ro‘yxatdan o‘tgan ilovalar haqidagi ma’lumotlarni saqlaydi.  

Foydalanuvchi ma'lumotlarini o'z ichiga olgan yana ikkita hiveni Foydalanuvchi profili katalogida topish mumkin **(C:\Users\<username>\)**.
 - **NTUSER.DAT** (foydalanuvchi tizimga kirganda HKEY_CURRENT_USER da oʻrnatiladi)
 - **USRCLASS.DAT** (HKEY_CURRENT_USER\Software\CLASSES da o'rnatilgan)  

USRCLASS.DAT hive **C:\Users\<username>\AppData\Local\Microsoft\Windows** katalogda joylashgan. 

**NTUSER.DAT** va **USRCLASS.DAT** yashirin fayllar ekanligini unutmang.  

 - **NTUSER.DAT**: Har bir foydalanuvchining shaxsiy Windows sozlamalari, dasturlar konfiguratsiyasi va boshqa ma’lumotlarni saqlaydi.
 - **USRCLASS.DAT**: Foydalanuvchi profili bilan bog‘liq sinflar (CLSID) va dastur sozlamalarini o‘z ichiga oladi.
