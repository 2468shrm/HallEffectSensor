# HallEffectSensor

This is a simple sensor for FRC mechanisms based on the Honeywell SM351LT.
The intended uses include contactless extension/rotation limit sensing.
I've tried many times to get the team to use one on turrets or elevators
and I hope that creating one for the team might encourage their use.

The datasheet for the sensor is [here](https://www.mouser.com/datasheet/2/187/HWSC_S_A0012827053_1-3073404.pdf).

The operating voltage of this circuit is 3.3V. The connector to a connecting
single-board computer is a 3-pin signal/power/ground 0.1 inch header.  It is
3.3V since the sensor operates at 3.3V and there was no intention of including
a 5V-to-3.3V regulator to minimize costs.

Since limit sensing is a digital operation (you're at the limit or not)
the circuit includes a voltage divider to set a sensitivity/reference level
and comparator to digitize the sensing. It also includes a LED to indicate
the output of the sensor.

There are two 3-pin 0.1" header footprints.
- One for the connection to a DIO on a feather board
- One that is in parallel to the output of the sensor, so that the sensor may
be depopulated an another 3.3V sensor is connected externally, OR, it makes a
good probe point
