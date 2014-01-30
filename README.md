booster
=======

A boost converter Addon for Nathan Chantrell's TinyTX to extend battery life: https://github.com/nathanchantrell/TinyTX/

<br>

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

========
German
========

Das PCB besteht aus 2 Layers:  Top (rot) und Bottom (blau)<br>
Wenn man normalerweise ein Board in Eagle öffnet wird die Polygon Fläche nicht angezeigt - was bei mir auf dem Screenshot aber der Fall ist, deshalb ist auch fast das ganze Board mit Rot auf der Oberseite und Blau auf der Unterseite ausgefüllt... Diese Polygon Fläche (Kupfer) wird einerseits zur Kühlung genutzt, anderseits für GND und zusätzlich muss beim Herstellungsprozess weniger Kupfer weggeätzt werden - deshalb sind die unteren beiden GND Löt-Pads auch nicht extra verdrahtet, sondern eben mit beiden Polygon Flächen verbunden. 

Beschriftungen auf der Oberseite:
* Links oben ist das "Open Hardware" Logo.
* Unten rechts ist ein "boost converter" Schriftzug.
* Die Bauteile "L1" mit 10uH , "C1" mit 1uF und "C2" mit 10uF (dessen Schriftgröße ich bisher nicht zu ändern geschafft habe)

Beschriftungen auf der Unterseite: (gespiegelt)
* Die Lötbohrungen für die Batterie: Vin und GND
* Die Lötbohrungen für die TinyTX Platine: GND und Vout
* Oben hab ich mir erlaubt einen Zweizeiler zu setzen:<br>
 TinyTX boost converter v1.0<br>
 http://forum-raspberrypi.de


Ich werd jetzt versuchen jemanden zu finden der das PCB nochmal prüft (wenn hier jmd is bitte bei mir melden) und dann erste Prototype PCB's anfertigen lassen - mal gucken ob das so funktioniert :-)


**Hintergrund:**<br>
Der LTC3525 boost regulator chip verbraucht sehr wenig Strom: 7 bis 30 µA im idle mode (kommt auf die Input Voltage an) und kann mit einer Spannung zwischen 1.0 und 5.5V umgehen. Man kann also auch problemlos 3xAA Alkaline (oder 4 x NiMh) Batterien benutzen.<br>
Ausserdem arbeitet der Boost Converter auch noch bei einer Spannung von nur 0.5V weiter, es wird also wirklich das letzte Quentchen aus den Batterien gelutscht ;)<br>
http://jeelabs.net/projects/hardware/wiki/AA_Power_Board haben ebenfalls ein PCB entwickelt wo der LTC3525 zum Einsatz kommt und auch OpenEnergyMonitor verwenden den LTC3525 mit ihren http://wiki.openenergymonitor.org/index.php?title=EmonTH Funk Sensoren.



PS: Ein gutes Tutorial für Eagle, was mir sehr geholfen hat: http://service.projektlabor.tu-berlin.de/onlinekurs/eagleboard/
