*  BLE firmware version 3.13 version works only with CC1110 2.2.21 firmware. Also, PCB version v4.0 or above is needed fo these firmware versions.
*  BLE firmware version 3.11 version works only with CC1110 2.2.19 firmware

The BLE firmware needs to be be unpacked and adjusted to offer best battery charge indication.

You will need to adjust 2 areas:
*  in file main.bgs, go through the sections that start with "#look-up table for..." and uncomment the one that seems to be for your battery. Contact the author if you don't manage to identify the right one based on the battery your EmaLink has. If you select another section versus the one selected by default, make sure to unselect the default section or you will get compilation errors.
*  in file main.bgs, search for "const voltage_adj =". You will need to replace the value 1000 with the value that is specific to your EmaLink. You can use the value noted in a corner of the EmaLink PCB, a value in between 970 and 1030. Or, execute the procedure below in case that value is not visible anymore.
*  measure current battery voltage with a multimeter. If the value is above 4.17v, you need to use EmaLink until the voltage drops a bit.
*  check the voltage as reported by EmaLink; to get the voltage from EmaLink, you need to connect to EmaLink with some BLE tool (I use BLE Scanner) and read the "BATTERY VOLTAGE" customer Characteristic, under the CUSTOM SERVICE offered by EmaLink. This is shown as a 16bit hex number. Convert it to decimal and divide by 100 to see the battery voltage (for ex., 0x0170 = 3.68v)
*  Once you have them both, calculate the factor as [measured battery voltage]/[reported battery voltage]1000. So if you have measured 4.16v while EmaLink reports 4.12v, you need a factor of 4.16/4.121000 = 1009. Edit main.bgs file to have "const voltage_adj = 1009" and flash again the firmware on BLE chip. 
*  Repeat the cycle, until the [measured battery voltage]=[reported battery voltage]
