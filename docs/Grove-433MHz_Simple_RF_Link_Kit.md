---
title: Grove - 433MHz Simple RF Link Kit
category: Communication
bzurl: https://seeedstudio.com/Grove-433MHz-Simple-RF-link-kit-p-1062.html
oldwikiname: Grove_-_433MHz_Simple_RF_Link_Kit
prodimagename: 433MHz_Simple_RF.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/433MHz RF kit.jpg
surveyurl: https://www.research.net/r/Grove-433MHz_Simple_RF_Link_Kit
sku: 113060000
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/img/433MHz_Simple_RF.jpg)

This kit is used for one way wireless communication at a frequency of 433MHz and includes a transmitter module and a receiver module. The twig configuration of this kit allows for around 40 meters of transmitting distance indoors, or around 100 meters outside.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-433MHz-Simple-RF-link-kit-p-1062.html)

Version Tracker
---------------

| Revision | Description            | Release     |
|----------|------------------------|-------------|
| v0.9b    | Initial public release | 03,Oct,2011 |

Features
--------

-   GROVE compatible interface.
-   Uses ASK (Amplitude Shift Keying) Modulation.
-   One way communication.

!!!Tip
    More details about Grove modules please refer to [Grove System](http://wiki.seeedstudio.com/Grove_System/)
    
Specifications
-------------

### Transmitter Module

<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Item
</th>
<th scope="col">
Min
</th>
<th scope="col">
Typical
</th>
<th scope="col">
Max
</th>
<th scope="col">
Unit
</th>
</tr>
<tr align="center">
<th scope="row">
Working Voltage
</th>
<td>
3.0
</td>
<td>
5.0
</td>
<td>
12.0
</td>
<td>
VDC
</td>
</tr>
<tr align="center">
<th scope="row">
Current
</th>
<td>
3
</td>
<td>
/
</td>
<td>
10
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Work Mode
</th>
<td colspan="3">
ASK
</td>
<td>
/
</td>
</tr>
<tr align="center">
<th scope="row">
Transmit Power(Max)
</th>
<td colspan="3">
15
</td>
<td>
mW
</td>
</tr>
<tr align="center">
<th scope="row">
Working Distance
</th>
<td>
40
</td>
<td>
/
</td>
<td>
100
</td>
<td>
m
</td>
</tr>
</table>

### Receiver Module

| Item                 | Typical | Unit |
|----------------------|---------|------|
| Working Voltage      | 5       | VDC  |
| Quiescent Current    | 5       | mA   |
| Receiver Sensitivity | -105    | dBm  |
| Operating frequency  | 433.92  | MHz  |

Application Ideas
-----------------

-   Remote control
-   Remote automation
-   Alarm

Platforms Supported
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Caution
    The platforms mentioned above as supported is/are an indication of the module's hardware or theoritical compatibility. We only provide software library or code examples for Arduino platform in most cases. It is not possible to provide software library / demo code for all possible MCU platforms. Hence, users have to write their own software library.

Getting Started
---------------

The transmitter and receiver modules both rely on a single wire for communication. Though using the UART supplied by the Arduino platform can work, it is recommended, instead, to use the RadioHead library which uses Amplitude Shift Keying for modulation which provides better communication.

Both the transmitter and receiver modules require three wires: Vcc, Ground, and signal. Pin 2 of both parts of the kit are not connected.

-   Connect the Transmitter module to Digital I/O 2 of the [Grove-Base Shield V2](/Base_Shield_V2 "Grove - Base Shield") on the Arduino being used for transmission.

Error creating thumbnail: Invalid thumbnail parameters

-   Connect the Receiver module to Digital I/O 2 of the [Grove-Base Shield V2](/Base_Shield_V2 "Grove - Base Shield") on the receiving Arduino.

Error creating thumbnail: Invalid thumbnail parameters

-   Download the [RadioHead library](https://github.com/adafruit/RadioHead) and unzip it into the libraries folder of the Arduino IDE. 
-   Upload the code below for transmitter module:

```c++
    #include <RH_ASK.h>

    const int BIT_RATE = 2000; // same as default

    const int RX_PIN = 2;

    RH_ASK driver(BIT_RATE, RX_PIN);

    void setup() {
      Serial.begin(9600);

      driver.init();
    }

    void loop() {
      uint8_t buf[RH_ASK_MAX_MESSAGE_LEN];
      uint8_t buflen = sizeof(buf);

      if (driver.recv(buf, &buflen)) {

        for (int i = 0; i < buflen; i++)
          Serial.print((char) buf[i]);

        Serial.println("");
      }

    }
```

-   Upload the code below for receiver module:

```c++
    #include <RH_ASK.h>

    const int BIT_RATE = 2000; // same as default

    const int RX_PIN = 11; // same as default
    const int TX_PIN = 2;

    RH_ASK driver(BIT_RATE, RX_PIN, TX_PIN);

    void setup() {
      driver.init();
    }

    void loop() {
      char str[] = "Hello, World!";

      driver.send((uint8_t *) str, strlen(str));

      driver.waitPacketSent();
    }
```

-   Open the serial monitor of receiver module to see the result.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/img/Receive_Data.jpg)

This is just a simple transmitter and receiver instance as a reference.

Resources
---------

-   [433MHz\_demo.zip](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/315MHz_Demo.zip)
-   [TI:LM358PSR](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/1110010P1.pdf)
-   [RadioHead documentation](http://www.airspayce.com/mikem/arduino/RadioHead/)
-   [R433A Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/ADI;ACTR433A.pdf)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_433MHz_Simple_RF_Link_Kit -->

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/).
