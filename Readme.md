# EmaLink

A device that bridges the communication between Loop software application and Omnipod and Medtronic insulin pumps. This is a fork from RileyLink, focusing on reducing size of the device, improving communication range and extending battery life. Also, you can charge EmaLink with any micro USB charger - much broader available vs. the mini port USB used by RileyLink.

### Charging

You can use any micro USB charges from a phone, tablet, headset or other devices. You can even use a powerbank to charge it if it has a micro USB cable. 
Charging is considered finished after the red led (the one close to the USB connector) is turning off. It may take up to 3 hours for Nano or Micro to fully charge, up to 5 hours for Standard or Maxx.

### LED Lights

There are 3 leds on the back of the device: a red one, close to the micro USB charing port, and a red + green cluster on the other side. 
When you switch-on EmaLink, the red + green cluster will light-up for 1 second. 
When you connect EmaLink to AAPS on Loop over bluetooth, the green led will start blinking every 3 seconds. The green led will stop blinking once battery is almost depleted.
The red led will start blinking once battery is almost depleted, you should consider charging it in the next few hours.

### Case

I have designed a new case to be 3D printed with TPU material. TPU is a flexbile material that cannot be shattered, this makes EmaLink
drop proof. There are several case styles to chose from, pick the one that makes most sense for your needs.

Chosing the right case:
* "I keep EmaLink with me most time, the smaller - the better" - Nano is the way to go
* "Having the best range while keeping a small size is important to me" - Micro is the perfect fit
* "Give me a product that has great range, can be charged once per week and can survive through drops and splashes" - Standard fits the bill
* "I keep forgeting to charge devices, can I have the biggest battery?" - Go for Maxx 

As of Mar 2021, the following EmaLink versions are available:

**Now thinner and splash-proof! EmaLink Maxx** (PCB: 4.x, Battery 850mAh)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/NewMaxx.png)
* Size: 55x40x17 mm, oval design with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/2sOWkvGTfb7)
* Weight: 38g
* Battery life:
    *	Loop/FreeAPS with Omnipod pod: 30 days
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 4 days (due to MySentry feature, EmaLink uses much more power, which impacts the battery life); With MySentry disabled, battery life increases to 18 days
    * Loop/FreeAPS with other Medtronic pumps - 18 days
    * AndroidAPS with Omnipod pods: 18 days
    * AndroidAPS with Medtronic pumps: 14 days

**EmaLink Standard** (PCB: 4.x, Battery: 500mAh)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Medium.png)
*  Size: 43x40x18mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/3494lPR24DK)
*	Weight: 24g
*	Battery life: 
    *	Loop/FreeAPS with Omnipod pod: 17 days
    *	Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 2 days (due to MySentry feature, EmaLink uses much more power, which impacts the battery life); With MySentry disabled, battery life increases to 10 days
    *	Loop/FreeAPS with other Medtronic pumps: 10 days
    * AndroidAPS with Omnipod pods: 17 days
    *	AndroidAPS with Medtronic pumps: 7 days

**EmaLink Micro** (PCB: 4.x, Battery: 250mAh) 
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Micro.png)
*	This is the smallest version of EmaLink optimized for use away from your body. If you cary EmaLink with you most time, go for Nano. If you have a mixed usage, try Standard.
*  Size: 43x41x12mm, dustproof, splash resistant, square [Tinkercad](https://www.tinkercad.com/things/kaO3JdWCOXo)
*	Weight: 20g
*	Battery life: 
    * Loop/FreeAPS with Omnipod pod: 7 days
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 16-18 hours (due to MySentry feature, EmaLink uses much more power, which impacts the battery life); With MySentry disabled, battery life increases to 5 days
    * Loop/FreeAPS with other Medtronic pumps: 5 days
    * AndroidAPS with Omnipod pods: 7 days
    * AndroidAPS with Medtronic pumps: 3 days
    
**EmaLink Nano** (PCB: 5.x, Battery: 250mAh)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Nano.png)
*	This is the smallest version of EmaLink, specially made to be used as a necklace. The antenna was optimized for keeping it close to your body. It still have a good range while kept around you (nightstand, desk) but for maximum range you should opt for Standard or Micro. [Tinkercad](https://www.tinkercad.com/things/bE5cdci4nX8)
*  Size: 41x31x12mm dustproof, splash resistant
*	Weight: 18g
*	Battery life: 
    * Loop/FreeAPS with Omnipod pod: 7 days
    * Loop/FreeAPS with Medtronic 523, 554, 723 or 754 pumps  - 16-18 hours (due to MySentry feature, EmaLink uses much more power, which impacts the battery life); With MySentry disabled, battery life increases to 5 days
    * Loop/FreeAPS with other Medtronic pumps: 5 days
    * AndroidAPS with Omnipod pods: 7 days
    * AndroidAPS with Medtronic pumps: 3 days

![versions](https://github.com/sks01/EmaLink/blob/master/pictures/Compare1.png)
![versions](https://github.com/sks01/EmaLink/blob/master/pictures/Compare2.png)
![versions](https://github.com/sks01/EmaLink/blob/master/pictures/Compare3.png)

### Hardware

See the [hardware](https://github.com/sks01/emalink/tree/master/hardware) directory for design files to build it. The hardware design is released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).  

![PCB_v4.0](https://github.com/sks01/EmaLink/blob/master/pictures/EL_PCB_v4.0.png)
![PCB_v5.0](https://github.com/sks01/EmaLink/blob/master/pictures/Nano_PCB.png)

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
