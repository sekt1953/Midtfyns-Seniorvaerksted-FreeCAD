# Notepad and Penholder, FreeCAD with Spreadsheet

Here I will try to create a fully parametric FreeCAD model, using FreeCAD ver. 0.21.0 with Spreadsheet

## Preferences

### General

* General -> Document -> General -> Create new document at start up: **Checked**

### Display

* Display -> Navigation -> Navigation -> 3D Navigation: **Mouse Blender**

### Start

* Start -> Start page option -> Options -> Switch workbench after loading: **Part Design**
* Start -> Start page option -> Options -> Close start page after loading: **Checked**

### Sketcher

* Sketcher -> Display -> Font size: **17px to 22px**
* Sketcher -> Colors -> Expression dependent constraint -> HTML: **#ff7f26 to #00ff00**
* Sketcher -> Colors -> Dimensional constraint -> HTML: **#ff2600 to #00ff00**

# Project

* Open FreeCAD in **[PartDesign Workbench](https://wiki.freecad.org/PartDesign_Workbench)**
  * Create a New Document
    * **[Create body](https://wiki.freecad.org/PartDesign_Body)**
      * **[Create sketch](https://wiki.freecad.org/PartDesign_NewSketch)**
        * Select XY-plane (Base plane)
          * Click [OK]
        * Click [Close]
      * Change to **[Spreadsheet Workbench](https://wiki.freecad.org/Spreadsheet_Workbench)**
        * **[CreateSheet](https://wiki.freecad.org/Spreadsheet_CreateSheet)**
  * Now save project first time
    * File -> Save As **[Ctrl + Shift + S]**

## Spreadsheet

### Cell properties -> Display unit

* Now enter some parameter for project
  * Click **Spreadsheet tab sheet**
  * Click **B** 
  * Right Click **B1**
    * Select **Properties**
    * Seelect **Display unit**
      * Enter **mm**
      * Click **[OK]**

### Parameter

||A|B|C|
|---:|:---|---:|---:|
|1|**Name (Alias)**|**Value**|
|2|**Notepad Box sketch**|
|3|nPadBoxWidth|80|
|4|nPadBoxHight|80|
|5|nPadBoxBorder|2|
|6|**Notepad Box Extrude**|
|7|nPadBoxPadLength|5|
|8|**Notepad foot Extrude**|
|9|nPadFootPadLenght|1|
|11|**Notepad Cut Sketch**|
|12|nPadFootCutRadius|5|
|13|**Pencil and pen holder sketch**|
|14|nHexagonToolsize|12|
|15|**Pencil and pen holder Extrude**|
|16|nHexagonPadLenght|36|
|17|**Pencil Holes Sketch**|
|18|nPencil tip lenght |18|
|19|nPencil1HoleDiameter |10|
|20|nPencil2TipDiameter |2|
|21|nPencil2HoleBottomDiameter|8|
|22|nPencil2HoleTopDiameter|8|
|23|nPencil3TipDiameter|3|
|24|nPencil3HoleBottomDiameter|9|
|25|nPencil3HoleTopDiameter|9|

## NotePadHolder

### CutOut

## Pen holder - Hexagon

* [Sketcher RectangularArray](https://wiki.freecad.org/Sketcher_RectangularArray)
  * Columns: **3**
  * Rows: **1**
  * Equal vertical/horizontal spacing: **Checked**
  * Constrain inter-element separation: **Checked**
  * Clone: **Unchecked**


### Datum Plane

* Datum plane parameters:
  * Plane: **XZ_Plane**
  * Attachment mode: **Plane face**
  * Attachment Offset (in local coordinates)
    * In z-direction: **(Spreadsheet.B3 / 2 + Spreadsheet.B7 / 2) * -1**

