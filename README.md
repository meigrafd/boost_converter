booster
=======

A boost converter Addon for Nathan Chantrell's TinyTX to extend battery life: https://github.com/nathanchantrell/TinyTX/


Its my first PCB so please be lenient :)


##License
Proudly open source<br>
The hardware designs (schematics and CAD files) are licensed under a Creative Commons Attribution-ShareAlike 3.0 Unported License.<br>
The documentation is subject to GNU Free Documentation License<br>



##Overview
The board uses an ultra low-drain LTC3525 boost regulator chip which draws only 7..30 µA in idle mode (depends on input voltage). The input can range from 1.0V to 5.5V (absolute maximum: 6V), so this can also be used with 2x or 3x AA battery packs (even 4, if NiMh). The regulator continues to operate with input voltage fading to less than 0.5V - squeezing the last bit of energy from the battery.

The board was specifically designed for use with a TinyTX, but can be used with anything that needs 3.3V. The maximum output current is 60..150 mA, depending on input voltage.

Taking a reading once every 60s the TinyTX batteries should last for 1-3 years. I recommend rechargeable alkaline batteries for best performance and environmental impact.


The PCB has a size of: 13.2mm x 11.0mm
