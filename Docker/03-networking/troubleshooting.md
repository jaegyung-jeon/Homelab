# Breaking DNS on purpose & fix it

## 1. Change DNS from 192.168.45.10 --> 1.1.1.1

![IIS Test](03screenshots/15.png)






## 2. Check DNS status (Domain joining failed)

![IIS Test](03screenshots/14.png)

+ CMD - gpdupate /force, ipconfig /flushdns 
+ Powershell - whoami /fqdn, ping company.local

Domain joined    

<img src="03screenshots/1.png" width="350">



vs



Not joined

<img src="03screenshots/2.png" width="350">




## 3. Fix/change back to domain controller ip : "192.168.45.10"
>>1.1.1.1 --> 192.168.45.10 </br>
>>CMD: ipconfi /flushdns,   gpupdate /force

## 4. Test Again
>>CMD: ipconfig /all, ping company.local