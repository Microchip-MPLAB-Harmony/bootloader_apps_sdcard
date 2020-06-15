[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

To clone or download these application from Github,go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/bootloader_apps_sdcard) and then click Clone button to clone this repo or download as zip file. This content can also be download using content manager by following [these instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki)

# SDCARD Bootloader

This example application shows how to use the Bootloader Library to bootload an application using SDCARD protocol.

### Bootloader Application

- This is a bootloader application which resides from
    - The starting location of the flash memory region for SAM devices
    - The starting location of the Boot flash memory region for PIC32MZ devices
    - The starting location of Program Flash memory for PIC32MK and PIC32MX devices
- It uses the Harmony 3 File System Framework to receive the application binary from a sdcard
- It calls the bootloader_Tasks() function which receives application to be programmed into flash memory from a sdcard
- It glows an LED once bootloader firmware is running
- Trigger Methods
    - It uses the On board Switch as bootloader trigger pin to force enter the bootloader at reset of device
    - It checks for bootloader request pattern **(0x5048434D)** from the starting 16 Bytes of RAM to force enter bootloader at reset of device

### Test Application

- This is a test application which resides from
    - The end of bootloader size in device flash memory for SAM devices
    - The end of bootloader size in Program Flash memory for PIC32MK and PIC32MX devices
    - The start of Program Flash memory for PIC32MZ devices
- It will be loaded into flash memory by bootloader application
- It blinks an LED and provides console output
- It uses the On board Switch to trigger the bootloader from firmware
    - Once the switch is pressed it loads first 16 bytes of RAM with bootloader request pattern **(0x5048434D)** and resets the device

## Development Kits
The following table provides links to documentation on how to build and run SDCARD bootloader on different development kits

| Development Kit |
|:---------|
|[PIC32MZ Embedded Graphics with Stacked DRAM (DA) Starter Kit (Crypto)](docs/readme_pic32mz_das_sk.md) |
|[SAM E54 Xplained Pro Evaluation Kit](docs/readme_sam_e54_xpro.md) |
|[SAM E70 Xplained Ultra Evaluation Kit](docs/readme_sam_e70_xult.md) |
|[SAM L22 Xplained Pro Evaluation Kit](docs/readme_sam_l22_xpro.md) |
