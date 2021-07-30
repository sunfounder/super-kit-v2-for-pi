Lesson 14  ADXL345
======================

Introduction
--------------------------

In this lesson, we will learn how to use the acceleration sensor
ADXL345.

Components
--------------------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 1 \* ADXL345 module

\- Jumper wires

Principle
--------------------------

**ADXL345**

The ADXL345 is a small, thin, low power, 3-axis accelerometer with high
resolution (13-bit) measurement at up to ±16 g. Digital output data is
formatted as 16-bit two’s complement and is accessible through either an
SPI (3- or 4-wire) or I2C digital interface.

The ADXL345 is well suited to measure the static acceleration of gravity
in tilt-sensing applications, as well as dynamic acceleration resulting
from motion or shock. Its high resolution (4 mg/LSB) enables the
inclination change measurement by less than 1.0°. And the excellent
sensitivity (3.9mg/LSB @2g) provides a high-precision output of up to
±16g. In this experiment, I2C digital interface is used.

Experimental Procedures
--------------------------

**Step 1:** Build the circuit.

.. image:: media/image0.png
    :align: center

.. image:: media/image152.png
    :align: center

The I2C interface is used in the following program. Before running the
program, please make sure the I2C driver module of Raspberry Pi has
loaded normally(Refer to Appendix).

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/14_ADXL345/

**Step 3:** Compile.

.. code-block::

    gcc adxl345.c -o adxl345 -lwiringPi

**Step 4:** Run.

.. code-block::

    sudo ./adxl345

For Python Users:
^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi

**Step 3:** Run.

.. code-block::

    sudo python3 14_ADXL345.py

Now, rotate the acceleration sensor, and you should see the values
printed on the screen change.

.. image:: media/image153.png
    :align: center