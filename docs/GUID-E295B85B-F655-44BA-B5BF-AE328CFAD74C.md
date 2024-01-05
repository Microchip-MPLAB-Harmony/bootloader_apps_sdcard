# SDCARD Bootloader

This example application shows how to use the File System Bootloader Library to bootload an application using SDCARD protocol.

**Bootloader Application**

-   This is a bootloader application which resides from

    -   The starting location of the flash memory region for SAM devices

    -   The starting location of the Boot flash memory region for PIC32MZ devices

    -   The starting location of Program Flash memory for PIC32MK and PIC32MX devices

-   It uses the Harmony 3 File System Framework to receive the application binary from a sdcard

-   It calls the bootloader\_Tasks\(\) function which receives application to be programmed into flash memory from a sdcard

-   It glows an LED once bootloader firmware is running

-   Trigger Methods

    -   It uses the On board Switch as bootloader trigger pin to force enter the bootloader at reset of device

    -   It checks for bootloader request pattern **\(0x5048434D\)** from the starting 16 Bytes of RAM to force enter bootloader at reset of device


**Test Application**

-   This is a test application which resides from

    -   The end of bootloader size in device flash memory for SAM devices

    -   The end of bootloader size in Program Flash memory for PIC32MK and PIC32MX devices

    -   The start of Program Flash memory for PIC32MZ devices

-   It will be loaded into flash memory by bootloader application

-   It blinks an LED and provides console output

-   It uses the On board Switch to trigger the bootloader from firmware

    -   Once the switch is pressed it loads first 16 bytes of RAM with bootloader request pattern **\(0x5048434D\)** and resets the device


**Development Kits**<br />The following table provides links to documentation on how to build and run SDCARD bootloader on different development kits

-   **[PIC32MZ Embedded Graphics with Stacked DRAM \(DA\) Starter Kit \(Crypto\): Building and Running the SDCARD Bootloader applications](GUID-E7B037AE-8CDD-4C80-8F07-DF4C46DB7059.md)**  

-   **[SAM E54 Xplained Pro Evaluation Kit: Building and Running the SDCARD Bootloader applications](GUID-EF78BCAB-61FC-4F86-9ED7-18A0C467F8DF.md)**  

-   **[SAM E70 Xplained Ultra Evaluation Kit: Building and Running the SDCARD Bootloader applications](GUID-CC641FFA-6C81-4DA1-A898-2B8FEBD6995D.md)**  

-   **[SAM L22 Xplained Pro Evaluation Kit: Building and Running the SDCARD Bootloader applications](GUID-A17DB6C3-2C40-4395-9F69-5F133D54A1DC.md)**  


**Parent topic:**[MPLAB® Harmony 3 SDCARD Bootloader Application Examples](GUID-E1BC6897-8F9B-44BA-9E80-06E0A27D73BD.md)

