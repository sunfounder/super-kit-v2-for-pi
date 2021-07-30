Lesson 4  Breathing LED
=========================


Introduction
-----------------

In this lesson, we will try something interesting – gradually increase
and decrease the luminance of an LED with PWM, just like breathing. So
we give it a magical name - Breathing LED.

Components
-----------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 1 \* LED

\- 1 \* Resistor (220Ω)

\- Jumper wires

Principle
-----------------

**PWM**

Pulse Width Modulation, or PWM, is a technique for getting analog
results with digital means. Digital control is used to create a square
wave, a signal switched between on and off. This on-off pattern can
simulate voltages in between full on (3.3 Volts) and off (0 Volts) by
changing the portion of the time the signal spends on versus the time
that the signal spends off. The duration of "on time" is called pulse
width. To get varying analog values, you change, or modulate, that
width. If you repeat this on-off pattern fast enough with some device,
an LED for example, the result would be like this: the signal is a
steady voltage between 0 and 3.3v controlling the brightness of the LED.
(See the PWM description on the official website of Arduino)

**Duty Cycle**

A duty cycle is the percentage of one period in which a signal is
active. A period is the time it takes for a signal to complete an
on-and-off cycle. As a formula, a duty cycle may be expressed as:

.. image:: media/image161.png
    :align: center

where **D** is the duty cycle, **T** is the time the signal is active,
and **P** is the total period of the signal. Thus, a 60% duty cycle
means the signal is on 60% of the time but off 40% of the time. The "on
time" for a 60% duty cycle could be a fraction of a second, a day, or
even a week, depending on the length of the period.


.. image:: media/image101.png
    :align: center

In this experiment, we use this technology to make the LED brighten and
dim slowly so it looks like our breath.

Schematic Diagram
------------------------------


.. image:: media/image102.png
    :align: center



Experimental Procedures
------------------------------

**Step 1:** Build the circuit.


.. image:: media/image103.png
    :align: center

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::
    
    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/04_PwmLed

**Step 3**: Compile.

.. code-block::
    
    gcc PwmLed.c -o PwmLed -lwiringPi -lpthread

**Step 4**: Run.

.. code-block::
    
    sudo ./PwmLed

For Python Users:
^^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::
    
    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 3**: Run.

.. code-block::
    
    sudo python3 04_pwmLed.py

Now you will see the gradual change of the LED luminance, between bright
and dim.


.. image:: media/image104.png
    :align: center

Summary
-------------

Through this experiment, you should have mastered the principle of PWM
and how to program Raspberry Pi with PWM. You can try to apply this
technology to DC motor speed regulation later.
