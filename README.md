# :snowflake: SmartFridge :ice_cube:

SmartFridge is an ESP-powered <a href="https://shop.m5stack.com/products/m5stack-cores3-se-iot-controller-w-o-battery-bottom">M5Stack CoreS3 SE</a> combined with a <a href="https://shop.m5stack.com/products/2-channel-spst-relay-unit">M5Stack 2-channel relay</a> and a <a href="https://ruuvi.com/ruuvitag/">Ruuvi Bluetooth temperature sensor</a>, that autonomously switches on our fridge in our van or to be more precise, turns the compressor of the fridge on and off, according to the settings chosen.

## Why?

Because I was tired of this:

<img height="400" alt="Temperature Profile Before" src="https://github.com/Naaf3/smartfridge/blob/main/preview/temperature_profile_before.png"/>

## Components

I used the following components:
- <a href="https://shop.m5stack.com/products/m5stack-cores3-se-iot-controller-w-o-battery-bottom">M5Stack CoreS3 SE</a>
- <a href="https://shop.m5stack.com/products/panel-frame-for-m5core">Frame for the M5Stack CoreS3 SE</a>
- <a href="https://shop.m5stack.com/products/2-channel-spst-relay-unit">M5Stack 2-channel relay</a>
- <a href="https://ruuvi.com/ruuvitag/">Ruuvi Bluetooth temperature sensor</a>
- <a href="https://www.amazon.de/dp/B0DC9SLNB7?ref=ppx_yo2ov_dt_b_fed_asin_title">Case</a>
- <a href="https://www.amazon.de/dp/B0CZDT7Q7W?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1">12V to 5V step-down converter</a> (I had to cut off the USB-C, because it didn't fit in the case)
- <a href="https://www.amazon.de/dp/B0CBWY3G45?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1">Connector</a>
- cables and other stuff

## Setup

Let's have a look at the parts:

<img width="400" alt="Parts" src="https://github.com/Naaf3/smartfridge/blob/main/preview/parts.jpg"/>

On the picture there is the black case and the black cable feedthrough next to the case. I had to cut a hole in one of the short sides of the case for the cable feedthrough.

The two connector cables on the bottom of the picture are to connect the SmartFridge box with the cable that is connected to the fridge compressor. The idea is to easy disconnect the box for example if you want to turn it off.

Then there is a fuseholder, the 12V-to-5V-Converter, the 2-channel relay, the CoreS3 and a frame for it, so it fits in the top of the case.

<img width="400" alt="cutout display" src="https://github.com/Naaf3/smartfridge/blob/main/preview/cutout_display.jpg"/>

It's not easy to fit everything in the case, but it works:

<img width="400" alt="everything assembled" src="https://github.com/Naaf3/smartfridge/blob/main/preview/everything_assembled.jpg"/>

Final product:

<img width="400" alt="endproduct" src="https://github.com/Naaf3/smartfridge/blob/main/preview/endproduct.jpg"/>

## Wiring

<img width="400" alt="wiring" src="https://github.com/Naaf3/smartfridge/blob/main/preview/wiring.png"/>

## In the camper

And here is the working SmartFridge control:

<img width="400" alt="Working SmartFridge" src="https://github.com/Naaf3/smartfridge/blob/main/preview/Working_SmartFridgejpg.jpg"/>

Temperature looks much better now 😃

<img width="400" alt="Temperature SmartFridge" src="https://github.com/Naaf3/smartfridge/blob/main/preview/temperature_profile_smartfridge.png"/>

## Status of SmartFridge

The following parameters can be controlled right now:
- target temperature
- hysteresis
- duration of night time mode

Parameters/features to be build in the future:
- better night time mode; the actual is just an increase of the hysteresis; the plan is to set up a time, i.e. 10pm, at which night time mode starts; the fridge should have a defined temperature, i.e. 2 degrees below target temperature, so the fridge stays cool longer
- on/off switch
- security feature like, what happens if the Ruuvi bluetooth sensor signal is lost
<br>
<br>
<br>
### Please note that there are still code snippets or functions in the yaml-file that are not fully reviewed or adapted to my needs.  
<br>
<br>
If you like my work and want to support me:
<br>
<a href="https://www.paypal.com/donate/?hosted_button_id=H9TBKLCDM8J2J">
  <img src="https://github.com/Naaf3/Introduction/blob/main/images/donate_button.png" width="300" alt="Donate with PayPal" />
</a>




