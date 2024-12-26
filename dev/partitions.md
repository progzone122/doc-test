### Partitions

>[!NOTE]
> Most sections are only accessible via mtkclient

This is a list of partitions that are of interest for this device:

| Partition name                                    | Read | Write |
|---------------------------------------------------|------|-------|
| misc                                              | ✅    | ❌     |
| para                                              | ✅    | ❌     |
| expdb                                             | ✅    | ❌     |
| frp                                               | ✅    | ❌     |
| hw                                                | ✅    | ❌     |
| uTags                                             | ✅    | ❌     |
| uTagsBackup                                       | ✅    | ❌     |
| vbmeta_a<br/>vbmeta_b                             | ✅    | ✅     |
| vbmeta_system_a<br/>vbmeta_system_b               | ✅    | ✅     |
| vbmeta_vendor_a<br/>vbmeta_vendor_b               | ✅    | ✅     |
| md_udc                                            | ✅    | ❌     |
| metadata                                          | ✅    | ❌     |
| nvcfg                                             | ✅    | ✅     |
| nvdata                                            | ✅    | ❌     |
| persist                                           | ✅    | ✅     |
| protect1                                          | ✅    | ✅     |
| protect2                                          | ✅    | ✅     |
| seccfg                                            | ✅    | ❌     |
| md1img_a<br/>md1img_b                             | ✅    | ❌     |
| spmfw_a<br/>spmfw_b                               | ✅    | ❌     |
| scp_a<br/>scp_b                                   | ✅    | ❌     |
| sspm_a<br/>sspm_b                                 | ✅    | ❌     |
| gz_a<br/>gz_b                                     | ✅    | ❌     |
| lk_a<br/>lk_b                                     | ✅    | ❌     |
| boot_a<br/>boot_b                                 | ✅    | ✅     |
| vendor_boot_a<br/>vendor_boot_b                   | ✅    | ✅     |
| dtbo_a<br/>dtbo_b                                 | ✅    | ❌     |
| tee_a<br/>tee_b                                   | ✅    | ❌     |
| sec1                                              | ✅    | ❌     |
| proinfo                                           | ✅    | ✅     |
| boot_para                                         | ✅    | ❌     |
| nvram                                             | ✅    | ✅     |
| rfcal                                             | ✅    | ❌     |
| cid                                               | ✅    | ❌     |
| sp                                                | ✅    | ❌     |
| elable                                            | ✅    | ✅     |
| prodber                                           | ✅    | ❌     |
| kpan                                              | ✅    | ❌     |
| logs                                              | ✅    | ❌     |
| carrier                                           | ✅    | ❌     |
| pad5<br/>pad4<br/>pad3<br/>pad2<br/>pad1<br/>pad0 | ✅    | ❌     |
| kdebuginfo                                        | ✅    | ❌     |
| logo                                              | ✅    | ❌     |
| super                                             | ✅    | ✅     |
| userdata                                          | ✅    | ❔     |
| otp                                               | ✅    | ❌     |
| flashinfo                                         | ✅    | ❌     |

* **`lk`** -- LittleKernel partition, cannot be written
* **`vbmeta`** -- VBMeta partition, can be flashed via mtkclient, but gives a REDSTATE
* **`boot`** -- Boot partition, main interest for root access and can be written via mtkclient, but gives a REDSTATE


* **`nvram`** -- Contains the IMEI and other device specific information, make a backup
* **`elable`** -- Carrier Lock partition, can be flashed. Flash empty elable.img from firmware to remove carrier lock. Could be a typo of e-label. 
* **`frp`** Factory Reset Protection partition. Also saves if OEM Unlocked is enabled in Developer settings. Can be reset with spefici tools, and maybe mtkclient (not tested). 

To backup all the important partitions, use the [Backup Critical Partition](https://github.com/moto-penangf/fuckyoumoto/blob/main/backup_critical_partitions.sh) script from [DiabloSat](https://github.com/moto-penangf/fuckyoumoto/)
