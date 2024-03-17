# Updating Hisense A9 to Android/Lineages GSI

> [!WARNING]
> Please proceed at your own risk. There are chances that performing below instructions could lead to unrecoverable phone.
The author is not responsible for any damage caused to the phone with below instructions. 


## Pre-requisites

- ADB Downloaded and in System Path
- Developer Options and USB Debugging Enabled
> [!IMPORTANT]
> Custom fastboot | Bootloader Unlocked | vbmeta downloaded.
- Desired Android/Lineage GSI downloaded
> [!NOTE]
> You will need to download non vndklite, arm64 ,ab version GSI for Hisense A9. Depending on your use- you can download secure|personal,with gapps or not, with super user or not. For more details visit -https://droidwin.com/arm64-a64-bgn-bvn-bgs-vndklite-which-gsi-to-download/ 
- Phone connected via USB ;)

## Steps to flashing Android/Lineage GSI

- Copy downloaded Android/Lineage GSI file to directory where custom fastboot and vbmeta are downloaded
- Open Command prompt window in directory to the above directory(if using Linux, then terminal window)
- Enter following command
  - <code>adb reboot bootloader</code>(if using Linux, use ./adb)
- To verify the Fastboot connection, type in the below command and you should get back the device ID.
  - <code>fastboot devices</code>(if using Linux, use ./fastboot)
> [!NOTE]
> If you are not getting any serial ID, then please install the Fastboot Drivers. Before proceeding further
- Disable verity check
  - <code>fastboot --disable-verification flash vbmeta vbmeta.img</code>(if using Linux, use ./fastboot)
- Boot into fastboot
  - <code>fastboot reboot fastboot</code>(if using Linux, use ./fastboot)
- Flash downloaded Android/Lineage GSI
  - <code>fastboot flash system <name_of_image.img></code>(if using Linux, use ./fastboot)
- Wipe User data
  - <code>fastboot -w</code>(if using Linux, use ./fastboot)
> [!NOTE]
> You might get error about failing to erase cache partition. User data has been erased if there is no other error
- Reboot the device
  -<code>fastboot reboot</code>(if using Linux, use ./fastboot)
- If everything above is successful, then phone will reboot to setup screen
> [!NOTE]
> Depending on GSI, some additional tweaks might be required to setup phone successfully. Would recommend using screen sharing utilities from your computer to setup with ease. For ex. running following command <code>adb shell wm density 360&& adb reboot</code> will help with resolution of phone during initial setup.
