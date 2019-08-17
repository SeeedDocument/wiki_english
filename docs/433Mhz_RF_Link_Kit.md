---
name: 433Mhz RF Link Kit
category: MakerPro
bzurl: https://www.seeedstudio.com/433mhz-rf-link-kit-p-127.html?cPath=139_140
oldwikiname: 433Mhz RF Link Kit
prodimagename: 113990010%201.jpg
surveyurl: https://www.research.net/r/433Mhz_RF_Link_Kit
sku: 113990010
---

![](https://github.com/SeeedDocument/433Mhz_RF_Link_Kit/raw/master/img/113990010%201.jpg)

This kit is consists of a transmitter and receiver pair, often used for a remote control.

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png)](http://www.seeedstudio.com/depot/433mhz-rf-link-kit-p-127.html?cPath=139_140)

## Specification
---
- Frequency: 433Mhz
- Modulation: ASK
- Receiver Data Output: High - 1/2 Vcc, Low - 0.7v
- Transmitter Input Voltage: 3-12V (high voltage = more transmitting power)
- Receiver Input Voltage : 3.3-6V (high voltage = more receiving power)

## Usage
---
A popular arrangement for this kit is: MCU -> Encoder -> Transmitter ------ Receiver -> Decoder -> MCU

PT2262 (Encoder) and PT2272 (Decoder) are optional, but you can use them to avoid confusing whith multiple RF links and block interference. You can also integrate the encoding and decoding into the MCUs on both sides. Whenever there is no 315Mhz devices around, you can use it as a direct cable connection.

Excuse us for the documentation, we are working on it. Meanwhile, please consult us for any information, we are happy to find the answer for you ^^. We tried this RF Link Kit using the guide from Sparkfun and it's compatible. The only difference is package in the guide, which has some excess GND and VCC pins.

More over, we will make more RF modules ourselves with different frequency and capacity. The next one in plan is based on cc1100 Please consult us about your needs :)

## Support

If you have any questions or better design ideas, you can go to our [forum](https://community.seeedstudio.com/) to discuss.

## Resources

- [Demo scheme](https://github.com/SeeedDocument/433Mhz_RF_Link_Kit/raw/master/res/315MRFlink.pdf)
- [VirtualWire 1.3 Arduino library (unmaintained)](https://github.com/SeeedDocument/433Mhz_RF_Link_Kit/raw/master/res/VirtualWire.rar)
- [VirtualWire 1.3 documentation](https://github.com/SeeedDocument/433Mhz_RF_Link_Kit/raw/master/res/VirtualWire.pdf)
- [RadioHead 1.92 Arduino library](http://www.airspayce.com/mikem/arduino/RadioHead/RadioHead-1.92.zip)
- [RadioHead documentation](http://www.airspayce.com/mikem/arduino/RadioHead/)
- [Example from Sparkfun](https://github.com/SeeedDocument/433Mhz_RF_Link_Kit/raw/master/res/KLP_Walkthrough.pdf)

## Licensing

This documentation is licensed under the Creative Commons [Attribution-ShareAlike License 3.0](https://creativecommons.org/licenses/by-sa/3.0/) Source code and libraries are licensed under [GPL/LGPL](http://www.gnu.org/licenses/gpl.html), see source code files for details.
External Links

Links to external webpages which provide more application ideas, documents/datasheet or software libraries
- [RCSwitch - Arduino Library to control 433Mhz remote power sockets](http://code.google.com/p/rc-switch)

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
