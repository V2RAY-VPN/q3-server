# q3-server
My Quake 3 dedicated server configuration
Quake III Linux installation
https://help.ubuntu.com/community/Games/Native/QuakeIIIArena

http://ubuntuforums.org/showthread.php?t=1977312

http://www.cyberciti.biz/faq/linux-install-doom3-game/

Quake III Arena
 
Installation (Retail)
 
 Data Files
 
mkdir /<path to install>/quake3
mount /cdrom
cp -r /cdrom/Quake3/baseq3 /<path to install>/quake3
umount /cdrom
 

Binaries

cd /<path to install>/quake3
wget ftp://ftp.idsoftware.com/idstuff/quake3/linux/linuxq3apoint-1.32b-3.x86.run
chmod +x linuxq3apoint-1.32b-3.x86.run
./linuxq3apoint-1.32b-3.x86.run (Use "/<path to install>/quake3" when asked)
 

Security Fix

wget ftp://ftp.idsoftware.com/idstuff/quake3/quake3-1.32c.zip
unzip quake3-1.32c.zip
cp Quake\ III\ Arena\ 1.32c/linux/* .
rm -rf Quake\ III\ Arena\ 1.32c/
 

Troubleshooting
Sound
If you have no sound with the following error message in console

/dev/dsp: Input/output error
Could not mmap /dev/dsp
you can try the following fix

sudo nano /etc/init.d/bootmisc.sh
add lines above : exit 0
echo 'quake3.x86 0 0 direct' > /proc/asound/card0/pcm0p/oss
echo 'quake3-smp.x86 0 0 direct' > /proc/asound/card0/pcm0p/oss''
 

Playing

Single CPU Systems
./quake3
 
Multiple (SMP) CPU Systems
./quake3-smp
 

Quake III Arena Mods
Q3JailBreak
Q3Pong
Rocket Arena Q3A

 
