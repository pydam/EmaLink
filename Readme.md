# EmaLink

A device that bridges the communication between Loop software application and Omnipod and Medtronic insulin pumps. This is a fork from RileyLink, focusing on reducing size of the device, improving communication range and extending battery life. Also, you can charge EmaLink with any micro USB charger - much broader available vs. the mini port USB used by RileyLink.
Currently, a battery lifetime of 72-110 hours is expected with Loop and an Omnipod pump. For Medtronic pumps, battery lifetime is expected to be over 48 hours, depending heavily on the application used and its settings.

![Connected to Omnipod](https://github.com/sks01/EmaLink/blob/master/pictures/Omnipod_conn.jpeg)

![Connected to Medtronic](https://github.com/sks01/EmaLink/blob/master/pictures/Medtronic_conn.jpeg)

### Case

I have designed a new case to be 3D printed with TPU material. TPU is a flexbile material that cannot be shattered, this makes EmaLink
drop proof. You will still break it if you step on it ...

![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Charging.png)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Top_case.png)
![Case](https://github.com/sks01/EmaLink/blob/master/pictures/Back_case.png)

You can see and edit the design in here: [Tinkercad](https://www.tinkercad.com/things/6nLdgedEDKC-emalinkcasetpu)

This case is 20x40x51 vs. the RileyLink SlimCase for Omnipod which is 34x16x72mm.

![Size_comparison](https://github.com/sks01/EmaLink/blob/master/pictures/EmaLink_vs_SlimCase.PNG)

### Hardware

See the [hardware](https://github.com/sks01/emalink/tree/master/hardware) directory for design files to build it. The hardware design is released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).  

![PCB_top](https://github.com/sks01/EmaLink/blob/master/pictures/Top_3.2.1.png)
![PCB_bottom](https://github.com/sks01/EmaLink/blob/master/pictures/Bottom_3.2.1.png)

### Firmware

The code in the [firmware](https://github.com/sks01/emalink/tree/master/firmware) directory runs on the hardware.  There are two main chips and thus two firmware images.

### LED Lights

There are 3 leds on the back of the device: one orange, one red and the last one green. The green led blinks every second while the module is connected over BLE and the battery in charged above 20%. The red led indicate battery status: one will start blinking every second once the battery drops below 20%. The orange led will turn on once you connect the charger. Once the battery is fully charged, the orange led will turn off, blinking every minute or so while the charger is connected. 

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
