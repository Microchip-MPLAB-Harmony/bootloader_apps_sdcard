# SAM E70 Xplained Ultra Evaluation Kit: Building and Running the SDCARD Bootloader applications

**Parent topic:**[SDCARD Bootloader](GUID-E295B85B-F655-44BA-B5BF-AE328CFAD74C.md)

## Downloading and building the application

To clone or download this application from Github,go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/bootloader_apps_sdcard) and then click Clone button to clone this repo or download as zip file. This content can also be download using content manager by following [these instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki)

Path of the application within the repository is **apps/sdcard\_bootloader/**

To build the application, refer to the following table and open the project using its IDE.

### Bootloader Application

|Project Name|Description|
|------------|-----------|
|bootloader/firmware/sam\_e70\_xult.X|MPLABX Project for [SAM E70 Xplained Ultra Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/DM320113)|

### Test Application

|Project Name|Description|
|------------|-----------|
|test\_app/firmware/sam\_e70\_xult.X|MPLABX Project for [SAM E70 Xplained Ultra Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/DM320113)|

## Setting up [SAM E70 Xplained Ultra Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/DM320113)

-   Connect the Debug USB port on the board to the computer using a micro USB cable

-   Use the micro sdcard slot at the bottom of the device to insert a micro sdcard


## Running the Application

1.  Open the test application project *test\_app/firmware/sam\_e70\_xult.X* in the IDE

2.  Build the project to generate the binary **\(Do not program the binary\)**

3.  Open the bootloader project *bootloader/firmware/sam\_e70\_xult.X* in the IDE

4.  Build and program the application using the IDE

5.  **LED1** will be Turned On once programming is completed and bootloader starts running

6.  Open the Terminal application \(Ex.:Tera Term\) on the computer to get test application messages through UART once bootloaded

7.  Configure the serial port settings as follows:

    -   Baud : 115200

    -   Data : 8 Bits

    -   Parity : None

    -   Stop : 1 Bit

    -   Flow Control : None

8.  Copy the generated application binary file to a micro sdcard from the Host PC

    -   *<harmony3\_path\>/bootloader\_apps\_sdcard/apps/sdcard\_bootloader/test\_app/firmware/sam\_e70\_xult.X/dist/sam\_e70\_xult/production/sam\_e70\_xult.X.production.bin*

9.  Rename the copied application binary file to **image.bin**

10. Insert the micro sdcard with the application binary **image.bin** to the micro sdcard slot on the device

11. Once the application is successfully programmed **LED1** should start blinking and you should see below output on the console

    ![output](GUID-3069D8A1-7C9E-483C-8ACD-2CB83302DE3D-low.png)

12. Remove the micro sdcard from the sdcard slot

13. Press and hold the Switch **SW0** to trigger Bootloader from test application and you should see below output

    ![output](GUID-1E0923BA-91D0-40D1-B646-6C1172C12DF1-low.png)

14. Repeat Steps 10-12 once and jump to Step-15

    -   This step is to verify that bootloader is running after triggering bootloader from test application in Step 13

15. **Press and hold** the Switch **SW0** and then press Reset button or Power cycle the device to force trigger bootloader at startup

16. Repeat Steps 10-12 once

    -   This step is to verify whether bootloader is triggered by switch press at reset


## Additional Steps \(Optional\)

-   To bootload any other application refer to [Application Configurations](GUID-641ADB02-676E-4999-B96D-44F018028A43.md)

-   Once done repeat the applicable steps mentioned in [Running The Application](#running-the-application)


