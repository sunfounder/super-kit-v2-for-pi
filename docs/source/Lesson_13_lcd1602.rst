Lesson 13  LCD1602
=====================

Introduction
---------------

In this lesson, we will learn how to use LCD1602 to display characters
and strings.

Components
---------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 1 \* LCD1602

\- 1 \* Potentiometer

\- Jumper wires

Principle
---------------

LCD1602, or character type LCD1602, is a dot matrix LCD module specially
used to display letters, figures, symbols, and so on. It consists of
many 16*2 dot matrixes, and each one is composed of 5*7 or 5*11
character bit. Each character bit can display one character. There is a
dot space between each adjacent character bit. Also there is a dot space
between each row. The dot space functions as a character space or line
space; thus, LCD1602 cannot display graphics very well. It is widely
used in pocket instruments and low power application systems due to its
micro power consumption, small size, richness in contents,
ultra-thinness and lightness.

LCD1602 uses the standard 16-pin port, among which:

**Pin 1 (GND):** connected to Ground

**Pin 2 (Vcc):** connected to 5V power supply

**Pin 3 (Vo):** used to adjust the contrast of LCD1602; the level is
lowest when it’s connected to a positive power supply, and highest when
connected to ground (you can connect a 10K potentiometer to adjust its
contrast when using LCD1602)

**Pin 4 (RS):** register select pin that controls where in the LCD’s
memory you are writing data to. You can select either the data register,
which holds what goes on the screen, or an instruction register, which
is where the LCD’s controller looks for instructions on what to do next.

**Pin 5 (R/W):** to read/write signals; it reads signals when supplied
with high level (1), and writes when low level (0) (in this experiment,
you only need to write data to LCD1602, so just connect this pin to
ground)

**Pin 6 (E):** An enable pin that, when low-level energy is supplied,
causes the LCD module to execute relevant instructions

**Pin 7 (D0-D7):** pins that read and write data

**A and K:** controlling LCD backlight

LCD1602 has two operation modes: 4-bit and 8-bit. When the IOs of
microprocessor (MCU) are insufficient, you can choose 4-bit mode, under
which only pins D4~D7 are used. After connecting the circuit, you can
operate LCD1602 by Raspberry Pi.

Schematic Diagram
------------------


.. image:: media/image149.png
    :align: center


Experimental Procedures
-----------------------------

**Step1:** Build the circuit (please be sure the pins are connected
correctly. Otherwise, characters will not be displayed properly):


.. image:: media/image150.png
    :align: center

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/13_LCD1602/

**Step 3:** Compile.

.. code-block::

    gcc lcd1602_2.c -o lcd1602_2 -lwiringPiDev -lwiringPi

**Step 4:** Run.

.. code-block::

    sudo ./lcd1602_2

For Python Users:
^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 3:** Run.

.. code-block::

    sudo python3 13_lcd1602.py

You should see two lines of characters displayed on the LCD1602:
"**SUNFOUNDER**" and "**Hello World ! :)**".


.. image:: media/image151.png
    :align: center

Further Exploration
-----------------------

In this experiment, the LCD1602 is driven in the 4-bit mode. You can try
programming by yourself to drive it in the 8-bit mode.
