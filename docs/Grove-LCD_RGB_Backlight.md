---
title: Grove - LCD RGB Backlight
category: Display
bzurl: https://www.seeedstudio.com/Grove-LCD-RGB-Backlight-p-1643.html
oldwikiname: Grove_-_LCD_RGB_Backlight
prodimagename: intro.jpg
surveyurl: https://www.surveymonkey.com/r/LCD_Backlight
sku: 104030001
---

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/intro.jpg)

Done with tedious mono color backlight? This Grove enables you to set the color to whatever you like via
the simple and concise Grove interface. It takes I2C as communication method with your microcontroller.
So number of pins required for data exchange and backlight control shrinks from ~10 to 2, relieving IOs for
other challenging tasks. Besides, Grove - LCD RGB Backlight supports user-defined characters. Want to get
a love heart or some other foreign characters? Just take advantage of this feature and design it!
This product is a replacement of Grove - Serial LCD. If you are looking for primitive 16x2 LCD modules, we
have green yellow backlight version and blue backlight version on sale also.

<p style="text-align:center"><a href="http://www.seeedstudio.com/Grove-LCD-RGB-Backlight-p-1643.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>


!!!Note
    This document works for Grove-LCD RGB Backlight Version 1.0, 2.0 and 4.0.

## Version

| Product Version              | Changes                                   | Released Date |
|------------------------------|-------------------------------------------|---------------|
| Grove-LCD RGB Backlight V1.0 | Initial                                   | June 2012     |
| Grove-LCD RGB Backlight V2.0 | Optimize PCB layout                       | Nov 2013     |
| Grove-LCD RGB Backlight V4.0 | Optimize PCB layout                       | Sep 2016     |

## Features

* RGB Backlight
* I2C communication
* Built-in English fonts
* 16x2 LCD

