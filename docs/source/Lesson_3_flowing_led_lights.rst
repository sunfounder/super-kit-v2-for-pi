Lesson 3  Flowing LED Lights
==============================


Introduction
--------------------------

In this lesson, we will learn how to make eight LEDs blink in various
effects as you want based on Raspberry Pi.

Components
--------------------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 8 \* LED

\- 8 \* Resistor (220Ω)

\- Jumper wires

Schematic Diagram
--------------------------

Set GPIO17-GPIO25 to low level in turn by programming, and then
LED0-LED7 will light up in turn. You can make eight LEDs blink in
different effects by controlling their delay time and the order of
lighting up.


.. image:: media/image95.png
    :align: center




Experimental Procedures
--------------------------

**Step 1**: Build the circuit.


.. image:: media/image96.png
    :align: center


**Step 2:** GPIO4 is the default pin for onewire driver (w1-gpio). In
this lesson, we need to disable the onewire function and use it as an
output pin.

.. code-block::

    sudo nano /boot/config.txt

Commit the following line.

.. code-block::

    #dtoverlay = w1-gpio

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^^^

**Step 3:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/03_8Led/

**Step 4:** Compile.

.. code-block::

    gcc 8Led.c -o 8Led -lwiringPi

**Step 5:** Run.

.. code-block::

    sudo ./8Led

For Python Users:
^^^^^^^^^^^^^^^^^^^^^^

**Step 3:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 4:** Run.

.. code-block::

    sudo python3 03_8Led.py

Then you will see eight LEDs brighten and dim left to right and right to
left circularly, just like flowing water.


.. image:: media/image97.png
    :align: center


**Further Exploration**

You can write the blinking effects of LEDs in an array. If you want to
use one of these effects, you can call it in the *main()* function
directly.
