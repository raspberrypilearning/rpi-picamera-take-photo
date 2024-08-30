The best Python library for controlling the Raspberry Pi Camera Module is `picamera-zero`. To get started, check out [this project guide](https://raspberrypifoundation.github.io/picamera-zero/hello_world/){:target="_blank"} for a handy walkthrough of how to use it.

#### Take a photo

- Import the `Picamzero` class and create a `camera` object.

```python
from picamzero import Camera

camera = Camera()

```

- To take a photo, you can use the `take_photo()` method. To do this, you need to tell Python where you would like the photo to be stored and what you would like it to be called. In this example below, the photo will be called `image.jpg` and will be stored in the `/home/pi/` directory by default.

```python
from picamzero import Camera

camera = Camera()
camera.take_photo("image.jpg")
```

- Run your code and then use either the File Manager or the Terminal to find the file `image.jpg`.

#### Documentation

- [https://raspberrypifoundation.github.io/picamera-zero](https://raspberrypifoundation.github.io/picamera-zero){:target="_blank"}