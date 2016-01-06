# robot

Robot built based on [Propeller Activity Board](http://learn.parallax.com/activitybot)


## Encoder Ticks and Distance

The ActivityBot updates the motor speeds 50 times per second, based on encoder feedback, to correct any small differences between how far it should have turned and how far it actually has turned.

Each encoder tick makes the wheel travel 3.25 mm forward. Remember, an encoder tick is counted when the encoder sensor detects a transition from spoke to hole or hole to spoke.  Since there are 32 spokes and 32 holes, there’s a total of 64 encoder ticks per wheel turn.

```
ticks = distance mm ÷ 3.25 mm/tick
```

The ActivityBot’s turning radius is typically 105.8 mm.

a) 360 degree turn:

```
r = 105.8 mm

2 × π × 105.8 mm ≈ 664.76 mm

664.76 mm ÷ 3.25 mm/tick ≈ 204.54 ticks ≈ 205 ticks.
```

b) 90 degree turn:

```
664.76 mm ÷ 4 ≈ 166.2 mm

166.2 mm ÷ 3.25 mm/tick ≈ 51.14 ticks ≈ 51 ticks.
```

## Whiskers

Robot able to dodge obstacles using whiskers.

![alt tag](https://github.com/m-wrona/robot/blob/master/img/assembly/IMG_20151220_080047.jpg)

## Troubleshooting

1) Add your user to dialout group in order to be able to push stuff to COM ports

```
sudo adduser MyUser dialout
```

2) Make sure that 'rw' rights are granted for COM ports

```
sudo chmod a+rw /dev/ttyUSB0
```
