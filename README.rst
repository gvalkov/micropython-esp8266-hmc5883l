HMC5883L ESP8266 Micropython
============================

A class for working with the HMC5883L_ 3-axis digital compass IC with
micropython on the esp8266.


Usage
-----

Upload `hmc5883l.py`_ to the micro-controller (e.g. you can use
`adafruit-ampy`_) and use as:

.. code-block:: python

  from hmc5883l import HMC5883L

  sensor = HMC5883L(scl=4, sda=5)

  x, y, z = sensor.read()
  print(sensor.format_result(x, y, z))

The above will produce a line similar to::

  X: -300.8398, Y: 106.7199, Z: -3768.3181, Heading: 160° 28′

That's about it - everything else can be figured out from the code and the links below.


Resources
---------

- `Datasheet <https://cdn-shop.adafruit.com/datasheets/HMC5883L_3-Axis_Digital_Compass_IC.pdf>`
- `Sparkfun tutorial <https://www.sparkfun.com/tutorials/301>`
- `HMC5883L driver for the PyBoard <https://github.com/CRImier/hmc5883l>`


.. _adafruit-ampy: https://github.com/adafruit/ampy/tree/master/ampy
.. _HMC5883L_:     https://cdn-shop.adafruit.com/datasheets/HMC5883L_3-Axis_Digital_Compass_IC.pdf
.. _hmc5883l.py:   https://github.com/gvalkov/micropython-esp8266-hmc5883l/blob/master/hmc5883l.py


License
-------

All code and documentation released under the terms of the Revised BSD License.
