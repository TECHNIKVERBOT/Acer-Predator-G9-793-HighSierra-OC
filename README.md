# Acer-Predator-G9-793-HighSierra-OC
 
 ### This repo includes the OpenCore EFI for Acer Predator G9-793 on High Sierra

Tested on:

Model | NB50TK1
------------- | ---------------
CPU | Intel Core i7-6700HQ
dGPU | NVIDIA GTX 1060
RAM | 16 GB DDR4
SSD | 500 GB WD Blue M.2 (SATA)
HDD | Toshiba L200 2 TB
WiFi | Qualcomm Atheros QCA6174
Software | macOS 10.13.6 High Sierra (running off an external drive)

## What works?

* Battery
* TrackPad
* Sleep
* Sound (incl. audio jack)
* GPU acceleration (using NVIDIA Web Driver)
* Internal SATA devices (thanks to SATA-unsupported.kext)

## What doesn't work?

* HDMI (not tested)
* Brightness control
* WiFi
* Bluetooth

## How to install

Download this repo and place the EFI folder into your EFI Partition... That's it.

## How to Install macOS High Sierra

1. Have a working install of macOS, download the Installer from the App Store, then make a bootable Installer with `createinstallmedia` by using this command in Terminal `sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume`

2. If you're on Windows, use [gibMacOS](https://github.com/corpnewt/gibMacOS) by corpnewt.

After you made a bootable Installer, copy the EFI folder to the EFI partition and install as usual. After the installation, mount the EFI of the installed OS and copy the EFI folder to its partition.

If you want an OOTB-WiFi: You need to change your WiFi card in order for your internet to work. Go to eBay or your trusted website and find a suitable card (M.2 NGFF) with the kexts.

Thanks to:

- [SkyrillHD](https://github.com/SkyrilHD) (for originally creating the EFI months ago)
- me (for recently trying SATA-unsupported)
- acidanthera (for making OpenCore)
- dortania (for their guide and SATA-unsupported.kext)
- [Max2002_](https://twitter.com/max2002_) (our tester)
