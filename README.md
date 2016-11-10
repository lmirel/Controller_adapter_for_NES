<a href="https://github.com/mcgurk/Controller_adapter_for_NES/raw/master/Images/Wii-Classic-Controller_Arduino_NES.jpg"><img src="https://github.com/mcgurk/Controller_adapter_for_NES/raw/master/Images/Wii-Classic-Controller_Arduino_NES.jpg" height="300"></a>

# Wii Classic Controller to NES.

Works with normal Arduino with Atmega328P (5V 16MHz). I used Arduino Pro Mini.

Lag under 1ms.

Compatible with PAL (50Hz) and NTSC (60Hz) (NTSC support not tested).

Arduino Pro Mini, AMS1117 regulator, signal voltage converter and Wii Classic Controller altogether 28mA.

## Images

https://github.com/mcgurk/Controller_adapter_for_NES/raw/master/Images/2016-11-10%2011.08.51.jpg

https://github.com/mcgurk/Controller_adapter_for_NES/raw/master/Images/2016-11-10%2011.23.53.jpg

## Connections

### Wii Classic Controller (I2C)

Arduino Uno/Pro Mini: SDA = A4, SCL = A5

Officially Wii extension controllers are 3.3V.  Might work with 5V. I used level converter with 3.3V AMS1117 regulator. Search from Ebay with Logic Level Converter Module AMS1117 DC 5V to 3.3V

### NES-controller:

- Pin 8 NES data (PORTB, bit 1) https://www.arduino.cc/en/Reference/PortManipulation
- Pin 2 NES latch
- Pin 3 NES pulse

Latch and pulse must be interrupt pins: https://www.arduino.cc/en/Reference/AttachInterrupt

## Links

http://www.mit.edu/~tarvizo/nes-controller.html
