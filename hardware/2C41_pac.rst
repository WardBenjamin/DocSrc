PAC PWM->Analog Signal Converter
================================

Product ID: Cu//2C41

.. note:: See also the shop page for this product: `link <https://shop.copperforge.cc/products/2c41>`__

Background
----------


Sensor Details
--------------

PAC Mechanical Drawing

Electrical connection
^^^^^^^^^^^^^^^^^^^^^

.. warning:: Always consult the technical specifications of the control system you are using *before* wiring the sensor, to ensure that the correct pins are connected.  Failure to do so can result in damage to the sensor or the control system.

The Lasershark has three pins to connect, as seen in the image above: signal ("PWM" or ~), power ("3.3V-5V" or +), and ground ("GND" or |ground|).

The power and ground pins are used to power the PAC, and power is also passed through the PAC to the PWM device.

The PWM signal pin is the pin on which the PWM signal is input, and the analog signal pin is the pin where the analog signal is output.

Mechanical mounting
^^^^^^^^^^^^^^^^^^^

.. warning:: Do not mount directly to metal or other conductive surfaces, since the sensor could be damaged. Mount to a nonconductive material, or use plastic standoffs and fasteners.

As seen in the image above, the PAC mounts using zip ties, and is also compatible with #6/M3 bolts or smaller.

.. todo:: Add content about the max signal itself

Software
--------

.. note:: For detailed information about LibCu, please see :ref:`libcu-header`.

Using LibCu, this sensor


.. |PAC Mechanical Drawing| image:: images/2A21_lasershark_mechanical.png
.. |ground| unicode:: 0x23DA
