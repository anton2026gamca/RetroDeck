---
title: "RetroDeck"
author: "@CyberIntruder"
description: "It's a DIY game console made for emulating retro games!"
created_at: "2025-06-11"
---

This is my journey of creating the RetroDeck game console. <br>
Total hours: 8.5

## 11. 6. 2025 (4.5 hours)

Today it's the first day of making the project.

I want the console to have some compute power, maybe I will want to run more advanced games on it in the future. I already have a [Raspberry Pi CM5](https://www.raspberrypi.com/products/compute-module-5), [5 inch display](https://www.elecrow.com/rc050s-hdmi-5-inch-800x480-capacitive-touch-monitor-built-in-speaker-with-backlight-control.html?idd=6) and [PiSugar 3 Plus](https://www.pisugar.com/products/pisugar-3-plus-raspberry-pi-ups) laying around, so I've decided to use those in this project.

I want the console to have 1 HDMI port, 1 USB C port for data and 2 joysticks with 12 buttons.

Because I went with the Raspberry Pi CM5, I will need to design an IO board. I downloaded the [official raspberry pi cm5 IO board design files](https://rpltd.co/cm5io-design-files) for reference. I don't have any experience with designing PCBs yet.

![image](https://github.com/user-attachments/assets/d816617a-8c7a-458e-bbcd-6ca73103f103)

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

I also removed the SD card, because I don't need it, I don't have the CM5 Lite version. <br>
I started wiring it, but didn't finish it today.
