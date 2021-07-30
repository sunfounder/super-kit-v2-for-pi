Lesson 2  Controlling an LED by a Button
==========================================

Introduction
-----------------------

In this lesson, we will learn how to turn an LED on or off by a button.

Components
-----------------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 1 \* LED

\- 1 \* Button

\- 1 \* Resistor (220Ω)

\- Jumper wires

Principle
-----------------------

**Button**

Buttons are a common component used to control electronic devices. They
are usually used as switches to connect or disconnect circuits. Although
buttons come in a variety of sizes and shapes, the one used here is a
6mm mini-button as shown in the following pictures. Pins pointed out by
the arrows of same color are meant to be connected.

.. image:: media/image90.png
    :align: center

When the button is pressed, the pins pointed by the blue arrow will
connect to the pins pointed by the red arrow (see the above figure),
thus closing the circuit, as shown in the following diagrams.

.. image:: media/image91.png
    :align: center

Generally, the button can be connected directly to the LED in a circuit
to turn on or off the LED, which is comparatively simple. However,
sometimes the LED will brighten automatically without any button
pressed, which is caused by various kinds of external interference. In
order to avoid this interference, a pull-up resistor is used – usually
connect a 1K–10KΩ resistor between the button and VCC. It can be
connected to VCC to consume the interference when the button is off.

Schematic Diagram
-------------------------

Use a normally open button as the input of Raspberry Pi. When the button
is pressed, the GPIO connected to the button will turn into low level
(0V). We can detect the state of the GPIO connected to the button
through programming. That is, if the GPIO turns into low level, it means
the button is pressed. You can run the corresponding code when the
button is pressed, and then the LED will light up.

.. image:: media/image92.png
    :align: center

Experimental Procedures
-------------------------

**Step 1**: Build the circuit.

.. image:: media/image93.png
    :align: center

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/02_BtnAndLed/

**Step 3:** Compile.

.. code-block::

    gcc BtnAndLed.c -o BtnAndLed -lwiringPi

**Step 4:** Run.

.. code-block::

    sudo ./BtnAndLed

**For Python Users:**

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 3:** Run.

.. code-block::

    sudo python3 02_btnAndLed.py

Now, press the button, and the LED will light up; press the button
again, and the LED will go out. At the same time, the state of the LED
will be printed on the screen.


.. image:: media/image94.png
    :align: center


Summary
----------------

Through this experiment, you have learnt how to control the GPIOs of the
Raspberry Pi by programming.
