**1. Login & Authentication Events**     
  **4624**	Successful logon (Muvaffaqiyatli kirish)      
  **4625**	Failed logon (Muvaffaqiyatsiz kirish)  
  **4634**	User logged off (Foydalanuvchi tizimdan chiqdi)  
  **4648**	Logon with explicit credentials    
  **4672**	Special privileges assigned at logon (Admin rights) (Maxsus imtiyozlarga ega kirish (Administrator huquqlarida))  
  **4776**	NTLM authentication on Domain Controller    
  **4768**	Kerberos Authentication Ticket (TGT) issued  
  **4769**	Kerberos Service Ticket (TGS) issued  
  **4771**	Kerberos authentication failure  
  **4740**	User account locked out (Foydalanuvchi akkaunti blokland)  


**2. Account & Group Changes**   
 **4720**	A new user account was created (Yangi foydalanuvchi yaratildi)  
 **4722**	A user account was enabled (Foydalanuvchi akkaunti faollashtirildi)  
 **4725**	A user account was disabled (Foydalanuvchi akkaunti o‘chirildi)  
 **4726**	A user account was deleted (Foydalanuvchi akkaunti o‘chirildi (Deleted))  
 **4738**	A user account was modified (Foydalanuvchi akkaunti o‘zgartirildi)  
 **4732**	A user was added to a security-enabled group (Foydalanuvchi guruhga qo‘shildi)  
 **4733**	A user was removed from a security-enabled group (Foydalanuvchi guruhdan olib tashlandi)  
 **4756**	A user was added to a privileged group (Administrators, Domain Admins) (Foydalanuvchi   muhim guruhga qo‘shildi (Administrators, Domain Admins))  
 **4757**	A user was removed from a privileged group (Foydalanuvchi muhim guruhdan olib tashlandi)    

**3. Kerberos & NTLM Authentication Events**  
 **4768**	A Kerberos TGT was issued  
 **4769**	A Kerberos service ticket was issued   
 **4771**	Kerberos pre-authentication failed    
 **4776**	NTLM authentication request to Domain Controller   


**4. Privilege & Permission Changes**   
 **4672**	Special privileges assigned at logon (Maxsus imtiyoz bilan tizimga kirish)   
 **4673**	A privileged service was accessed (e.g., SeImpersonatePrivilege) (Maxsus xizmatlar ishlatilishi)   
 **4674**	Privileged object access attempted (Maxsus obyektlarga ruxsat berish)   


**5. Remote Access & RDP Events**  
 **4624** (Logon Type 10/7)	Remote logon (RDP) successful  
 **4625** (Logon Type 3/10)	Remote logon (RDP) failed  
 **4778**	RDP session reconnected  
 **4779**	RDP session disconnected  


**6. File & Audit Log Events**  
 **4663**	Access to a file or folder (Fayl yoki jildga kirish)  
 **5145**	Network share object accessed (Tarmoq orqali faylga kirish)  
 **4656**	A handle to an object was requested (Ob'ektga kirish talabi)  
 **4657**	A critical registry key was modified (Muhim registr kaliti o‘zgartirildi)  


**7. Services & Scheduled Tasks**  
 **4697**	A new service was installed (Yangi xizmat o‘rnatildi)  
 **7045**	A new service was created (Yangi xizmat yaratildi)  
 **4698**	A scheduled task was created (Yangi scheduled task yaratildi)   
 **4699**	A scheduled task was deleted (Scheduled task o‘chirildi)  
 **4702**	A scheduled task was updated (Scheduled task o‘zgartirildi)   


**8. Network & Firewall Events**   
 **5156**	A network connection was allowed (Tarmoqda yangi bog‘lanish yaratildi
)   
 **5157**	A network connection was blocked (Tarmoq bog‘lanishi rad etildi)   
 **5158**	A network session was closed (Tarmoq sessiyasi yakunlandi)    
 **5031**	Windows Firewall blocked a port (Windows Firewall port blokladi)   


**9. Process Execution & Suspicious Activities**   
 **4688**	A new process was created (Yangi jarayon ishga tushirildi)   
 **4689**	A process was terminated (Jarayon yakunlandi)   
 **4691**	A code injection was detected (Code injection aniqlangan)   
 **4964**	In-memory code execution detected (potential threat) (In-memory kod ishlatilgan (xavfli faoliyat))   


**10. Security & Attack Indicators**    
 **1102**	Security log cleared (Potential log tampering attack) (Jurnal tozalandi (Potential Log Cleansing Attack))   
 **4616**	System time changed (Potential attacker activity) (System Time o‘zgartirildi (Potensial hujum alomati))  
 **4776**	NTLM authentication (potential hash relaying)   
 **5140**	Access to a shared network folder (Tarmoqdagi umumiy papkalarga kirish)   
 **4660**	A file or directory was deleted (Fayl yoki katalog o‘chirildi
)    
