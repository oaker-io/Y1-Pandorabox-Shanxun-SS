# Y1-Pandorabox-Shanxun-SS
## Introduction

This project is for Chinese college whom use ChinaNet or Shanxun to skip the client and use WiFi to connect the internet.
And this has been TESTED ON Newifi mini(Y1), other models could refer to this.

**Statement:** All files are from internet and I just gather them up to accomplish this project.

## Reference

[miao1007](https://github.com/miao1007/Openwrt-NetKeeper)  
[branchzero](https://branchzero.com/tech/zj-telecom-shanxun-auto-link.html)  
[naxizi](http://www.encrhome.com/?p=3298)  

**Thanks all these guys work!** 
 
## Support Province

1. Chongqing  
2. Hainan
3. Hangzhou
4. Hebei
5. Nanchang
6. Qinghai
7. Shandong
8. Wuhan

**I successfully used Hangzhou's file in Wenzhou, therefore, I guess it supports other cities in Zhejiang province.**

## Usage
### 1. Download latest Pandorabox&Support files

1. [PandoraBox-ralink-mt7620-y1-squashfs-sysupgrade-r1024-20150608.bin](http://downloads.pandorabox.org.cn/pandorabox/Lenovo-Y1_RY-1S/firmware/stable/)

2. [sxplugin.so](https://github.com/Jarchin/Y1-Pandorabox-Shanxun-SS/releases)

### 2. ROOT Pandorabox in Newifi(Y1)

Use u-boot or [root assistant](http://www.newifi.com/download.shtml) to finish this process.  
When you successed, you could try to login 192.168.1.1, and set up WAN, select **PPPoE** and type your **Username** and **password**  

Save! 

### 3. Upload Files

**1.For Mac or Linux**  
> 1.Open **Terminal**, and type  
`scp yourpronvice_sxplugin.so root@192.168.1.1:/usr/lib/pppd/2.4.7/`  
2.Login to your router  
`ssh root@192.168.1.1`  
3.revise a file  
`vi /etc/config/network`  
4.AFTER "pppoe" line add  
`option pppd_options 'plugin yourprovince_sxplugin.so'`  

NOW log into Luci and redail.  


**2.For Windows** 
> use WINSCP to upload file and revise "network" file in /etc/config/network 

**Now, if every steps you have followed, you could use router to connect to internet.**




