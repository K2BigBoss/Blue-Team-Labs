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

**HKEY_LOCAL_MACHINE** - Kompyuterning barcha foydalanuvchilarga 
tegishli konfiguratsiya ma’lumotlarini saqlaydi.  

