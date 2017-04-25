# Taking a photograph with PiCamera

You can use Python and the PiCamera module to take photos with the Raspberry Pi and it's camera module.

*[PiCamera]: A [python module](https://picamera.readthedocs.io/en/release-1.13/) to interface with the Raspberry Pi Camera module

[Open IDLE](link-to-IDLE-OPEN-Resource) for the Raspberry Pi Menu and then create a new file.

1. The first thing you need to do is to import the `PiCamera` class and create a `camera` object.

	~~~python
	from picamera import PiCamera

	camera = PiCamera()
	~~~

1. Before you take a picture, it is often a good idea to visualise what the camera sees. To do this you can use the `start_preview()` and `stop_preview()` methods. Before doing this though, you'll need to also import the `sleep` method from the `time` module, so that you can have a pause between the preview opening and closing.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview()
	sleep(2)
	camera.stop_preview()
	~~~

1. Save and run the code and you should see the view from the PiCamera displayed on the screen. It is important to note, however, that the picture is not rendered to your Desktop in a window. This means there's no handy `X` to click on if you want to close the preview. Sometimes you might have bugs in your code that cause your program to crash before the preview is closed, and it can then be tricky to use your operating system. To help out here, you can make the preview slightly transparent. This means if your code crashes, it's easy to find the Python shell and close it, which will kill the preview. To make the preview transparent, you can provide it with an `alpha` value.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview(alpha=190)
	sleep(2)
	camera.stop_preview()
	~~~
	
1. To take a photo, you can use the `capture()` method. This requires you to tell Python where you would like the photo to be stored and what you would like it to be called. In this case it's going to be called `selfie.png` and stored in the user's `home directory`. [Have a look at this [explanation](link-to-file-paths-ingredient) of how Linux and other Unix like operating systems store files if you want to know more.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview(alpha=190)
	camera.capture('home/pi/selfie.png')
	sleep(2)
	camera.stop_preview()
	~~~

1. Run your code and then use either the File Manager or the Terminal to find your `selfie.png`. Opening it should reveal you smiling features.
