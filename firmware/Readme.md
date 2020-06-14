# Loading Firmware

There are two microprocessors on the EmaLink board; a ble113 module, and a cc1110. Each needs it's own firmware.

## CC1110 Firmware

For the cc1110, you should install the latest [subg_rfspy](https://github.com/sks01/subg_rfspy) firmware or the alternative [emalink_rfspy](https://github.com/sks01/EmaLink/blob/master/firmware/cc1110/cc1110_emalink_3.5.hex) for omnipod pumps. This version saves some power, your battery lifetime will increase. This version was not yet tested fully with Medtronics pumps, do not use it.

You can then use the following tools to write the firmware:

* For Windows: [cc-debugger](http://www.ti.com/tool/cc-debugger)
* For Linux: cc-tool. See [cc-tool](https://github.com/oskarpearson/mmeowlink/wiki/Firmware-install-with-CC-Tool-%28Linux%29) for instructions on installation and usage.

## BLE113 Bluetooth Module

Windows machine:
1. Install the Bluetooth Firmware Update and the Bluetooth SDK tools:
* SmartRF Studio from http://www.ti.com/tool/smartrftm-studio (Make sure to 'Extract All' if prompted at install/unzip time)
* "Bluetooth Smart Software and SDK v.1.8.0" (or above) from (https://www.silabs.com/documents/login/software/Bluegiga_ble-1.8.0-143.exe)

Note that you will need to sign up for an accounts to download both installers.

3. Go to https://github.com/sks01/emalink and click the "Clone or download" option.
4. Select "Download ZIP"
5. Extract the Zip in your download directory.
6. Double click on the Project file in the ble_firmware.
7. If you receive the message "Unable to automatically select BGBuild":
  - Click BGBuild menu item, and choose "Manually Select"
  - Choose My Computer -> C: -> Bluegiga -> blue-1.8.0-143 (or similar) -> bin -> bgbuild

## Connecting the CC Debugger to EmaLink

<Picture to be added>
