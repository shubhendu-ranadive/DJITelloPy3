# DJITelloPy
DJI Tello drone python 3 interface using the official [Tello SDK](https://dl-cdn.ryzerobotics.com/downloads/tello/20180910/Tello%20SDK%20Documentation%20EN_1.3.pdf) and [Tello EDU SDK](https://dl-cdn.ryzerobotics.com/downloads/Tello/Tello%20SDK%202.0%20User%20Guide.pdf). This library has the following features:

- implementation of all tello commands
- retrieve a video stream
- receive and parse state packets
- support for python >= 3.6

Feel free to contribute!

## Install in developer mode
Using the commands below you can install the repository in an _editable_ way. This allows you to modify the library and use the modified version as if you had installed it regularly.

```
git clone https://github.com/shubhendu-ranadive/DJITelloPy3.git
cd DJITelloPy3
pip install -e .
```

### Simple example
```python
from djitellopy import Tello

tello = Tello()

tello.connect()
tello.takeoff()

tello.move_left(100)
tello.rotate_counter_clockwise(90)
tello.move_forward(100)

tello.land()
```
### More examples
In the [examples](examples/) directory there are some code examples.
Comments in the examples are mostly in both english and chinese.

- [taking a picture](examples/take-picture.py)
- [recording a video](examples/record-video.py)
- [simple controlling using your keyboard](examples/manual-control-opencv.py)

### Notes
- If you are using the ```streamon``` command and the response is ```Unknown command``` means you have to update the Tello firmware. That can be done through the Tello app.
