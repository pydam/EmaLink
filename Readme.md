# EmaLink

A device that bridges the communication between Loop software application and Omnipod and Medtronic insulin pumps. This is a fork from RileyLink, focusing on reducing size of the device, improving communication range and extending battery life. Also, you can charge EmaLink with any micro USB charger - much broader available vs. the mini port USB used by RileyLink.

### Turning on
Use a nail, a small plastic or a wood bit to move the power switch towards the USB port. When EmaLink is powered on, you should see a red and a green LED turning on for 1 second.

### Connecting EmaLink to Loop/FreeAPS/AndroidAPS
Please follow the instructions provided by each application for connecting to EmaLink, the procedure is the same as for RileyLink, just the name of the device will be EmaLink.Once EmaLink is connected to Loop/FreeAPS/AndroidAPS, a green led will start blinking every 3 seconds on EmaLink.

### Charging

Once the battery gets almost depleted, a red led will start blinking every 3 seconds.
To charge it, you can use any micro USB charger from a phone, tablet, headset or another device. You can even use a power bank to charge it if it has a micro USB cable. Charging is considered finished after the red led (the one close to the USB connector) is turned off. It may take up to 3 hours for Nano.
For QI versions, charging can be also done with any QI compatible charge. Place EmaLink with the coil (you can see a round, copper coil, through the case) down on the middle of the QI charger and check that a red led is lighting from the top of the EmaLink. Once charging is completed, you should remove EmaLink from the charger as the charger reduces communication range.
Charging can be done every few days until EmaLink is fully charged (the red led turned off) or for a few minutes every day, depending on your schedule. Overnight charging also works well with a Micro USB charge but avoid leaving QI versions on the QI charger overnight as this reduced communication range and may generate red loops.

### LED Lights 

There are 3 leds on the back of the device: a red one, close to the micro USB charging port, and a red + green cluster on the other side. First, turn the EmaLink on by flipping the switch located next to the micro USB port. After you switch-on EmaLink, the red + green cluster will light-up for 1 second. When you connect EmaLink to AAPS on Loop over bluetooth, the green led will start blinking every 3 seconds. The green led will stop blinking once battery is almost depleted. The red led will start blinking once battery is almost depleted, you should consider charging it in the next few hours.

### Case

I have designed a new case to be 3D printed with TPU material. TPU is a flexbile material that cannot be shattered, this makes EmaLink
drop proof. There are several case styles to chose from, pick the one that makes most sense for your needs.

### Hardware

See the [hardware](https://github.com/sks01/emalink/tree/master/hardware) directory for design files to build it. The hardware design is released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).  

### Firmware

The code in the [firmware](https://github.com/sks01/emalink/tree/master/firmware) directory runs on the hardware.  There are two main chips and thus two firmware images.
Check the "EmaLink 3_7 3_8 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.7, 3.8 or 3.9.

Check the "EmaLink 3_2 3_3 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.2 or 3.3. You can use breadboard wires also but you may need to keep them at an angle while flashing as the PCB holes are slightly bigger.

Check the "EmaLink%204_4%20-%20firmware%20update%20guide.pdf" if you would like to understand how you can update the firmware for EmaLink with PCB version 4.x. 

### License

The MIT License (MIT)

Copyright (c) 2015 Pete Schwamb

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
