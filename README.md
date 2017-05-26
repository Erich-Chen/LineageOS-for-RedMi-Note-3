# LineageOS-for-RedMi-Note-3
my installation of LineageOS for RedMi Note 3 Snapdragon  
Getting tired of MIUI...  

主要的安装过程参考：  
https://wiki.lineageos.org/devices/kenzo/install  

## 去小米官网解锁unlock  
  http://www.miui.com/unlock/index.html
  貌似中文版解锁的回复速度更快一点，手机刚到手就unlock过了，所以记不清楚了。   
  
## 下载安装TWRP
  直接下载地址： https://dl.twrp.me/kenzo/  当前是twrp-3.1.0-kenzo.img  
  访问https://twrp.me/devices/xiaomiredminote3.html  
  直接跳到“Fastboot Install Method (No Root Required)”的部分，参考下载platform工具。  
  ```
    adb reboot bootloader   # 或者按VolDown + Power
    fastboot devices
    fastboot flash recovery twrp-*-*.img
    # fastboot reboot      #输入这条命令，回车的同时按住VolUp键; 
  ```
  或者不用最后一条reboot命令，直接VolUp + Power，进入TWRP  

## 下载安装LineageOS  
  Download LineageOS for RedMi Note 3 (Kenzo) at   
    https://download.lineageos.org/kenzo  
    (ver. 0419 till I am writing)  
  ref. Guideline at  
    https://wiki.lineageos.org/devices/kenzo/install#installing-lineageos-from-recovery  
  其实这个教程包括了全部的三项，但是个别细节没提到。  
  另外，我是把LingeageOS下载到U盘上，然后通过USB-OTG安装的，跟SD卡几乎没有区别。  
  
## 安装Gapps
  下载地址：http://opengapps.org/  
  我需要的是Platform ARM64, Android 7.1， 选择了aroma版，在安装过程中仅选择了小部分app。  
  ref. kenzo的信息：https://wiki.lineageos.org/devices/kenzo  
  我发现安装stock版的话，电话功能不正常，~~因此自己选的时候不要安装google Dialer~~
  安装完成时其实有提示，需要主动去修改默认的电话程序改成Google Dialer
  另文附上我的Gapp Log, 另外下次考虑安装google webView，替换AOSP WebView
  
## 安装supersu  
  ref. https://download.lineageos.org/extras    
  下载arm64的supersu，跟gapps一样在TWRP中安装  
  
## 第一次reboot
  没什么可说  
  
## 注意事项  
  要启用全部的google服务，第一次开机时千万不要插中国的SIM卡。  
  能跳过的全部跳过。  
  a. 启用root，同时启用local terminal  
  b. 利用local terminal，运行这条命令，避免WiFi和Cellular上的叉号.  
  ```
    su
    settings put global captive_portal_https_url https://captive.v2ex.co/generate_204
  ```  
  ref. https://www.v2ex.com/t/303889  
  c. 安装LocationReportEnabler  
      (神器，能够启用包括location history在内的google service）  
    ref.  https://github.com/GhostFlying/LocationReportEnabler  
  d. 配置一个VPN，shadowsocks也可以  
  e. google账号，安装app，etc...   
  f. 插上SIM卡
