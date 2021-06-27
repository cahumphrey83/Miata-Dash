# Miata Digital Dash Project
## This page is built to document the process of building my Raspberry Pi powered digital dashboard in my Turbocharged 1999 Mazda Miata.

My goal was to create a display to monitor coolant temp and boost levels on my car without cluttering the interior up with lots of gauges. Since the car is already running on a Megasquirt 3 ECU, sensors already exist for most of the values that I would want to monitor. Because I was going to run a digital display, I also wanted to be able to make basic tuning adjustments to the car without requiring a laptop with me at all times.

Knowing that I want the ability to perform changes to the tune without a laptop, the two options I was considering were either a tablet or a Raspberry Pi based setup. I wasn't happy with any of the mounting solutions that I'd found for tablets, and was worried about the hardware performance compared to a Pi. Once I settled on a Raspberry Pi 4, it was time to choose the rest of the hardware involved.

## Hardware
- [Raspberry Pi Official 7" Touchscreen](https://www.raspberrypi.org/products/raspberry-pi-touch-display/)
- [Raspberry Pi 4 (4GB)](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/)
- [HiFiBerry amp2](https://www.hifiberry.com/shop/boards/hifiberry-amp2/)
- [Geekwork 2x20 Header Extender](https://www.amazon.com/gp/product/B0827THC7R)
- [Raspberry Pi Terminal Block](https://www.amazon.com/gp/product/B084C69VSQ/)
- Future Improvements
  - [10 Amp Timer](http://timers.shop/6V-28V-10-Amp-Timer-POSITIVE-OUTPUT_p_13.html)
  - Automotive Relays

### Step 1 - Connect the Raspberry Pi to the 7" Touchscreen Display

The hardware stack I used had simplicity and compatibility at the front of my mind. When working with the Official 7" Touchscreen display, the Pi will mount to the standoffs on the back of the display. it simply connects with a ribbon cable for the display, and 4 wires run to the GPIO header for power and touchscreen controls.

1. Connect the video ribbon cable to the display.
2. When looking at the back of the display, connect the jumper wires front left to right, in the following order:
   - 5V (Red Wire)
   - Blank Pin (No Wire)
   - SDA (Green Wire)
   - SCL (Yellow Wire)
   - GND (Black Wire)
3. Attach the Raspberry Pi to the metal standoffs on the back of the display with the included machine screws. Make sure that the Pi is oriented properly to allow the ribbon cable from the display to connect to the Pi.
4. Attach the ribbon cable from the display to the Raspberry Pi.
5. (Optional) If you are skipping the HiFiBerry Amp2, then you will now need to connect the jumpers from the display to the GPIO headers on the Pi.
   - 5V (Red Wire) to pin 4
   - GND (Black Wire) to pin 6
   - SDA (Green Wire) to pin 3
   - SCL (Yellow Wire) to Pin 5

### Step 2 - Connect HiFiBerry Amp2 to the Pi



### Step 3 - Connect Header Extender and Terminal Block

## Software
- [OpenAuto Pro](https://bluewavestudio.io/shop/openauto-pro-car-head-unit-solution/)
- [TunerStudio Ultra](http://tunerstudio.com/)

## 3D Printing
- [3D Printed Mount for Raspberry Pi 7" Display](https://www.thingiverse.com/thing:4892851)

## TLDR Links
- Hardware
  - https://www.raspberrypi.org/products/raspberry-pi-4-model-b/ Raspberry Pi 4 (4gb)
  - https://www.raspberrypi.org/products/raspberry-pi-touch-display/ Display
  - https://www.hifiberry.com/shop/boards/hifiberry-amp2/ Sound Card / 2 channel amplifier
  - http://timers.shop/6V-28V-10-Amp-Timer-POSITIVE-OUTPUT_p_13.html Current Timer
  - https://www.amazon.com/gp/product/B0827THC7R Geekwork 2x20 Header Extender
  - https://www.amazon.com/gp/product/B084C69VSQ/ Terminal Block 
- Software
  - https://bluewavestudio.io/shop/openauto-pro-car-head-unit-solution/
  - http://tunerstudio.com/ TunerStudio Ultra
- 3D Printing
  - https://www.thingiverse.com/thing:4892851 Mount for 7" Display