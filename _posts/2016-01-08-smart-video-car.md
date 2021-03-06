---
layout: post
title:  Sunfounder Smart Video Robot Car Kit for Raspberry Pi
meta:   August 01, 2016
author: Juan Pablo Soto
---
This is a short blog about the troubleshooting process we had to face when
assembling and configuring the Car kit with the Raspberry Pi. We hope it can be useful for everyone, specially for those who are doing it alone and with a limited knowledge of how
the raspberry pi works.

### Batteries

When we first started reading the manual to get an idea of how to start assembling the Car, we soon realized that the batteries required to power the Car were not included in the package.

Please be aware of this before purchasing the kit, so make sure you do buy the batteries which are (x2) 18650 of 3.7v rechargeable Li-on according to the manual. It will save you a lot of time and headaches.

There is another thing worth mentioning, since we did not have the required batteries, we had to come up with a workaround to solve the power issue. So, we did a little research on the voltage regulator included in the power board and found out that we were actually able to use another kind of battery to power it. The voltage regulator is a: **XL1509** which is a **2A 150KHz 40V Buck DC to DC Converter**, so based on that we were able to power the car with a 4 cells **14.8v 1000mAh** Li-Po battery (under our own risk) without any problems.

### Copper Standoffs

Please be extremely careful when placing the M2.5*8 Copper Standoffs on the acrylic (Upper) plate. This is because the plate can be broken easily if too much force is applied. 

Make sure you take your time when assembling this part. 

### Copper Standoffs Screws

<img src="{{ site.baseurl }}/assets/wrong_screws.png" alt="circuit">

Unfortunately, we got the wrong 4 M3*8 when it was time to assemble this section. We had to come up with a workaround for this section by using a different set of screws. Please make sure to try the screws first before assembling the Copper Standoffs, this can save you a lot of time.

### Client and Server scripts

Please make sure to download the latest version of the repository code [here](https://github.com/sunfounder/Sunfounder_Smart_Video_Car_Kit_for_RaspberryPi).

### Calibration Configuration

Once you have come to this step, you will need to calibrate properly the Car by following the calibration menu.

## Conclusion

We hope the above information can be useful to you when configuring your own Car kit.

In the next blog we will be talking about how to assemble and configure the Raspberry Pi from scratch. Also, we will be creating a basic first script to print information on the console. 

In the below links you can find useful information about the Car kit:

[Github Repo](https://github.com/sunfounder/Sunfounder_Smart_Video_Car_Kit_for_RaspberryPi)

[Manual](https://www.sunfounder.com/learn/category/Smart-Video-Car-for-Raspberry-Pi.html)

[Components](https://www.sunfounder.com/blog/A-Car-Robot-with-Video-Transmission/)

[Tutorial Videos](https://www.youtube.com/watch?v=Tg_g4YoAZdc)

[SunFounder](https://www.sunfounder.com)
  
