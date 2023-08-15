# Notepad and Penholder, FreeCAD with Spreadsheet

Here I will try to create a fully parametric FreeCAD model, using FreeCAD ver. 0.21.0 with Spreadsheet

## Preferences

* Sketcher -> Display -> Font size: **17px to 22px**
* Sketcher -> Colors -> Expression dependent constraint -> HTML: **#ff7f26 to #00ff00**
* Sketcher -> Colors ->  -> HTML: **#ff2600 to #00ff00**
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

## Spreadsheet Cell properties

### Display unit

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
|:---|:---|---:|:---:|
|1|**Name (Alias)**|**Value**||
|2|NotePadWidth|80||
|3|NotePadHight|80 ||NotePadCutRadius
|4|NotePadBorder|2||
|5|NotePadPadLength|15||
|6|NotePadCutRadius|5||

|7|NotePadHexagonToolsize|15||
|8|NotePadHexagonHight|36||

|10|NotePadHexagon1Hole|10||

## NotePadHolder

### CutOut

## Hexagon

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

