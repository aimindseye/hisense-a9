# Backup & Restore using [BKerler EDL tool]

> [!WARNING]
> Please proceed at your own risk. There are chances that performing below instructions could lead to unrecoverable phone.
The author is not responsible for any damage caused to the phone with below instructions. 

## Pre-requisites

- EDL Downloaded and in System Path
- Developer Options and USB Debugging Enabled
- Elf file(prog_firehose_ddr_001360E1.elf) downloaded
- Phone connected via USB ;)


## Backup Phone/Partitions
 - Open command prompt window (if using Linux, then terminal window)
 - Run below command
    - <code>edl rl dumps --memory=ufs --loader=prog_firehose_ddr_001360E1.elf --skip=userdata --genxm</code>
 - dumps is directory name where phone/partitions will be backed up. This directory will be created in directory from where command prompt run
 - if elf file is not in system path then add path to --loader
 - there will be error complaining about lun6. Just ignore it


## Restore Phone/Partitions(if backedup using above instructions)
- Open command prompt window (if using Linux, then terminal window)
 - Run below command
   - <code>edl wl dumps --memory=ufs --loader=prog_firehose_ddr_001360E1.elf</code>
 - dumps is directory name where phone/partitions were backed up.
 - if elf file is not in system path then add path to --loader
