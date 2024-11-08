Cara menjalankan mining verus via termux

termux-setup-storage

pkg install root-repo 
pkg install x11-repo

yes | pkg update && pkg upgrade

yes | pkg install libjansson wget nano

mkdir ccminer && cd ccminer

wget https://github.com/zeecell/zeeminer.git

chmod +x ccminer start.sh

nano config.json

Lanjut setting wallet dll ... 

untuk menjalankan mining :
./start.sh


Cara setting autorun :
cd && cd && cd && nano ../usr/etc/bash.bashrc

Copykan ini kebaris paling bawah,lalu ctrl X, simpan pilih Y enter
cd ccminer/&&./start.sh


Cara setting auto start :
Download Termux Boot lalu instal
Buka termux

cd ccminer

mkdir ~/.termux/boot
cd ~/.termux/boot
nano termux.sh

copy script dibawah ini lalu ctrl X, simpan pilih Y enter lalu reboot hp

#!/data/data/com.termux/files/usr/bin/sh
termux-wake-lock
~/ccminer/start.sh >> ~/miner.log 2>&1
