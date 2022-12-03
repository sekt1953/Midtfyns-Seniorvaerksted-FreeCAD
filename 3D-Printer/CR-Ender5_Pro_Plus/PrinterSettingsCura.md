# Start & End G-code

## Marlin G-code index

[Marlin G-code index](https://marlinfw.org/meta/gcode/)

## Creality CR-10 Mini

### M503 - Report Settings

```text
Send: M503
Recv: echo:Steps per unit:
Recv: echo:  M92 X80.00 Y80.00 Z400.00 E143.00
Recv: echo:Maximum feedrates (mm/s):
Recv: echo:  M203 X500.00 Y500.00 Z5.00 E25.00
Recv: echo:Maximum Acceleration (mm/s2):
Recv: echo:  M201 X500 Y500 Z100 E5000
Recv: echo:Acceleration: S=acceleration, T=retract acceleration
Recv: echo:  M204 S500.00 T500.00
Recv: echo:Advanced variables: S=Min feedrate (mm/s), T=Min travel feedrate (mm/s), B=minimum segment time (ms), X=maximum XY jerk (mm/s),  Z=maximum Z jerk (mm/s),  E=maximum E jerk (mm/s)
Recv: echo:  M205 S0.00 T0.00 B20000 X20.00 Z0.40 E5.00
Recv: echo:Home offset (mm):
Recv: echo:  M206 X0.00 Y0.00 Z0.00
Recv: echo:PID settings:
Recv: echo:   M301 P21.73 I1.54 D76.55
Recv: ok
```


### Start G-code

```text
M201 X500.00 Y500.00 Z100.00 E5000.00 ;Setup machine max acceleration
M203 X500.00 Y500.00 Z10.00 E50.00 ;Setup machine max feedrate
M204 P500.00 R1000.00 T500.00 ;Setup Print/Retract/Travel acceleration
M205 X8.00 Y8.00 Z0.40 E5.00 ;Setup Jerk
M220 S100 ;Reset Feedrate
M221 S100 ;Reset Flowrate

;*** Start Preheating ***
M140 S{material_bed_temperature}; the bed
M104 S{material_print_temperature}; the hotend
G28 ;Home
M190 S{material_bed_temperature}; bed wait
M109 S{material_print_temperature}; hotend wait
;*** End Preheating

G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
G1 X10.1 Y20 Z0.28 F5000.0 ;Move to start position
G1 X10.1 Y200.0 Z0.28 F1500.0 E15 ;Draw the first line
G1 X10.4 Y200.0 Z0.28 F5000.0 ;Move to side a little
G1 X10.4 Y20 Z0.28 F1500.0 E30 ;Draw the second line
G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
```

### End G-code

```text
G91 ;Relative positioning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more
G90 ;Absolute positioning

G1 X0 Y{machine_depth} ;Present print
M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z
```

## Creality Ender-5 Plus

* Start G-code forklaring 
  * Init Printer
    * [M201 - Print Move Limits](https://marlinfw.org/docs/gcode/M201.html)
    * [M203 - Set Max Feedrate](https://marlinfw.org/docs/gcode/M203.html)
    * [M204 - Set Starting Acceleration](https://marlinfw.org/docs/gcode/M204.html)
    * [M205-Set Advanced Settings](https://marlinfw.org/docs/gcode/M205.html)
    * [M220 - Set Feedrate Percentage](https://marlinfw.org/docs/gcode/M220.html)
    * [M221 - Set Flow Percentage](https://marlinfw.org/docs/gcode/M221.html)
  * Start Preheating
    * [M104 - Set Hotend Temperature](https://marlinfw.org/docs/gcode/M104.html)
    * [M140 - Set Bed Temperature](https://marlinfw.org/docs/gcode/M140.html)
    * [G28 - Auto Home](https://marlinfw.org/docs/gcode/G028.html)
    * [M420 - Bed Leveling State](https://marlinfw.org/docs/gcode/M420.html)
    * [M109 - Wait for Hotend Temperature](https://marlinfw.org/docs/gcode/M109.html)
    * [M190 - Wait for Bed Temperature](https://marlinfw.org/docs/gcode/M190.html)
  * Draw two line to the left
    * [G92 - Set Position (E0 - New extruder position)](https://marlinfw.org/docs/gcode/G092.html)
    * [G1 - Linear Move](https://marlinfw.org/docs/gcode/G000-G001.html)
    * [G92 - Set Position (E0 - New extruder position)](https://marlinfw.org/docs/gcode/G092.html)
    * [G1 - Linear Move](https://marlinfw.org/docs/gcode/G000-G001.html)

### Start G-code

```text
M201 X500.00 Y500.00 Z100.00 E5000.00 ;Setup machine max acceleration
M203 X500.00 Y500.00 Z10.00 E50.00 ;Setup machine max feedrate
M204 P500.00 R1000.00 T500.00 ;Setup Print/Retract/Travel acceleration
M205 X8.00 Y8.00 Z0.40 E5.00 ;Setup Jerk
M220 S100 ;Reset Feedrate
M221 S100 ;Reset Flowrate

;*** Start Preheating ***
M140 S{material_bed_temperature}; the bed
M104 S{material_print_temperature}; the hotend
G28 ;Home
M420 S1 Z2 ;Enable ABL using saved Mesh and Fade Height
M190 S{material_bed_temperature}; bed wait
M109 S{material_print_temperature}; hotend wait
;*** End Preheating

G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
G1 X10.1 Y20 Z0.28 F5000.0 ;Move to start position
G1 X10.1 Y200.0 Z0.28 F1500.0 E15 ;Draw the first line
G1 X10.4 Y200.0 Z0.28 F5000.0 ;Move to side a little
G1 X10.4 Y20 Z0.28 F1500.0 E30 ;Draw the second line
G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
```

* End G-code forklaring
  * Relative positioning
    * [G91 - Relative Positioning](https://marlinfw.org/docs/gcode/G091.html)
    * [G1 - Linear Move](https://marlinfw.org/docs/gcode/G000-G001.html)
  * Absolute positioning
    * [G90 - Absolute Positioning](https://marlinfw.org/docs/gcode/G090.html) 
    * [G1 - Linear Move](https://marlinfw.org/docs/gcode/G000-G001.html)
  * Turn-off
    * [M106 - Set Fan Speed](https://marlinfw.org/docs/gcode/M106.html)
    * [M104 - Set Hotend Temperature](https://marlinfw.org/docs/gcode/M104.html)
    * [M140 - Set Bed Temperature](https://marlinfw.org/docs/gcode/M140.html)
  * Disable all steppers but Z
    * [M18, M84 - Disable steppers](https://marlinfw.org/docs/gcode/M018.html)


### End G-code

```text
G91 ;Relative positioning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more

G90 ;Absolute positioning
G1 X{machine_width} Y{machine_depth} ;Present print

M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z
```
