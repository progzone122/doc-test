### Partitions

This is a list of partitions that are of interest for this device:


* **`lk`** -- LittleKernel partition, cannot be written
* **`vbmeta`** -- VBMeta partition, can be flashed via mtkclient, but gives a REDSTATE
* **`boot`** -- Boot partition, main interest for root access and can be written via mtkclient, but gives a REDSTATE


* **`nvram`** -- Contains the IMEI and other device specific information, make a backup
* **`elable`** -- Carrier Lock partition, can be flashed. Flash empty elable.img from firmware to remove carrier lock. Could be a typo of e-label. 
* **`frp`** Factory Reset Protection partition. Also saves if OEM Unlocked is enabled in Developer settings. Can be reset with spefici tools, and maybe mtkclient (not tested). 

To backup all the important partitions, use the [Backup Critical Partition](https://github.com/progzone122/fuckyoumoto/blob/main/backup_critical_partitions.sh) script from [DiabloSat](https://github.com/progzone122/fuckyoumoto/)