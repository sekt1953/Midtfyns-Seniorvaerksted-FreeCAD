# Grbl-Settings

## Kilde

* [www.sainsmart.com](https://www.sainsmart.com/blogs/news/grbl-v1-1-quick-reference)

|Settings|Description|
|:---:|:---|
|$0|Step pulse, microseconds|
|$1|Step idle delay, milliseconds
|$2|Step port invert, XYZmask*
|$3|Direction port invert, XYZmask* 
||The direction each axis moves.|
|$4|Step enable invert, (0=Disable, 1=Invert)
|$5|Limit pins invert, (0=N-Open. 1=N-Close)
|$6|Probe pin invert, (0=N-Open. 1=N-Close)
|$10|Status report, ‘?’ status.  0=WCS position, 1=Machine position, 2= plan/buffer and WCS position, 3=plan/buffer and  Machine position.|
|$11|Junction deviation, mm|
|$12|Arc tolerance, mm|
|$13|Report in inches, (0=mm. 1=Inches)**|
|$20|Soft limits, (0=Disable. 1=Enable, Homing must be enabled)|
|$21|Hard limits, (0=Disable. 1=Enable)|
|$22|Homing cycle, (0=Disable. 1=Enable)|
|$23|Homing direction invert, XYZmask* Sets which corner it homes to.|
|$24|Homing feed, mm/min|
|$25|Homing seek, mm/min|
|$26|Homing debounce, milliseconds|
|$27|Homing pull-off, mm|
|$30|Max spindle speed, RPM|
|$31|Min spindle speed, RPM|
|$32|Laser mode, (0=Off, 1=On)|
|$100|Number of X steps to move 1mm|
|$101|Number of Y steps to move 1mm|
|$102|Number of Z steps to move 1mm|
|$110|X Max rate, mm/min|
|$111|Y Max rate, mm/min|
|$112|Z Max rate, mm/min|
|$120|X Acceleration, mm/sec^2|
|$121|Y Acceleration, mm/sec^2|
|$122|Z Acceleration, mm/sec^2|
|$130|X Max travel, mm Only for Homing and Soft Limits.|
|$131|Y Max travel, mm Only for Homing and Soft Limits.|
|$132|Z Max travel, mm Only for Homing and Soft Limits.|

* XYZmask is a value setting for the X Y and Z axes. Change if an axis is moving in the wrong direction. Value will be 0-7. ** Reporting units are independent of the units set in the Gcode!