# Information
information

    $ cat /proc/version
    $ cat /proc/cpuinfo

    라즈베리파이 3
    Raspberry Pi 3 B+	(ARM)Quad Core 1.2GHz Cortex-A57 Broadcom BCM2837 64bit CPU



    라즈베리파이 4
    Os: Linux version 4.19.118-v7l+ (dom@buildbot) (gcc version 4.9.3 (crosstool-NG crosstool-ng-1.22.0-88-g8460611)) #1311 SMP Mon Apr 27 14:26:42 BST 2020
    model name: ARMv7 Processor rev 3 (v7l) Cortex-A72 1.5GZ
    Hardware: BCM2835
    Revision: c03112
    Model: Raspberry Pi 4 Model B Rev 1.2



    라즈베리파이 성능 비교 분석
    $ sudo apt install sysbench

    $ sysbench --test=cpu run




    라즈베리파이 4

    Threads fairness:
        events (avg/stddev):           10000.0000/0.00
        execution time (avg/stddev):   92.7153/0.00



    $ sysbench --test=fileio --file-test-mode=seqwr run

    라즈베리파이 4
    Threads fairness:
        events (avg/stddev):           58208.0000/0.00
        execution time (avg/stddev):   122.1220/0.00





Utils

1 putty install

https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html




 git init

 git add .
 
 git commit -m "first"
 
 git config user.email 

 git config user.name
 
 git remote add origin https://github.com/sotoedu/mh_z19Co2.git
 
 git push -u origin master

1  #라즈베리파이 한글 폰트

Setup > cancel

Menu > preferances > Pi  configure >  wifi  country > us

Wifi setup

Open console

sudo apt-get update


1. 폰트 설치 sudo apt-get install fonts-nanum
2. 입력기 설치 sudo apt-get install fcitx-hangul
3. 입력기 지정 im-config -n fcitx

Menu > preferances > Pi  configure >  
locale > ko (korea) EUC-KR
Timezone > asia >seoul
Keyboard > 105key > korea , korea
Ok > Reboot
