# Back up Boot Image using BKerler's EDL tool


> [!WARNING]
> Please proceed at your own risk. There are chances that performing below instructions could lead to unrecoverable phone.
The author is not responsible for any damage caused to the phone with below instructions. 

## Pre-requisites

- BKerler's EDL tool Downloaded and in System Path
- Developer Options and USB Debugging Enabled
- Elf file(prog_firehose_ddr_001360E1.elf) downloaded
- Phone connected via USB ;)


## Backup Boot Image
 - Find out your active partition using fastboot getvar all
 - Open command prompt window (if using Linux, then terminal window)
 - Run below command (if active partition is b , use boot_b, if a then use boot_a)
    - <code>edl r boot_b  boot.img --memory=ufs --loader=prog_firehose_ddr_001360E1.elf</code>
 - if elf file is not in system path then add path to --loader
 - there will be error complaining about lun6. Just ignore it
