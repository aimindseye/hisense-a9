# Unlock Bootloader

## Pre-requisites
- ADB Downloaded and in System Path
- Developer Options and USB Debugging Enabled
- Custom Fastboot downloaded
- Phone connected via USB ;)


## Steps to Unlock Bootloader (using Windows as OS)

- Open two command prompt windows (if using Linux, then terminal windows)
- In first window, goto directory where adb is installed if adb is not in system path
- In second window, goto directory where custom fastboot is downloaded
- In first window, enter following command
  - adb reboot bootloader (if using Linux, use ./adb)
- In second window, enter following commands
    - fastboot Hisense unlock (if using Linux, use ./fastboot)
    - fastboot erase avb_custom_key (if using Linux, use ./fastboot)
    - fastboot continue (if using Linux, use ./fastboot)
 - Phone will reboot and display a message in Chinese to confirm a complete data wipe.Press Volume Up and wait.
 - Once phone restarts, you will need to setup phone again.
 - To confirm if bootloader is unlocked, goto Settings> System & Updates > Developer Options. Under OEM unlocking, there will be "Bootloader is already unlocked"


**If you get any errors or do not get any response using fastboot commands then it means you are not using custom fastboot. Repeat the above steps using custom fastboot**
