# robot
Robot built based on [Propeller Activity Board](http://learn.parallax.com/activitybot)


# Troubleshooting

1) Add your user to dialout group in order to be able to push stuff to COM ports

```
sudo adduser MyUser dialout
```

2) Make sure that 'rw' rights are granted for COM ports

```
sudo chmod a+rw /dev/ttyUSB0
```
