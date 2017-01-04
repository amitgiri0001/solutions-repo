Register ntfs drive to ubuntu(otherwise it would create problem every time you restart if any drive ref is given to some app)

1: sudo blkid(will give UUID of drives) or sudo blkid -c /dev/null
2:  sudo mkdir /media/"name of drive in ubuntu(anything)"
3: sudo nano /etc/fstab (add drive in fstab list with UUID of drive wanna add like this
UUID=DA76E1F176E1CE77 /media/New_Volume ntfs    defaults,nls=utf8,umask=000,uid=1000,windows_names 0       0
)
4: sudo mount -a (restart after if required)

westorm
https://www.youtube.com/watch?v=Q_GOS7otX8k

node
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
// to not use nojs cmd but just node
sudo ln  -s /usr/bin/nodejs /usr/bin/node

// for bower and npm install access issue
sudo chown -R $USER:$GROUP ~/.npm
sudo chown -R $USER:$GROUP ~/.config

// if ruby required
sudo apt-get install ruby-dev

or

sudo add-apt-repository ppa:chris-lea/node.js
sudo apt-get update
sudo apt-get install nodejs



chrome
sudo dpkg -i google-chrome*.deb
(after downloading chrome .deb)

virtual box
see website or 
sudo sh -c "echo 'deb http://download.virtualbox.org/virtualbox/debian '$(lsb_release -cs)' contrib non-free' > /etc/apt/sources.list.d/virtualbox.list" && wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add - && sudo apt-get update && sudo apt-get install virtualbox-5.0

if some kernal module issue comes follow below: 
sudo apt-get install dkms 
and 
*make sure Secure Boot is disabled in BIOS*

Making executable
google making ".desktop" file
[Desktop Entry]
Version=1.1
Name=Skype
Comment=
Exec=
Icon=/home/alex/Pictures/icon.png
Terminal=false
Type=Application
Categories=Utility;Application;

and in EXEC set command like 
/bin/bash -c 'sudo -S <<< "0101" sh "/media/amitu/New Volume/ubuntu/WebStorm-145.1616.9/bin/webstorm.sh"'



if wifi doesn't work or any issue with network:
(worked for me)sudo systemctl restart network-manager.service 
or
(didn't work for me)sudo service network-manager restart


#Remove extra kernal from boot on linux upgrade probably when bootarea gets full
 ##Example how I did before
 
ls /boot

uname -a

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-headers-4.4.0-28

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-headers-4.4.0-42

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-headers-4.4.0-47

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-headers-4.4.0-53

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-image-4.4.0-28-generic

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y linux-image-4.4.0-42-generic

sudo apt-get -y purge linux-image-4.4.0-42-generic

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-image-4.4.0-47-generic

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get -y purge linux-image-4.4.0-53-generic

dpkg -l 'linux-*' | sed '/^ii/!d;/'"$(uname -r | sed "s/\(.*\)-\([^0-9]\+\)/\1/")"'/d;s/^[^ ]* [^ ]* \([^ ]*\).*/\1/;/[0-9]/!d'

sudo apt-get install

sudo apt autoremove

sudo apt-get update

sudo apt-get upgrade

sudo apt-get dist-upgrade

sudo apt-get update



