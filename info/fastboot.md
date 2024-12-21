## Available commands and mode for fastboot:

### Access fastbootd:

To access fastbootd, you can run `adb reboot bootloader` while the device is booted normally.<br>
DO NOT reboot to fastbootd from fastboot, as it may cause a dm-verity error due to a glitch.

### Available commands

```sh
fastboot getvar all
fastboot oem unlock <KEY> # fastboot will hang and will no longer be detected. Уou will have to reboot
fastboot flashing get_unlock_ability
fastboot flashing unlock # (doesn't unlock)
fastboot flashing unlock_critical # (freezes fastboot and doesn't unlock)
fastboot reboot
```