**Beshinchi vazifa:** Tajovuzkorlar qo'lga kiritgan zararlangan kompyuterlarga buyruqlar yubormoqda. Ushbu buyruqlarni  aniqlab, 
hujumlarni bartaraf etish;   

1. **Faol Jarayonlarni Tekshirish:**
  Hujumchilar odatda **nc (netcat)** yoki **powershell** orqali buyruq yuboradi.
 - Linux
   1. Faol jarayonlarni ko'rish:
   ```
   ps aux
   ```
   2. Netcat yoki bash orqali ochiq shellni topish:
   ```
   lsof -i | grep LISTEN
   ```
