You can use Python and the `picamera` module to take photos with the Raspberry Pi and its Camera Module.

*[picamera]: A Python module to interface with the Raspberry Pi Camera Module


- Import the `PiCamera` class and create a `camera` object.

	```python
	from picamera import PiCamera

	camera = PiCamera()
	```

- To take a photo, you can use the `capture()` method. To do this, you need to tell Python where you would like the photo to be stored and what you would like it to be called. In this example below, the photo will be called `selfie.png` and will be stored in the `/home/pi/` directory.

	```python
	from picamera import PiCamera

	camera = PiCamera()
	camera.capture('home/pi/selfie.png')
    camera.close()
	```

- Run your code and then use either the File Manager or the Terminal to find the file `selfie.png`.
