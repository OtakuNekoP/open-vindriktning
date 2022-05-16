# open-vindriktning

Open-Vindriktning is a modification kit for Ikea Vindriktning PM2.5 sensor including open source PCB design and firmware.

<img src="https://cdn-image.wenzelu.com/2022/05/16/PCB1-render.png" style="zoom:40%;" />



## Description
Open-Vindriktning uses ESP8266 as MCU to provide serial, TWI, ADC and Wi-Fi support for Ikea Vindriktning. 

![](https://cdn-image.wenzelu.com/2022/05/16/Sch_2022-05-16_12-09-27.png)



## Making

There is a verified and actually produced Gerber file in the Release of this repo. You can send it to any PCB prototype manufacturer, such as JLCPCB and PCBWay etc., to get your open-vindriktning PCB. And Open-Vindriktning is double side 2-layer design, so it's very cheap for ordering. BOM has also been included. All components can be ordered from LCSC.

<img src="https://cdn-image.wenzelu.com/2022/05/16/P1070798.jpg" style="zoom: 20%;" />



## Firmware

Of course you can write firmware by yourself. 

Here is a recommended open source firmware written by my dear friend @amefs .

https://github.com/amefs/open-vindriktning-firmware

This fw supports Web Portal, MQTT and Home Assistant etc.



## Installation

The 3D mechanical size design of the PCB is fully compatible with the original black PCB. Can be dropped directly into the unmodified IKEA Vindriktning enclosure. Don't forget to connect two cables of PM1006K PM2.5 sensor.

You can also connect extra SPI, I2C, UART or 1-Wire sensors to TWI extension port on board. It provides 3.3V power supply, and the maximum power supply capacity of 3.3V rail is 2A, include ESP8266.



## Flashing

Auto reset and flash circuit has been designed in Open-Vindriktning. So you can connect Open-Vindriktning to your PC via USB Type-C cable directly. Open-Vindriktning will be recognized as a CP2102 serial port device. 

You can flash firmware with Arduino IDE or ESP flash tools as your wish. After firmware flashing it will automatic reset it self. But I still recommend unplug the USB cable and replug for a cold start avoid any PM1006K malfunction.



## Usage
Depends on firmware.



## Authors and acknowledgment
Thanks to @amefs for writing firmware for Open-Vindriktning and participating in hardware testing and giving valuable suggestions for hardware optimization. 



## License
MIT
