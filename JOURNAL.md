---
title: "RetroDeck"
author: "@CyberIntruder"
description: "It's a DIY game console made for emulating retro games!"
created_at: "2025-06-11"
---

This is my journey of creating the RetroDeck game console. <br>
Total hours: 21.25

## 11. 6. 2025 (4.5 hours)

Today it's the first day of making the project.

I want the console to have some compute power, maybe I will want to run more advanced games on it in the future. I already have a [Raspberry Pi CM5](https://www.raspberrypi.com/products/compute-module-5), [5 inch display](https://www.elecrow.com/rc050s-hdmi-5-inch-800x480-capacitive-touch-monitor-built-in-speaker-with-backlight-control.html?idd=6) and [PiSugar 3 Plus](https://www.pisugar.com/products/pisugar-3-plus-raspberry-pi-ups) laying around, so I've decided to use those in this project.

I want the console to have 1 HDMI port, 1 USB C port for data and 2 joysticks with 12 buttons.

Because I went with the Raspberry Pi CM5, I will need to design an IO board. I downloaded the [official raspberry pi cm5 IO board design files](https://rpltd.co/cm5io-design-files) for reference. I don't have any experience with designing PCBs yet.

![image](https://github.com/user-attachments/assets/0a0c9e3e-010a-425a-8ac7-4fbea0cfbc26)

I put a USB C port for charging the PiSugar. It is supposed to be like an USB C cable, though I'm not sure if it's going to work. I'll find out later.

![image](https://github.com/user-attachments/assets/ee02b9e1-235f-4121-9758-7ab1a2f0a689)

I started laying out the components. I precisely measured the distances on my 5 inch screen and drew its outline.

![Screenshot 2025-06-11 154423](https://github.com/user-attachments/assets/1abfea29-b796-4895-937e-14d929d374df)


## 12. 6. 2025 (4 hours)

I started wiring the components that I layed out yesterday. I tried to keep the board 2 layered, because more layers increase the cost. <br>
I tuned also the length of the P and N tracks of the USB and HDMI.

![image](https://github.com/user-attachments/assets/994359ac-d6c1-4e85-9a7e-8700c2efff2a)

After I almost finished, I measured the distance it will have with the PiSugar conected. <br>
Yeah, it was too long ... and I had to redesign the whole thing.

Here is the new component placement I came up with:
![image](https://github.com/user-attachments/assets/e8c3a5b9-1fc6-48b7-992f-7be9a816c550)

I also removed the SD card, because I don't need it, I don't have the CM5 Lite version.


## 13. 6. 2025 (3.75 hours)

Today I finished the wiring of the board. It was a bit harder than yesterday, but I got it. I firstly wired everything but the +5V, +3.3V and GND lines (Which was a mistake I think, because I had to put them on the inner layers due to lack of space in the outer layers).

![image](https://github.com/user-attachments/assets/9c4f00ec-2b83-44e5-a07e-a8cdc9b9a26d)

I don't really like the wiring, I might redo it some day. Also the inner layers are designed for 1 oz copper and that is another $14 at JLCPCB. <br>
I really hope this PCB is going to work.


## 16. 6. 2025 (5.5 hours)

I started to make the schematic for the built in gamepad. I want the board to be symmetrical to lower PCB manugacturing price (Each side will be the same PCB). Each board will have an ATmega32U4 and the other stuff. The 2 boards will communicate through I2C and 1 will be connected through USB to the Raspberry Pi CM5.

I downloaded the [SparkFun Pro Micro](https://github.com/sparkfun/Pro_Micro) schematic for reference, I had no clue how to wire the ATmega32U4.

![image](https://github.com/user-attachments/assets/ba31222e-6a77-42f3-8f6f-c41919fac0f7)

The PCBs will be connected through an FFC cable and to the CM5 too, but I'm not yet sure (I'll need to modify the IO board).

![image](https://github.com/user-attachments/assets/fc7935fb-7002-4a0e-a1e4-5512e2b4ca2f)
NOTE: The USB-C is there just for debugging


## 22. 6. 2025 (3)

Firstly, I changed the buttons and the joystick. I chose smaller buttons and the nintendo joycon joystick, because I like the feel of it. For the shoulder button I'll be using a special 90 degree angled button. Hope I connected the joystick right :)

![image](https://github.com/user-attachments/assets/5070bef5-bd65-4186-b249-ed6f4c4b0069)
![image](https://github.com/user-attachments/assets/285c1ecc-1bf5-4674-a960-7546252e2b8c)

I also assigned a 3d model to most components to help me later with designing the case.

![image](https://github.com/user-attachments/assets/7cea2feb-6cf8-485a-a637-c3a112a0f169)
