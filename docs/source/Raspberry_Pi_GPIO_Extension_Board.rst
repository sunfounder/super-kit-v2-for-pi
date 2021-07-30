Raspberry Pi GPIO Extension Board
========================================

We apply the GPIO Extension Board to extend the pins of Raspberry Pi to
the breadboard and avoid damage caused by frequent plugging and
unplugging.

Here, we apply a 40-pin GPIO Extension board and a 40-pin GPIO cable. In
case of the potential risk of short circuit, you must build your circit in
strict accordance with the following picture.

.. image:: media/image82.png
    :align: center


The pins of Raspberry Pi have three kinds of ways to name and they are
wiringPi, BCM and Board. Among these naming methods, 40-pin GPIO
Extension board uses the naming method, BCM. But for some special
pins, such as I2C port and SPI port, they use the Name that comes with
themselves. The following table shows us the naming methods of
WiringPi, Board and the intrinsic Name of each pin on GPIO Extension
board. For example, for the GPIO17, the Board naming method of it is
11, the wiringPi naming method is 0, and the intrinsic naming method
of it is GPIO0.
 
.. Note::

    1）In C Language, what is used is the naming method WiringPi.
    
    2）In Python Language, the applied naming methods are Board and BCM,
    and the function GPIO.setmode() is used to set them.

+------+--------+--------+--------+--------+------+--------+--------+
|Name  |WiringPi| Board  |       BCM       |Board |WiringPi|Name    | 
+------+--------+--------+--------+--------+------+--------+--------+
|      |        | GPIO Extention Board     |      |        |        |
+------+--------+--------+--------+--------+------+--------+--------+
|3.3V  | 3V3    | 1      | 3V3    | 5.0V   | 2    | 5.0V   | 5V     |
+------+--------+--------+--------+--------+------+--------+--------+
|SDA   | 8      | 3      | SDA    | 5.0V   | 4    | 5.0V   | 5V     |
+------+--------+--------+--------+--------+------+--------+--------+
|SCL   | 9      | 5      | SCL    | GND    | 6    | GND    | 0V     |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO7 | 7      | 7      | GPIO4  | TXD    | 8    | 15     | TXD    |
+------+--------+--------+--------+--------+------+--------+--------+
|0V    | GND    | 9      | GND    | RXD    | 10   | 16     | RXD    |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO0 | 0      | 11     | GPIO17 | GPIO18 | 12   | 1      | GPIO1  |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO2 | 2      | 13     | GPIO27 | GND    | 14   | GND    | 0V     |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO3 | 3      | 15     | GPIO22 | GPIO23 | 16   | 4      | GPIO4  |
+------+--------+--------+--------+--------+------+--------+--------+
|3.3V  | 3.3V   | 17     | 3.3V   | GPIO24 | 18   | 5      | GPIO5  |
+------+--------+--------+--------+--------+------+--------+--------+
|MOSI  | 12     | 19     | MOSI   | GND    | 20   | GND    | 0V     |
+------+--------+--------+--------+--------+------+--------+--------+
|MISO  | 13     | 21     | MISO   | GPIO25 | 22   | 6      | GPIO6  |
+------+--------+--------+--------+--------+------+--------+--------+
|SCLK  | 14     | 23     | SCLK   | CE0    | 24   | 10     | CEO    |
+------+--------+--------+--------+--------+------+--------+--------+
|0V    | GND    | 25     | GND    | CE1    | 26   | 11     | CE1    |
+------+--------+--------+--------+--------+------+--------+--------+
|IN_SDA| 30     | 27     | EED    | EEC    | 28   | 31     | ID_SCL |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO21| 21     | 29     | GPIO5  | GND    | 30   | GND    | 0V     |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO22| 22     | 31     | GPIO6  | GPIO12 | 32   | 26     | GPIO26 |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO23| 23     | 33     | GPIO13 | GND    | 34   | GND    | 0V     |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO24| 24     | 35     | GPIO19 | GPIO16 | 36   | 27     | GPIO27 |
+------+--------+--------+--------+--------+------+--------+--------+
|GPIO25| 25     | 37     | GPIO26 | GPIO20 | 38   | 28     | GPIO28 |
+------+--------+--------+--------+--------+------+--------+--------+
|0V    | GND    | 39     | GND    | GPIO21 | 40   | 29     | GPIO29 |
+------+--------+--------+--------+--------+------+--------+--------+
