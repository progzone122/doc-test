# Fastboot

## Available commands and mode for fastboot:

### Access fastbootd:
To access fastbootd, you can run `adb reboot fastboot` while the device is booted normally.

> [!WARNING]
> DO NOT reboot to fastbootd from fastboot, as it may cause a dm-verity error due to a glitch.

> [!WARNING]
> DO NOT USE "fastboot reboot fastboot" to reboot into fastbootd, you will get a soft brick!

### Available commands

```sh
fastboot getvar all
fastboot flashing get_unlock_ability
fastboot flashing unlock
fastboot reboot
fastboot oem key <KEY>
fastboot oem get_key
fastboot oem get_socid
fastboot oem p2u <on/off> # sets UART logs
fastboot oem dump_pllk_log # dumps preloader and lk logs
fastboot oem lks # Return the lockstate (1 -> locked, 0 -> unlocked)
fastboot oem scp_status # Crashes fastboot
fastboot oem scp_log_thru_ap_uart <on/off> # Redirects SCP (I don't know what it is) to UART
fastboot oem usb2jtag <1/0> # I think it allows to use a modded usb cable as a JTAG?
```

> [!INFO]
> On the moto g23 and g13, `fastboot flashing unlock_critical` doesn't exist, and instead treats `_critical` as the buffer for
> `fastboot flashing unlock`, making the phone freeze
