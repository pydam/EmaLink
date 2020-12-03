# EmaLink

A device that bridges the communication between Loop software application and Omnipod and Medtronic insulin pumps. This is a fork from RileyLink, focusing on reducing size of the device, improving communication range and extending battery life. Also, you can charge EmaLink with any micro USB charger - much broader available vs. the mini port USB used by RileyLink.

### Charging

You can use any micro USB charges from a phone, tablet, headset or other devices. You can even use a powerbank to charge it if it has a micro USB cable. 
Charging is considered finished after the red led (the one close to the USB connector) is turning off. It may take up to 3 hours for 3XS or XS to fully charge, up to 4 hours for Medium and up to 5 hours for Maxx.


### LED Lights

There are 3 leds on the back of the device: a red one, close to the micro USB charing port, and a red + green cluster on the other side. 
When you switch-on EmaLink, the red + green cluster will light-up for 1 second. 
When you connect EmaLink to AAPS on Loop over bluetooth, the green led will start blinking every 1.5 seconds. The green led will stop blinking once battery is almost depleted.
The red led will start blinking once battery is almost depleted, you should consider charging it in the next few hours.

### Case

I have designed a new case to be 3D printed with TPU material. TPU is a flexbile material that cannot be shattered, this makes EmaLink
drop proof. You will still break it if you step on it ...

As of Oct 2020, the following EmaLink versions are available:

**EmaLink Medtronic Maxx** (PCB: 3.8/3.9, Battery 1050mAh)
* Size: 55x40x21 mm, oval design [Tinkercad](https://www.tinkercad.com/things/aMPzEObGEE7)
* Weight: 34g
* Battery life:
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 4 days (due to MySentry feature, EmaLink uses much more power, which impacts the battery life)
    * Loop/FreeAPS with other Medtronic pumps - 9+ days
    * AndroidAPS with Medtronic pumps: 9+ days
    * Not available for Omnipod

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Maxx.png)

**EmaLink Medium** (PCB: 3.7/3.8/3.9, Battery: 550mAh)
*	Size: 43x40x18mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/3494lPR24DK)
*	Weight: 24g
*	Battery life: 
    *	Loop/FreeAPS with Omnipod pod: 7-8 days
    *	Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 2 days (due to MySentry feature, EmaLink uses much more power, which impacts the battery life)
    *	Loop/FreeAPS with other Medtronic pumps: 5-6 days
    * AndroidAPS with Omnipod pods: 7-8 days
    *	AndroidAPS with Medtronic pumps: 3 days

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Medium.png)

**EmaLink XS** (PCB: 3.7/3.8/3.9, Battery: 310mAh) 
*	Size: 42x40x15mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/bysJBdyaAnK)
*	Weight: 23g
*	Battery life: 
    * Loop/FreeAPS with Omnipod pod: 4 days
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 1 day (due to MySentry feature, EmaLink uses much more power, which impacts the battery life)
    * Loop/FreeAPS with other Medtronic pumps: 3 days
    * AndroidAPS with Omnipod pods: 4 days
    * AndroidAPS with Medtronic pumps: 2 days

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/XS.png)

**EmaLink 3XS** (PCB: 3.9, Battery: 250mAh) 
*	Size: 42x40x11mm, square [Tinkercad](https://www.tinkercad.com/things/354TEb6AY1d)
*	Weight: 21g
*	Battery life: 
    * Loop/FreeAPS with Omnipod pod: 3 days
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 16-18 hours (due to MySentry feature, EmaLink uses much more power, which impacts the battery life)
    * Loop/FreeAPS with other Medtronic pumps: 2.5 days
    * AndroidAPS with Omnipod pods: 3 days
    * AndroidAPS with Medtronic pumps: 1.5 days

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/3XS.png)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Medium_XS_3XS.png)

### Hardware

See the [hardware](https://github.com/sks01/emalink/tree/master/hardware) directory for design files to build it. The hardware design is released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).  

![PCB_top_Omnipod](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_top_Omnipod.png)
![PCB_top_Medtronic](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_top_Medtronic.png)
![PCB_back](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_back.png)

### Firmware

The code in the [firmware](https://github.com/sks01/emalink/tree/master/firmware) directory runs on the hardware.  There are two main chips and thus two firmware images.
Check the "EmaLink 3_7 3_8 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.7, 3.8 or 3.9.

Check the "EmaLink 3_2 3_3 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.2 or 3.3. You can use breadboard wires also but you may need to keep them at an angle while flashing as the PCB holes are slightly bigger.

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
