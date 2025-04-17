# Lenovo Legion 5 15ACH6A Linux Mint Postinstall

```
             ...-:::::-...                  
          .-MMMMMMMMMMMMMMM-.               
      .-MMMM`..-:::::::-..`MMMM-.          OS: Linux Mint 22.1 x86_64 
    .:MMMM.:MMMMMMMMMMMMMMM:.MMMM:.        Host: 82NW Legion 5 15ACH6A 
   -MMM-M---MMMMMMMMMMMMMMMMMMM.MMM-       Kernel: 6.8.0-58-generic 
 `:MMM:MM`  :MMMM:....::-...-MMMM:MMM:`    Shell: bash 5.2.21
 :MMM:MMM`  :MM:`  ``    ``  `:MMM:MMM:    Resolution: 2912x1638
.MMM.MMMM`  :MM.  -MM.  .MM-  `MMMM.MMM.   DE: Cinnamon 6.4.8 
:MMM:MMMM`  :MM.  -MM-  .MM:  `MMMM-MMM:   WM: Mutter (Muffin) 
:MMM:MMMM`  :MM.  -MM-  .MM:  `MMMM:MMM:   Terminal: gnome-terminal
:MMM:MMMM`  :MM.  -MM-  .MM:  `MMMM-MMM:   CPU: AMD Ryzen 5 5600H with Radeon Graphics (12) @ 4.280GHz
.MMM.MMMM`  :MM:--:MM:--:MM:  `MMMM.MMM.   GPU: AMD ATI Radeon RX 6600/6600 XT/6600M
 :MMM:MMM-  `-MMMMMMMMMMMM-`  -MMM-MMM:    Memory: 4673MiB / 15841MiB
  :MMM:MMM:`                `:MMM:MMM:     
   .MMM.MMMM:--------------:MMMM.MMM.       
     '-MMMM.-MMMMMMMMMMMMMMM-.MMMM-'        
       '.-MMMM``--:::::--``MMMM-.'          
            '-MMMMMMMMMMMMM-'               
               ``-:::::-``
```                                                  

## BIOS
Disable Secure Boot<br>
Use Discrete Graphics mode (don't worry, derivatives of Windows, Linux, MacOS, ChromiumOS and Androidx84 will work)

## Install
Don't install [LMDE](https://linuxmint.com/download_lmde.php), use [Ubuntu derivative](https://linuxmint.com/download.php) or you'll loose Grub in Windows dual boot

## Fix Grub
For better loading, stay un Discrete Graphic mode.<br>
1. Open Grub Config:
```
sudo xed /etc/default/grub
```
2. Add this line:
```
GRUB_PRELOAD_MODULES="part_gpt part_msdos videoinfo gfxterm"
```
3. For different resolutions add/edit this:
```
GRUB_GFXMODE="{{resolution here}}"
```
Allowed Grub resolutions for this device:<br>
2560x1440x32 (16:9)<br>
640x480x32 (4:3)<br>
800x600x32 (4:3)<br>
1024x768x32 (4:3)<br>
1280x1024x32 (5:4)<br>
1400x1050x32 (4:3)<br>
1600x1200x32 (4:3)<br>
1280x960x32 (4:3)

## Kernel
Stay on stock kernel, don't change.

## AMD drivers
Stay on default AMD drivers, [AMD web graphics drivers](https://www.amd.com/en/support/download/linux-drivers.html) will work worst.

## Fix autologin
Stay on kernel stock, default AMD drivers and Discrete Graphic on BIOS.<br>
Login Windows > Users > Delay before connections (in seconds) > `0`<br>
Users and Groups > Groups > Add `nopasswdlogin`

## Fix resolution
1. Open Display
2. Go to Settings > Enable fraction scaling control > `Enable`
3. Go to Layout and change Monitor scale<br>
125% ≈ 1920x1080 FHD<br>
150% ≈ 1600x900 HD+<br>
175% ≈ 1366x768 HD<br>
   



