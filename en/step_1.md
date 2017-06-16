You can use Python and the PiCamera module to take photos with the Raspberry Pi and its camera module.

*[PiCamera]: A Python module to interface with the Raspberry Pi Camera module


- Import the `PiCamera` class and create a `camera` object.

	```python
	from picamera import PiCamera

	camera = PiCamera()
	```


- To take a photo, you can use the `capture()` method. This requires you to tell Python where you would like the photo to be stored and what you would like it to be called.

	```python
	from picamera import PiCamera

	camera = PiCamera()
	camera.capture('home/pi/selfie.png')
	```

    In this case the photo will be called `selfie.png` and will be stored in the `/home/pi/` directory.

- Run your code and then use either the File Manager or the Terminal to find the file `selfie.png`
