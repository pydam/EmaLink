# EmaLink

A device that bridges the communication between Loop software application and Omnipod and Medtronic insulin pumps. This is a fork from RileyLink, focusing on reducing size of the device, improving communication range and extending battery life. Also, you can charge EmaLink with any micro USB charger - much broader available vs. the mini port USB used by RileyLink.

### Case

I have designed a new case to be 3D printed with TPU material. TPU is a flexbile material that cannot be shattered, this makes EmaLink
drop proof. You will still break it if you step on it ...

As of July 2020, the following EmaLink versions are known to exist:

**EmaLink Medtronic Maxx** (PCB: 3.8, Battery 1050mAh)
•	Size: 55x40x21 mm, oval design [Tinkercad](https://www.tinkercad.com/things/aMPzEObGEE7)
•	Weight: 34g
•	Battery life: 
  o	 Loop / FreeAPS with Medtronic pump - 11 days (estimated, to be confirmed)
  o	 AndroidAPS with Medtronic pums - 5 days (estimated, to be confirmed)
•	Not available for Omnipod, the 433Mhz antenna would not fit nicely in this case design 

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Maxx.png)

**(to be retired)EmaLink Classic** (PCB: 3.2/3.3, Battery: 400-500mAh)
•	Size: 56x40x22mm, oval design [Tinkercad](https://www.tinkercad.com/things/86kA2tHxB7g)
•	Weight: 26g
•	Battery life: 
  o	 Loop / FreeAPS with Omnipod pod: 5-7 days (confirmed)
  o	 Loop / FreeAPS with Medtronic pump: 3.5-5 days (confirmed)
  o	 AndroidAPS with Medtronic pums: 2.5-3 days (confirmed)
  
 ![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Classic_3_2.png)

**EmaLink Classic** (PCB: 3.7/3.8, Battery: 500mAh)
•	Size: 49x40x20mm, oval design [Tinkercad](https://www.tinkercad.com/things/7E4MjrtWril)
•	Weight: 24g
•	Battery life: 
  o	 Loop / FreeAPS with Omnipod pod: 6.5-7 days (confirmed)
  o	 Loop / FreeAPS with Medtronic pump: 4.5-5 days (estimated, to be confirmed)
  o	 AndroidAPS with Medtronic pums: 3 days (estimated, to be confirmed)
  
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Classic_3_7.png)

**EmaLink Medium** (PCB: 3.7/3.8, Battery: 500mAh)
•	Size: 45x40x19mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/9jWhSiQkAbo)
•	Weight: 24g
•	Battery life: same as for Classic

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Medium.png)

**EmaLink NeoClassic** (PCB: 3.7/3.8, Battery: 500mAh)
•	Size: 45x40x19mm, flatten oval [Tinkercad](https://www.tinkercad.com/things/3WlRqooTBQr)
•	Weight: 25g
•	Battery life: same as for Classic

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/NeoClassic.png)

**EmaLink Omnipod XS** (PCB: 3.7/3.8, Battery: 250mAh) 
•	Size: 43x40x16mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/0KXGFfexw8S)
•	Weight: 23g
•	Battery life: 
  o	 Loop / FreeAPS with Omnipod pod: 3-3.5 days (estimated, to be confirmed)

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/XS.png)

**EmaLink Medtronic XXS** (PCB: 3.7/3.8, Battery: 250mAh) 
•	Size: 43x40x14mm, square with 2 caps, dustproof, splash resistant [Tinkercad](https://www.tinkercad.com/things/fs7lsaBEtP7)
•	Weight: 22g
•	Battery life: 
  o	 Loop / FreeAPS with Medtronic pump: 2.5-3days (confirmed)
  o	 AndroidAPS with Medtronic pums: 1.5 days (estimated, to be confirmed)

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/XXS.png)

### Hardware

See the [hardware](https://github.com/sks01/emalink/tree/master/hardware) directory for design files to build it. The hardware design is released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).  

![PCB_top_Omnipod](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_top_Omnipod.png)
![PCB_top_Medtronic](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_top_Medtronic.png)
![PCB_back](https://github.com/sks01/EmaLink/blob/master/pictures/PCB_back.png)

### Firmware

The code in the [firmware](https://github.com/sks01/emalink/tree/master/firmware) directory runs on the hardware.  There are two main chips and thus two firmware images.
Check the "EmaLink 3_7 3_8 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.7 or 3.8.
Check the "EmaLink 3_2 3_3 - firmware update guide.docx" if you would like to understand how you can update the firmware for EmaLink with PCB version 3.2 or 3.3. You can use breadboard wires also but you may need to keep them at an angle while flashing as the PCB holes are slightly bigger.

### LED Lights

There are 3 leds on the back of the device: one orange, one red and the last one green. The green led blinks every 1-1.5 seconds while the module is connected over BLE and the battery in charged above 20%. The red led indicate battery status: one will start blinking battery drops below 12h of remaining lifetime. The orange led will turn on once you connect the charger. Once the battery is fully charged, the orange led will turn off, blinking every minute or so while the charger is connected. 

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
