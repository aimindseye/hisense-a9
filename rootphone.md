# Rooting Hisense A9


## Pre-requisites

- ADB Downloaded and in System Path
- Developer Options and USB Debugging Enabled
> [!IMPORTANT]
> Custom Fastboot downloaded | Bootloader Unlocked | Boot Images and vbmeta downloaded.

> [!NOTE]
> Depending on your firmware version, use appropriate boot.img
- Magisk installed on phone
- Phone connected via USB ;)


## Steps to root phone on Windows

- Copy appropriate boot.img to your phome
- Open Magisk on your phone
- Select Install
- Select "Select and Patch a File"
- Pick the  copied "boot.img" from the file manager
- Select "Let's Go"
- Move the magisk_patched image file(it will be created in same folder where boot.img was copied to, on your phone)to your computer(in same folder where vbmeta.img is downloaded)
- Rename to magisk_patched_boot.img
- Open Command prompt window in directory where vbmeta.img and magisk_patched_boot.img are located(if using Linux, then terminal window)
- Enter following commands
  - <code>adb reboot bootloader</code>(if using Linux, use ./adb)
  - <code>fastboot flash --disable-verity --disable-verification vbmeta vbmeta.img</code>(if using Linux, use ./fastboot)
  - <code>fastboot flash boot_a magisk_patched_boot.img</code>(if using Linux, use ./fastboot)
  - <code>fastboot flash boot_b magisk_patched_boot.img</code>(if using Linux, use ./fastboot)
  - <code>fastboot reboot</code>(if using Linux, use ./fastboot)
 - If everything above is successful, then phone will reboot and it should be rooted.
 - To confirm, Open Magisk app on your phone. It should prompt you to reboot. On reboot, check that Superuser tab is enabled
