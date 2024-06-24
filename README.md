## Adafruit High Voltage UPDI Friend - USB Serial UPDI Programmer PCB

<a href="http://www.adafruit.com/products/5893"><img src="assets/5893.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit High Voltage UPDI Friend - USB Serial UPDI Programmer. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5893

### Description

UPDI stands for Unified Program and Debug Interface, but this board is so smol and cute that we will call it the Unusually Playful Device Interfacer and pat its head when it does a good job. It's designed to make programming modern ATtiny chips very easy because it has 3V or 5V power and logic select, power, and transmit indicator LEDs, and a quick cable for poking into a breadboard.

Unlike our simple UPDI version, this board is HV for High Voltage because it will let you send a quick 12V pulse to the UPDI like right before programming. This is required for when the chip is configured to use the UPDI pin as a reset or GPIO. This board will also let you 'unbrick' any chip configured for HV usage, you can use it to reset the fuses for Low Voltage programming.

As for our seesaw boards, we have been working a lot with ATtiny816, ATtiny817, and ATtiny1616 chips lately. And we're often needing to program them with a CP2102-based breakout with a 1K resistor soldered between the RX and TX pins. But we were hankering for a nicer programmer!

This UPDI High Voltage Friend makes programming such chips very easy:

* Select between 3V or 5V power and logic - the 3V regulator can source up to 500mA to run even big projects. 
* Internal 12V boost converter with analog switch that will send a pulse to the UPDI line when the RTS pin is toggled low. 
* CH340E USB Serial converter chip with cross-platform drivers
* 1K Loop-back Resistor between RX and TX
* USB Type C for data and power connection to any computer
* JST SH cable included for quick plugging into a breadboard - you can get another JST SH 3-pin cable with sockets or with pin header here.
* 0.1" spaced breakout holes for custom connections.
* Green power OK LED
* Red serial activity LED
* Inspired by this [open-source hardware design](https://github.com/wagiminator/AVR-Programmer/tree/master/SerialUPDI_HV_Programmer) from [Stefan Wagner](https://github.com/wagiminator)!

We use Arduino IDE with the megaTinyCore board support package installed; simply select "Serial UPDI" as the programmer type. We use 230Kbps, but 56Kbps is also good. In order to enable the high-voltage fuses settings, you'll need to edit boards.txt to remove the # comment tag on the “UPDI/RESET PIN CONFIGURATION” lines.
### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