!!!Tip
    More details about Grove modules please refer to [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Specification

|Item|Value|
|------|----------|
| Input Voltage|5V|
| Operating Current | <60mA |
|CGROM | 10880 bit |
| CGRAM | 64x8 bit |
| LCD I2C Address | 0X3E |
| RGB I2C Address | 0X62 |


!!!Note
    There are 4 I2C addresses and we use 2 I2C addresses for LCD and RGB.

## Platforms Supported

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Caution
    The platforms mentioned above as supported is/are an indication of the module's hardware or theoritical compatibility. We only provide software library or code examples for Arduino platform in most cases. It is not possible to provide software library / demo code for all possible MCU platforms. Hence, users have to write their own software library.

## Application Ideas

* Human Machine Interface
* Smart House
* Sensor Hub

Here are some projects for your reference.

|Edison Wi-Fi Address|WiFi Enabled Greenhouse|Grove Lucky Dumpling|
|------------------------|-------------------|--------------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project2.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project3.jpg)|
|[Make it Now!](http://www.instructables.com/id/Show-the-Intel-Edison-WiFi-IP-Address-on-a-Grove-L/)|[Make it Now!](http://www.instructables.com/id/Arduino-Grove-Greenhouse/)|[Make it Now!](http://www.instructables.com/id/Grove-Lucky-Dumpling/)|


|Toothbrushing Instructor|LinkIt ONE Pager|LinkIt ONE IoT Demo|
|------------------------|-------------------|--------------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project5.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LCD_RGB_Backlight/master/images/project6.jpg)|
|[Make it Now!](http://www.instructables.com/id/Toothbrushing-Instructor/)|[Make it Now!](http://www.instructables.com/id/LinkIt-ONE-Pager/)|[Make it Now!](https://community.seeedstudio.com/project_detail.html?id=78)|


## Getting Started

!!!Note
    If this is the first time you work with Arduino, we firmly recommend you to see [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.


### Play With Arduino

**Hardware**


- **Step 1.** Prepare the below stuffs:

| Seeeduino V4.2 | Base Shield|  Grove-LCD RGB Backlight |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight/raw/master/img/rgb.jpg)|
|[Get One Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get One Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Get One Now](http://www.seeedstudio.com/Grove-LCD-RGB-Backlight-p-1643.html)|

- **Step 2.** Connect Grove-LCD RGB Backlight to **I2C** port of Grove-Base Shield.
- **Step 3.** Plug Grove - Base Shield into Seeeduino.
- **Step 4.** Connect Seeeduino to PC via a USB cable.

![](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight/raw/master/img/seeeduino_rgb.jpg)

!!!Note
	If we don't have Grove Base Shield, We also can directly connect Grove-LCD RGB Backlight to Seeeduino as below.

| Seeeduino       | Grove-LCD RGB Backlight |
|---------------|-------------------------|
| 5V            | Red                     |
| GND           | Black                   |
| SDA           | White                   |
| SCL           | Yellow                  |

**Software**

- **Step 1.** Download the  [ Grove-LCD RGB Backlight Library](https://github.com/Seeed-Studio/Grove_LCD_RGB_Backlight/archive/master.zip)  from Github.
- **Step 2.** Refer [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) to install library for Arduino.
- **Step 3.** Here are 12 examples in the library as below. 

    - Autoscroll
    - Blink
    - Cursor
    - CustomCharacter
    - Display
    - fade
    - HelloWorld
    - Scroll
    - SerialDisplay
    - setColor
    - setCursor
    - TextDirection

- **Step 4.** Please follow below picture to select example **HelloWorld** and upload the arduino. If you do not know how to upload the code, please check [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

![](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight/raw/master/img/example.jpg)

Here is the code of HelloWorld.ino.

```c++
    #include <rgb_lcd.h>

    rgb_lcd lcd;

    void setup() {
      lcd.begin(16, 2);

      lcd.print("Hello, World!");
    }

    void loop() {
    }
```

- **Step 4.** We will see the "Hello, World!" on the LCD.

### Play With Raspberry Pi

**Hardware**

- **Step 1.** Prepare the below stuffs:

| Raspberry pi | GrovePi_Plus | Grove-LCD RGB Backlight |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight/raw/master/img/rgb.jpg)|
|[Get One Now](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Get One Now](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Get One Now](http://www.seeedstudio.com/Grove-LCD-RGB-Backlight-p-1643.html)|


- **Step 2.** Plug the GrovePi_Plus into Raspberry.
- **Step 3.** Connect Grove-LCD RGB Backlight to **I2C** port of GrovePi_Plus.
- **Step 4.** Connect the Raspberry to PC through USB cable.

![](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight/raw/master/img/rpi_rgb.jpg)

**Software**

- **Step 1.** Follow [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) to configure the development environment.
- **Step 2.** Git clone the Github repository.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Step 3.** Excute below commands to use the Grove-LCD RGB Backlight to display.


```python
cd ~/GrovePi/Software/Python/grove_rgb_lcd
python grove_rgb_lcd.py
```

Here is the grove_rgb_lcd.py code.

```python
    import smbus
    import time

    # I2C addresses

    LCD_ADDRESS = 0x3e
    RGB_ADDRESS = 0x62

    # Commands

    LCD_CLEARDISPLAY = 0x01
    LCD_DISPLAYCONTROL = 0x08
    LCD_ENTRYMODESET = 0x04
    LCD_FUNCTIONSET = 0x20
    LCD_SETCGRAMADDR = 0x40
    LCD_SETDDRAMADDR = 0x80

    # Flags

    LCD_2LINE = 0x08

    LCD_DISPLAYON = 0x04
    LCD_CURSOROFF = 0x00
    LCD_BLINKOFF = 0x00

    LCD_ENTRYLEFT = 0x02
    LCD_ENTRYSHIFTDECREMENT = 0x00

    # Registers

    REG_MODE1 = 0x00 # backlight on
    REG_MODE2 = 0x01 # control LEDs by PWM registers
    REG_OUTPUT = 0x08 # blinky mode

    REG_RED = 0x04 # PWM2
    REG_GREEN = 0x03 # PWM1
    REG_BLUE = 0x02 # PWM0

    # The next block is equivalent to the "begin" call in the Arduino library

    time.sleep(.05)

    bus = smbus.SMBus(1)

    bus.write_byte_data(LCD_ADDRESS, LCD_SETDDRAMADDR, LCD_FUNCTIONSET | LCD_2LINE)

    time.sleep(.0045)

    bus.write_byte_data(LCD_ADDRESS, LCD_SETDDRAMADDR, LCD_DISPLAYCONTROL | LCD_DISPLAYON | LCD_CURSOROFF | LCD_BLINKOFF)

    bus.write_byte_data(LCD_ADDRESS, LCD_SETDDRAMADDR, LCD_CLEARDISPLAY)

    time.sleep(.002)

    bus.write_byte_data(LCD_ADDRESS, LCD_SETDDRAMADDR, LCD_ENTRYMODESET | LCD_ENTRYLEFT | LCD_ENTRYSHIFTDECREMENT)

    bus.write_byte_data(RGB_ADDRESS, REG_MODE1, 0)
    bus.write_byte_data(RGB_ADDRESS, REG_OUTPUT, 0xFF)
    bus.write_byte_data(RGB_ADDRESS, REG_MODE2, 0x20)

    # Set color to white
    bus.write_byte_data(RGB_ADDRESS, REG_RED, 255)
    bus.write_byte_data(RGB_ADDRESS, REG_GREEN, 255)
    bus.write_byte_data(RGB_ADDRESS, REG_BLUE, 255)

    # The next line is equivalent to the "print" call in the Arduino library

    bus.write_i2c_block_data(LCD_ADDRESS, LCD_SETCGRAMADDR, list('Hello, World!'.encode()))
```

- **Step 4.** We will see the Grove-LCD RGB Backlight display as Going to sleep in 1...

## FAQ

- Q1: How to use multiple Grove-LCD RGB Backlight? 
    - A1: Please refer to [Arduino Software I2C user guide](http://wiki.seeedstudio.com/Arduino_Software_I2C_user_guide/).

## Resources

- **[Library]** [Software Library](https://github.com/Seeed-Studio/Grove_LCD_RGB_Backlight/archive/master.zip)
- **[Document]** [Github page for this document](https://github.com/SeeedDocument/Grove_LCD_RGB_Backlight)

## Projects

**Particle + Grove LCD RGB Backlight = Realtime Clock**: Connect Grove LCD RGB Backlight to Particle using I2C to display time.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/peacemoon/particle-grove-lcd-rgb-backlight-realtime-clock-42151f/embed' width='350'></iframe>

**LCD RGB Grove module**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/yniND_abVos" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/tbdTTC3Jmgk" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/).
