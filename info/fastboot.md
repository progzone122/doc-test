## Available commands and mode for fastboot:

### Access fastbootd:
To access fastbootd, you can run `adb reboot bootloader` while the device is booted normally.

> [!WARNING]
> DO NOT reboot to fastbootd from fastboot, as it may cause a dm-verity error due to a glitch.

> [!WARNING]
> DO NOT USE "fastboot reboot fastboot" to reboot into fastbootd, you will get a soft brick!

### Available commands

```sh
fastboot getvar all
fastboot oem unlock <KEY> # fastboot will hang and will no longer be detected. Уou will have to reboot
fastboot flashing get_unlock_ability
fastboot flashing unlock # (doesn't unlock)
fastboot flashing unlock_critical # (freezes fastboot and doesn't unlock)
fastboot reboot
```
