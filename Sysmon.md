https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon   
https://github.com/olafhartong/sysmon-modular/blob/master/sysmonconfig.xml   
SysmonView -> https://github.com/nshalabi/SysmonTools/blob/master/SysmonView/64.zip    

**1. Sysmon’ni o‘rnatish:**  
```
sysmon -accepteula -i sysmonconfig.xml
```
**2. Sysmon’ni tekshirish:**
```
sysmon.exe -c
```

Event Viewer   
Windows + R -> eventvwr.msc   
Applications and Services Logs -> Microsoft -> Windows -> Sysmon -> Operational   

sysmonviewlog.xml -> SysmonView
![image](https://github.com/user-attachments/assets/30e6a413-24a1-47d0-b92f-46dcf4496c63)

https://medium.com/@Mr.Aur0ra/a-guide-to-sysmon-view-9c2e2c373397

**Sysmon Event IDs**
Event ID 1: Process creation  
Event ID 2: Process changed a file creation time  
Event ID 3: Network connection  
Event ID 4: Sysmon service state changed  
Event ID 5: Process terminated  
Event ID 6: Driver loaded   
Event ID 7: Image loaded   
Event ID 8: CreateRemoteThread   
Event ID 9: RawAccessRead   
Event ID 10: ProcessAccess   
Event ID 11: FileCreate   
Event ID 12: RegistryEvent (Creation and Deletion)   
Event ID 13: RegistryEvent (Value set)   
Event ID 14: Registry Event (Key and Value rename)   
Event ID 15: FileCreateStreamHash   
Event ID 16: ServiceConfigurationChange   
Event ID 17: PipeEvent (Creation)   
Event ID 18: PipeEvent (Connected)   
Event ID 19: WmiEvent (WmiEventFilter activity)   
Event ID 20: WmiEvent (WmiEventConsumer activity)   
Event ID 21: WmiEvent (WmiEventConsumerToFilter activity)   
Event ID 22: DNSEvent (DNS Query)   
Event ID 23: FileDelete   
Event ID 255: Error   


