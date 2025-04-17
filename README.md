# Lenovo Legion 5 15ACH6A Linux Mint Postinstall

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

## Fix auto login
Stay on kernel stock, default AMD drivers and Discrete Graphic on BIOS.<br>
Login Windows > Users > Delay before connections (in seconds) > `0`<br>
Users and Groups > Groups > Add `nopasswdlogin`



