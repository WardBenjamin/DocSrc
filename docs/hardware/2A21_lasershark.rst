Lasershark 12ft Laser Rangefinder
=================================

Product ID: Cu//2A21

.. note:: See also the shop page for this product: `link <https://shop.copperforge.cc/products/2a21>`__

The Lasershark 12ft Ranging Sensor is a state-of-the-art Time-of-Flight laser ranging sensor, which offers precise ranging up to 12ft in an easy-to-use form factor and interface. Onboard firmware allows students to interact with this complex sensor with only a standard 3-wire 0.1" pitch "PWM" cable and minimal programming.

Background
----------

LIDAR (LIght Detection And Ranging) sensors are a variety of rangefinder seeing increasing use in competition robotics. The Lasershark (Cu//2A21) is an example of a single-dimension (1D) LIDAR sensor.

1D LIDAR sensors works much like common ultrasonic sensors - they measure the distance to the nearest object which is more or less along a line in front of it. These sensors can often be more reliable than ultrasonics, as they have narrower beam profiles. This means that they are less susceptible to interference from other nearby objects.

Similarly to an ultrasonic, this sensor uses time-of-flight measurement techniques. Distance is calculated by measuring the round trip time between a laser pulse and its return to the sensor. This method is more accurate than calculating the distance based on reflected light intensity, which is the method typically used for infrared proximity sensors.

Sensor Details
--------------

|Lasershark Mechanical Drawing|

Electrical connection
^^^^^^^^^^^^^^^^^^^^^

.. warning:: Always consult the technical specifications of the control system you are using *before* wiring the sensor, to ensure that the correct pins are connected.  Failure to do so can result in damage to the sensor or the control system.

The Lasershark has three pins to connect, as seen in the image above: signal ("PWM" or ~), power ("3.3V-5V" or +), and ground ("GND" or |ground|).

The power and ground pins are used to power the sensor. The signal pin is the pin on which the PWM output signal is actually measured.



.. note:: Some simple sensors (such as :doc:`potentiometers <analog-potentiometers-hardware>`) may have interchangeable power and ground connections.

Most sensors that connect to analog input ports will have three wires - signal, power, and ground - corresponding precisely to the three pins of the analog input ports.  They should be connected accordingly.

.. todo:: add picture

Connecting a sensor to multiple analog input ports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Some sensors may need to connect to multiple analog input ports in order to function.  In general, these sensors will only ever require a single power and a single ground pin - only the signal pin of the additional port(s) will be needed.

.. todo:: add picture

.. |Lasershark Mechanical Drawing| image:: images/2A21_lasershark_mechanical.png
.. |ground| unicode:: 0x23DA

Footnotes
---------

.. [1] A 12-bit resolution yields :math:`2^{12}`, or 4096 different values.  For a 5V range, that's an effective resolution of approximately 1.2 mV, or .0012V.  The actual accuracy specification is plus-or-minus 50mV, so the discretization is not the limiting factor in the measurement accuracy.
.. [2] All power pins are actually connected to a single rail, as are all ground pins - there is no need to use the power/ground pins corresponding to a given signal pin.
