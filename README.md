

# Information

Index of /raspbian/images

http://downloads.raspberrypi.org/raspbian/images/

Utils

1 Win32DiskImager

http://sourceforge.net/projects/win32diskimager/


2 putty install

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html


1  #라즈베리파이 한글 폰트

Setup > cancel

Menu > preferances > Pi  configure >  wifi  country > us

Wifi setup

Open console

sudo apt-get update


1. 폰트 설치 sudo apt install fonts-nanum
2. 입력기 설치 sudo apt install fcitx-hangul -y
3. 입력기 지정 im-config -n fcitx

Menu > preferances > Pi  configure >  
locale > ko (korea) EUC-KR
Timezone > asia >seoul
Keyboard > 105key > korea , korea
Ok > Reboot

2
samba

    $ sudo apt-get install samba samba-common-bin
    
    Samba server and utilities -->  NO
    
    $ sudo smbpasswd -a pi
    
    $ sudo nano /etc/samba/smb.conf
    
    [pi]
    path = /home/pi
    writeable=Yes
    create mast=0777
    directory mast=0777
    public=no
    
    $ sudo systemctl restart smbd
    
    
    
    3 
information

    $ cat /proc/version
    $ cat /proc/cpuinfo
    $ cat /proc/device-tree/model

    라즈베리파이 3
    OS: Linux version 4.14.98-v7+ (dom@dom-XPS-13-9370) (gcc version 4.9.3 (crosstool-NG crosstool-ng-1.22.0-88-g8460611)) 
    #1200 SMP Tue Feb 12 20:27:48 GMT 2019
    model name      : ARMv7 Processor rev 4 (v7l) Raspberry Pi 3 B+	(ARM)Quad Core 1.4GHz Cortex-A57 Broadcom BCM2837 64bit CPU
    Hardware        : BCM2835
    Revision        : a52082
    Model: Raspberry Pi 3 Model B Rev 1.2

    라즈베리파이 4
    Os: Linux version 4.19.118-v7l+ (dom@buildbot) (gcc version 4.9.3 (crosstool-NG crosstool-ng-1.22.0-88-g8460611)) 
    #1311 SMP Mon Apr 27 14:26:42 BST 2020
    model name: ARMv7 Processor rev 3 (v7l) Cortex-A72 1.5GZ
    Hardware: BCM2835
    Revision: c03112 (4GB) /a03111 (1GB) / b03111 (2GB) / d03114 (8GB)
    Model: Raspberry Pi 4 Model B Rev 1.2
    
    라즈베리파이 성능 비교 분석
    $ sudo apt install sysbench

    $ sysbench --test=cpu run
    
    라즈베리파이 3
    
    Threads fairness:
    events (avg/stddev):           10000.0000/0.00
    execution time (avg/stddev):   139.0755/0.00

    라즈베리파이 4

    Threads fairness:
        events (avg/stddev):           10000.0000/0.00
        execution time (avg/stddev):   92.7153/0.00



    $ sysbench --test=fileio --file-test-mode=seqwr run
    
    라즈베리파이 3
    
    Threads fairness:
    events (avg/stddev):           131072.0000/0.00
    execution time (avg/stddev):   171.7977/0.00


    라즈베리파이 4
    
    Threads fairness:
        events (avg/stddev):           58208.0000/0.00
        execution time (avg/stddev):   122.1220/0.00
    
    
    
    멀티 쓰레드
    sysbench --test=cpu --cpu-max-prime=10000 --num-threads=4 run

    싱글 쓰레드
    sysbench --test=cpu --cpu-max-prime=10000 --num-threads=1 run
    
    
    멀티
    3
    Threads fairness:
    events (avg/stddev):           2500.0000/9.35
    execution time (avg/stddev):   34.9161/0.01

    
    4
    Threads fairness:
    events (avg/stddev):           2500.0000/92.97
    execution time (avg/stddev):   23.7309/0.00
    
    싱글
    3
    Threads fairness:
    events (avg/stddev):           10000.0000/0.00
    execution time (avg/stddev):   139.6026/0.00
    
    4
    Threads fairness:
    events (avg/stddev):           10000.0000/0.00
    execution time (avg/stddev):   92.7026/0.00



 git init

 git add .
 
 git commit -m "first"
 
 git config user.email 

 git config user.name
 
 git remote add origin https://github.com/sotoedu/mh_z19Co2.git
 
 git push -u origin master




![tn_scan](https://user-images.githubusercontent.com/17608995/89761088-a9abba00-db28-11ea-86e5-c803496396dd.jpg)

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/ELCaLhCEJ7A/0.jpg)](https://youtu.be/ELCaLhCEJ7A)
