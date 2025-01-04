# PCS mode

> [!WARNING]
> We are actively trying to learn more about this mode, if you have any information that you think might be useful - [send a message in the forum topic “PCS Mode”](https://github.com/orgs/moto-penangf/discussions/8)

It's not known what the mode is, we just discovered it by accident

## What is known about this mode
- It's definitely not BROM / Preloader
- MtkClient / FlashTool does not detect the phone after booting into this mode
- If you disconnect the phone from the PC - it will continue to be in this mode

## Boot to PCS mode
There are **two ways** to boot into PCS mode - using the **VOL- button** or using **KPCOL testpoint**

### Using VOL- button
1. Connect the switched off phone to a PC
2. Wait until Preloader mode is disabled and the gray battery icon appears
3. Press and hold the VOL- button until the phone is detected by the computer

### Using TestPoint KPCOL
1. Connect the switched off phone to a PC
2. Wait until Preloader mode is disabled and the gray battery icon appears
3. Short the testpoint KPCOL to GND

![Image](../files/assets/pcs-mode-kpcol0.png)

## Phone Detection in PCS Mode
On Linux and Windows, the device is detected differently in this mode

### Linux
![Image](../files/assets/pcs-mode-linux.png)

### Windows
![Image](../files/assets/pcs-mode-windows.png)