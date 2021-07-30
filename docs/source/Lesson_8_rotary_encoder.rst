Lesson 8  Rotary Encoder
===========================

Introduction
----------------

A rotary encoder is a type of electro-mechanical device that converts
the angular position or motion of a shaft or axle to an analog or
digital code. In this lesson, we will learn how to use this device.

Components
----------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 1 \* Rotary Encoder Module

\- Jumper wires

Principle
----------------

A rotary encoder is an electronic switch with a set of regular pulses
with strictly timing sequence. When used with IC, it can achieve
increment, decrement, page turning and other operations such as mouse
scrolling, menu selection, acoustic sound regulation, frequency
regulation, toaster temperature regulation, and so on.

There are mainly two types of rotary encoders: absolute and incremental
(relative) encoders. The output of absolute encoders indicates the
current position of the shaft, making them angle transducers. The output
of incremental encoders provides information about the motion of the
shaft, which is typically further processed elsewhere into information
such as speed, distance, and position.

.. image:: media/image120.png
    :align: center

Most rotary encoders have 5 pins with three functions of turning left,
turning right and pressing down:

**Pin 4 & 5**: switching wiring terminals for pressing down (no
different from the buttons mentioned previously, so no more details will
be provided here.)

**Pin 2**: generally connected to ground.

**Pin 1 & 3**: first connected to a pull-up resistor and then to a
microprocessor (in this experiment, to GPIO0 and GPIO1 of Raspberry Pi);
when you spin the knob of the encoder clockwise and counterclockwise,
there will be pulse outputs in pin 1 and pin 3.

If both GPIO0 and GPIO1 are at high level, the switch rotates clockwise;
if GPIO0 is at high level but GPIO1 is low, the switch rotates
counterclockwise. Therefore, when programming, you only need to check
the state of pin 3 when pin 1 is at high level, and then you can tell
whether the switch rotates clockwise or counterclockwise.



**Step 1:** Build the circuit.

+--------------+----------------+
| Raspberry Pi | Rotary Encoder |
+--------------+----------------+
| 3.3V         |  \+            |
+--------------+----------------+
| GND          | GND            |
+--------------+----------------+
| GPIO17       | DT             |
+--------------+----------------+
| GPIO18       | CLK            |
+--------------+----------------+
| GPIO27       | SW             |
+--------------+----------------+

.. image:: media/image121.png
    :align: center

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/08_RotaryEncoder/

**Step 3:** Compile.

.. code-block::

    gcc rotaryEncoder.c -o rotaryEncoder **-**\ lwiringPi

**Step 4:** Run.

.. code-block::

    sudo ./rotaryEncoder

For Python Users:
^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 3:** Run.

.. code-block::

    sudo python3 08_rotaryEncoder.py

Now, gently rotate the encoder to change the value of the variable in
the above program, and you will see the value printed on the screen.
Rotate the encoder clockwise, the value will increase; or rotate it
counterclockwise, the value will decrease.

.. image:: media/image122.png
    :align: center

Further Exploration
----------------------

In this experiment, the pressing down function of rotary encoder is not
involved. Try to explore this function by yourself!

