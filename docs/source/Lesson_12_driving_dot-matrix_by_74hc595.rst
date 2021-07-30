Lesson 12  Driving Dot-Matrix by 74HC595
============================================

Introduction
-----------------

With low-voltage scanning, dot matrix LED displays have advantages such
as power saving, long service life, low cost, high brightness, a wide
angle of view, long visual range, waterproofness, and so on. They can
meet the needs of different applications and thus have a broad
development prospect. In this lesson, we will learn how to use 74HC595
to drive an LED dot-matrix.

Components
-----------------

\- 1 \* Raspberry Pi

\- 1 \* Breadboard

\- 2 \* 74HC595

\- 1 \* Dot-Matrix

\- Jumper wires

Principle
-----------------

**Dot Matrix**

The external view:

.. image:: media/image144.png
    :align: center

Pin definition:

Define the row and column numbering at first (only for the dot matrix
whose model number ends with BS)

.. image:: media/image145.png
    :align: center

Pin numbering corresponding to the above rows and columns:

+-------------+--------+--------+-------+--------+-------+--------+--------+--------+
| **COL**     | **1**  | **2**  | **3** | **4**  | **5** | **6**  | **7**  | **8**  |
+-------------+--------+--------+-------+--------+-------+--------+--------+--------+
| **Pin No.** | **13** | **3**  | **4** | **10** | **6** | **11** | **15** | **16** |
+-------------+--------+--------+-------+--------+-------+--------+--------+--------+
| **ROW**     | **1**  | **2**  | **3** | **4**  | **5** | **6**  | **7**  | **8**  |
+-------------+--------+--------+-------+--------+-------+--------+--------+--------+
| **Pin No.** | **9**  | **14** | **8** | **12** | **1** | **7**  | **2**  | **5**  |
+-------------+--------+--------+-------+--------+-------+--------+--------+--------+

The 8*8 dot matrix is made up of sixty-four LEDs and each LED is placed
at the cross point of a row and a column. When the electrical level of a
certain row is High and the electrical level of a certain column is Low,
the corresponding LED at their cross point will light up. For example,
to turn on the LED at the first dot, you should set ROW 1 to high level
and COL 1 to low, so the LED at the first dot brightens; to turn on all
the LEDs on the first row, set ROW 1 to high level and COL 1-8 to low,
and then all the LEDs on the first row will light up; similarly, set COL
1 to low level and ROW 1-8 to high level, and all the LEDs on the first
column will light up.

The principle of 74HC595 has been illustrated previously. One chip is
used to control the rows of the dot matrix while the other, the columns.


Schematic Diagram
----------------------

.. image:: media/image146.png
    :align: center

Experimental Procedures
------------------------------

**Step 1:** Build the circuit.

.. image:: media/image147.png
    :align: center

For C Language Users:
^^^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_C_code_for_RaspberryPi/12_DotMatrix/

**Step 3**: Compile.

.. code-block::

    gcc dotMatrix.c -o dotMatrix -lwiringPi

**Step 4**: Run.

.. code-block::

    sudo ./dotMatrix

For Python Users:
^^^^^^^^^^^^^^^^^^^^^^

**Step 2:** Change directory.

.. code-block::

    cd/home/pi/Sunfounder_SuperKit_Python_code_for_RaspberryPi/

**Step 3**: Run.

.. code-block::

    sudo python3 12_DotMatrix.py

You should see LEDs light up as you control.

.. image:: media/image148.png
    :align: center

Summary
----------
Through this lesson, you have got the basic principle of LED dot matrix
and how to program the Raspberry Pi to drive an LED dot matrix based on
74HC595 cascade. With the knowledge learnt, try more fascinating
creations!


