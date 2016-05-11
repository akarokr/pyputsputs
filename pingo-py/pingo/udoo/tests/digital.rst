=============
Basic usage
=============

Turn on a led for 1s
--------------------

::

	>>> import pingo
	>>> from time import sleep
	>>>
	>>> board = pingo.udoo.Udoo()
	>>> board.pins[13]
	<DigitalPin gpio40@13>
	>>>
	>>> led_pin = board.pins[13]
	>>> led_pin.set_mode(pingo.OUT)
	>>> led_pin.on()
	>>> led_pin.state
	'HIGH'
	>>> sleep(1)  # 1 second
	>>> led_pin.off()
	>>> led_pin.state
	'LOW'
