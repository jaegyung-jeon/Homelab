# NTFS, SHARE permission setup

1. create a folder  
>>>>>Work
>>>>- management</br>
>>>>- shopfloor



</br>
</br>

2. share permission

>>>right click-properties-sharing-advanced sharing

</br>![IIS Test](screenshots/1.png)




3. NTFS permission

>>>right click-properties-security-advanced sharing
>>>>management-full control, shop-read only</br>

![IIS Test](screenshots/2.png) </br>


4. Check shared file access / NTFS permission at client vm
>>type : \\\server ip address\shared file </br>
>>ex)  : \\\192.168.45.10\Work

![IIS Test](screenshots/3.png) </br>


# Drive mapping

Create drive mapping group policy in Group Policy Management </br>
<*make sure to link OU in domain once group policy is created>

>>User Configuration - Preferences - Windows settings - Drive Maps
>>>Action : Create</br> 
Location : \\\server ip\file name</br>
Drive Letter : ex)F

![IIS Test](screenshots/4.png) </br>


