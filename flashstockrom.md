
# Flashing Stock ROM

## Pre-requisites
- ADB Downloaded and in System Path
- Developer Options and USB Debugging Enabled
- Hisense A9 Stock Rom downloaded
>[!IMPORTANT]
>**EDL Cable** (without EDL Cable - stock rom cannot be flashed)
- Phone connected via USB ;)



## Flashing Stock ROM on Windows

- Download and install, if not already installed
  - [QFIL 2.0.3.5](https://qfiltool.com/qfil-tool-v2-0-3-5)
  - [Qualcomm HS-USB QDLoader 9008 Driver](https://gsmusbdrivers.com/download/qualcomm-hs-usb-qdloader-9008-driver-64-bit-windows/)
- Reboot you computer
- Open QFIL and select the following options:
  - Select Build Type - <code>Flat Build</code>
  - Programmer Path: Browse and select the <code>prog_firehose_ddr_001360E1.elf</code> file from directory where stock rom is downloaded.
  - Load XML: Select <code>rawprogram0_001360E1</code> to <code>rawprogram5_001360E1</code>. You don't need to select rawprogram_unspare0. Select patch0 to patch5.
  - Storage Type: UFS (located on the bottom right side)
- Put your phone into EDL mode. This is achieved by having it reboot with the EDL cable unplugged. Then plug in your cable, and hold the power button, volume up, volume down, and the button on your EDL cable. Wait until the backlight turns off, then count down from ten. If your screen freezes with the backlight off, congratulations, you are now in EDL mode.
- You should now see your phone as an available port on QFIL. Click download.
- If it hangs and fails, put your phone into EDL again.
- If it succeeds and your phone starts boot looping into a screen which says "fastboot mode", follow above two steps again.
- Turn your phone back on by holding the power button. You should now be directed to the setup screen.


## Flashing Stock ROM on Linux

- Download and install <code>Linaro's QDL Tool</code> if not already installed.
- Add QDL to system path if not already done
- Open terminal window in directory where stock rom is downloaded
- Run below command in terminal window
- <code>qdl --debug --storage ufs --finalize-provisioning --include . prog_firehose_ddr_001360E1.elf rawprogram0_001360E1.xml rawprogram1_001360E1.xml rawprogram2_001360E1.xml rawprogram3_001360E1.xml rawprogram4_001360E1.xml rawprogram5_001360E1.xml patch0.xml patch1.xml patch2.xml patch3.xml patch4.xml patch5.xml</code>
- Put your phone into EDL mode. This is achieved by having it reboot with the EDL cable unplugged. Then plug in your cable, and hold the power button, volume up, volume down, and the button on your EDL cable. Wait until the backlight turns off, then count down from ten. If your screen freezes with the backlight off, congratulations, you are now in EDL mode.
- You can also put your phone into EDL mode by opening another terminal window and typing command -<code> ./adb reboot edl</code>
- If the download is successful then turn your phone back on by holding the power button. You should now be directed to the setup screen.
