# klipper-biqu-b1

configs are still a work-in-progress

## Things to verify before first print

- run pid calibration in the terminal. when calibration is finished, the temperature will be set to off automatically and always do SAVE_CONFIG to update the printer.cfg values

```
PID_CALIBRATE HEATER=extruder TARGET=230
PID_CALIBRATE HEATER=heater_bed TARGET=100
```

- Try homing all axis, make sure direction is fine, endstop are working, etc

- For BLTOUCH only, you can tune z offset with

```
Z_ENDSTOP_CALIBRATE

#Then change Z position with
TESTZ Z=-.1
# the value is in mm

#When value is perfect, save with
ACCEPT
```

PS: don't forget thermal expension, heat your bed and nozzle before running the calibration
