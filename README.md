# hisense-a9

## repository for hisense-a9 system information 

The aim of this repository is to be wiki for someone who wants to modify/change their hisense a9.
The information is collected from various reddit posts and xdaforums posts.


- [device info](https://github.com/aimindseye/hisense-a9/blob/main/deviceInfo.md)
- [default apps](https://github.com/aimindseye/hisense-a9/blob/main/defaultApps.md)
- [system apps](https://github.com/aimindseye/hisense-a9/blob/main/sysApps.md)


and tips 
- **recommended buy**- EDL cable- cable used on all Qualcomm phones to put phone into DEEP FLASH MODE, also known as Qualcomm 9008 Mode / Emergency Download Mode. 
- [non root modifications](https://github.com/aimindseye/hisense-a9/blob/main/non-root-mods.md) (for someone who just wants basic changes like access to keyboard, eink brower. eink reader, other apps without Google Playstore install)
- [to setup developer mode and usb debugging](https://github.com/aimindseye/hisense-a9/blob/main/devmodeusbdebug.md)
- to debloat and block apps
- [to unlock bootloader](https://github.com/aimindseye/hisense-a9/blob/main/unlockbootloader.md)
- [to root](https://github.com/aimindseye/hisense-a9/blob/main/rootphone.md)
- [update to android/lineage gsi](https://github.com/aimindseye/hisense-a9/blob/main/updateandroidgsi.md)
- [flash to stock rom](https://github.com/aimindseye/hisense-a9/blob/main/flashstockrom.md)
- [backup & restore phone](https://github.com/aimindseye/hisense-a9/blob/main/backuprestore.md)


### A9 Resources:
- [Elf file]( https://drive.google.com/file/d/16tMxSO-fa9BHyBZqoZD7rywGcmyZC_aW/view?usp=drive_link) FireHose Elf file for A9 (needed for restoring to stock rom)
- [Stock rom](https://drive.google.com/drive/folders/1_5PvcvgA9TltEU_XwmiL-t2Eh0VM6C40?usp=drive_link) Hisense A9 stock rom which will have version L2037.6.04.06.00 . You should be able to update to L2037.6.08.01.00(this is last update provided by Hisense) using system update under settings
- [Boot Image & vbmeta](https://drive.google.com/drive/folders/1lSOJqfIWaUJ9EnchshKYnNoZNrFZNY9g?usp=drive_link) These will be used during rooting process.
- [Custom Fastboot](https://drive.google.com/drive/folders/1TB3I6_ejs7Y8GyEumty0aDFiJvycEgWH?usp=drive_link) Created by Denzil Ferreira for unlocking bootloader. Windows and Linux versions are available.

### Android Platform Tools/Apps, Drivers and Other Utilities:

- [ADB:](https://developer.android.com/tools/releases/platform-tools) Download ADB from Android Platform tools for your operating system. **Add directory where ADB installed to path of your operating system.** Fastboot from Android Platform tools will not work for unlocking bootloader. Need to use custom fastboot created by Denzil Ferreira.
- [EDL:](https://wiki.bananahackers.net/en/guides/edl) Qualcomm Emergency Download mode, commonly known as EDL mode, is a special engineering interface implemented on devices with Qualcomm chipsets. Its purpose is to perform special operations on the phone that are intended for device manufacturer only, such as unlocking the bootloader, read and flash firmwares on the phone's filesystem or recover it from being a dead paperweight. Unlike bootloader or Fastboot mode, system files needed by the EDL mode resides on a separate 'primary bootloader' that cannot be affected by software modifications. Below some of EDL utilities:
  - [Renate EDL Utility](http://www.temblast.com/edl.htm) Windows Only
  - [BKerler EDL tool](https://github.com/bkerler/edl) Linux/Windows both
    
- [Google USB Driver:](https://developer.android.com/studio/run/win-usb) The Google USB Driver is required to perform adb debugging on Windows with Google devices. Windows drivers for all other devices are provided by the respective hardware manufacturer, as listed in [Install OEM USB drivers](https://developer.android.com/studio/run/oem-usb) If you're using Linux, then you do not need to install a USB driver. Instead see [Run apps on a hardware device](https://developer.android.com/studio/run/device).
- [Magisk:](https://github.com/topjohnwu/Magisk) Magisk v27.0 was working without any issues. Needed for root access. It can be used for installing apps via modules, unpacking and repacking Android boot images
- [Magisk LiteGapps:](https://sourceforge.net/projects/litegapps/files/litegapps/arm64/) Download the MAKSU version of LiteGapps
- [Magisk HidePropsConf:](https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf/releases) Used to change ur device's fingerprint, to pass SafetyBet's CTS profile check. With device certification, apps that require device certifications will work.ex. bank apps, streaming apps etc.
- [Linaro's QDL:](https://git.codelinaro.org/linaro/qcomlt/qdl) This Linux tool communicates with USB devices of id 05c6:9008 to upload a flash loader and use this to flash images.
- [Qualcomm Flash Image Loader(QFIL):](https://qfiltool.com/qfil-tool-v2-0-3-5) Qualcomm Flash Image Loader (QFIL) is a small Windows application that allows you to flash or install Stock Firmware on devices powered by Qualcomm Chipset.
- [Qualcomm HS-USB QDLoader 9008 Driver- Windows](https://gsmusbdrivers.com/download/qualcomm-hs-usb-qdloader-9008-driver-64-bit-windows/)
- Screen Sharing: These screen sharing utilities are helpful while setting up android gsi and lineage gsi as gsi are not yet optimized for eink devices.
  - [scrcpy:](https://github.com/Genymobile/scrcpy/tree/master) Linux/Windows both
  - [Vysor:](https://www.vysor.io/) Linux/Windows both. Free version works well.

- [Universal SafetyNetFix:](https://github.com/kdrag0n/safetynet-fix/releases) Magisk module to work around Google's SafetyNet and Play Integrity attestation.

## Reference:
- xdaforums - [Hisense a9 root - Reward Offered](https://xdaforums.com/t/hisense-a9-root-reward-offered-snapdragon-662.4495809/)
- reddit - [How to root the Hisense A9](https://www.reddit.com/r/eink/comments/16tpr96/guide_how_to_root_the_hisense_a9/)
