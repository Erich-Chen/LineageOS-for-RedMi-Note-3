# LineageOS-for-RedMi-Note-3
my installation of LineageOS for RedMi Note 3 Snapdragon  
Getting tired of MIUI...  


## LineageOS
Follow Guideline at  
https://wiki.lineageos.org/devices/kenzo/install  

1. 去小米官网解锁unlock  
http://www.miui.com/unlock/index.html
貌似中文版解锁的回复速度更快一点，手机刚到手就unlock过了，所以记不清楚了。   

2. 下载安装TWRP
直接下载地址： https://dl.twrp.me/kenzo/  当前是twrp-3.1.0-kenzo.img  
访问https://twrp.me/devices/xiaomiredminote3.html  
直接跳到“Fastboot Install Method (No Root Required)”的部分，参考下载platform工具。  
```
adb reboot bootloader   # 或者按VolDown + Power
fastboot devices
fastboot flash recovery twrp-*-*.img
# fastboot reboot      #输入这条命令，回车的同时按住VolUp键; 
```
或者最后一条reboot命令，直接VolUp + Power，进入TWRP

3. 下载安装LineageOS

Download LineageOS for RedMi Note 3 (Kenzo) at   
https://download.lineageos.org/kenzo
(ver. 0419 till I am writing)  
ref. Guideline at  
https://wiki.lineageos.org/devices/kenzo/install#installing-lineageos-from-recovery
其实这个教程包括了全部的三项，但是个别细节没提到。  
另外，我是把LingeageOS下载到U盘上，然后通过OTG安装的。

4. 安装Gapps
