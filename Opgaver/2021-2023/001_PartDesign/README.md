# Opgave 001 Part Design  

**I denne opgave skal vi arbejde med følgende tools:**

* [![Standard_menu_tools.png](../../Images/Standard_menu_tools.png)  Standardmenuen <br> er sammensat af 7 undermenuer. Hver undermenu har en dedikeret side.](https://wiki.freecadweb.org/Std_Base)
  * [Std File Menu](https://wiki.freecadweb.org/Std_File_Menu)
    * [![Std New](../../Images/Std_New.svg) Std New: Som opretter et nyt tomt dokument og gør det til det aktive dokument.](https://wiki.freecadweb.org/Std_New)
    * [![Std Save](../../Images/Std_Save.svg) Std Save: Som gemmer det aktive dokument.](https://wiki.freecadweb.org/Std_Save)
    * [![Std CloseActiveWindow](../../Images/Std_CloseActiveWindow.svg) Std CloseActiveWindow: Som lukker det aktive vindue. For at lukke et dokument skal alle dets vinduer være lukkede.](https://wiki.freecadweb.org/Std_CloseActiveWindow)
    * [![Std Save](../../Images/Std_CloseAllWindows.svg) Std CloseAllWindows: Som lukker alle vinduer og lukker derved alle dokumenter.](https://wiki.freecadweb.org/Std_CloseAllWindows)
* [![PartDesign.svg](../../Images/Workbench_PartDesign.svg) PartDesign Workbench](https://wiki.freecadweb.org/PartDesign_Workbench)
  * Part Design Helper tools
    * [![PartDesign Body.svg](../../Images/PartDesign_Body.svg) Create body: opretter et Body-objekt i det aktive dokument og gør det aktivt.](https://wiki.freecadweb.org/PartDesign_Body)
    * [![PartDesign NewSketch](../../Images/Sketcher_NewSketch.svg) Opret skitse: opretter en ny skitse på et valgt ansigt eller et valgt plan.](https://wiki.freecadweb.org/PartDesign_NewSketch)
    * [![Sketcher EditSketch](../../Images/Sketcher_EditSketch.svg) Denne kommando giver dig mulighed for at redigere en eksisterende skitse. Det åbner Sketcher-dialogen.](https://wiki.freecadweb.org/Sketcher_EditSketch)
  * Part Design Modeling tools
    * [![PartDesign Plane](../../Images/PartDesign_Plane.svg) PartDesign Plane.svg Opret et datumplan: opretter et datumplan i den aktive krop.](https://wiki.freecadweb.org/PartDesign_Plane)
  * Additive tools
    * [![Pad](../../Images/PartDesign_Pad.svg) Pad: Ekstruderer et solidt materiale fra en valgt skitse.](https://wiki.freecadweb.org/PartDesign_Pad)
  * Subtractive tools
    * [![Pocket](../../Images/PartDesign_Pocket.svg) Pocket: opretter en lomme ud fra en valgt skitse.](https://wiki.freecadweb.org/PartDesign_Pocket)
  * Transformation tools
    * [![Mirrored](../../Images/PartDesign_Mirrored.svg) Mirrored: spejler en eller flere funktioner.](https://wiki.freecadweb.org/PartDesign_Mirrored)
    * [![Linear Pattern](../../Images/PartDesign_LinearPattern.svg) Lineært mønster: opretter et lineært mønster af en eller flere funktioner.](https://wiki.freecadweb.org/PartDesign_LinearPattern)

I den første opgave skal vi tegne et skab, der har følgende mål:  

* Udvendig Højde: **600mm**  
* Udvendig Bredde: **300mm**  
* Udvendig Dybde: **300mm**  
* Matriale tykkelse: **12mm**  
* Bagbeklædning matriale tykkelse: **6mm**  
* Bagbeklædningen skal forsænkes **10mm** fra bagkant  
* Hjørne skal være 45°

## Opret ny opgave

* Klik på
  * File -> New

### Gem opgaven i ./Dokumenter/FreeCAD/Opgave_001

* File -> Save As
  * Vælg Dokument mappen
    * Klik på **Create New Folder**
      * Navngiv den nye Folder **FreeCAD**
      * File name: Opgave_001
      * ![Folder](./Images/OpgaveFolder.png)
      * Klik **Save**

## [![PartDesign_Body_Images](../../Images/PartDesign_Body.svg) PartDesign_Body - SkabsSide](https://wiki.freecad.org/PartDesign_Body)  

![SkabsSider](./Images/001.000_PartDesign_skabsSider.png)

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Sketch](https://wiki.freecad.org/Sketcher_NewSketch)

![Skabs Side Sketch](./Images/001.001_PartDesign_skabsSide_Sketch.png)

* Attachment  
  * Support: **XZ_Plane**  
* [Skabs højde: 600mm](https://wiki.freecad.org/Sketcher_ConstrainDistanceX)
* [plade tykelse: 12mm](https://wiki.freecad.org/Sketcher_ConstrainDistanceY)
* [vinkel i top og bund: 45°](https://wiki.freecad.org/Sketcher_ConstrainAngle)

### [![PartDesign_Pad_Images](../../Images/PartDesign_Pad.svg) PartDesign_Pad - Pad](https://wiki.freecad.org/PartDesign_Pad)

![Skabs Side Pad](./Images/001.002_PartDesign_skabsSide_Pad.png)

* Pad parameter
  * Type: **Dimention**
  * Length: **300mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal:  **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

### [![Sketcher_NewSketch_Image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Sketch001](https://wiki.freecad.org/Sketcher_NewSketch)

![Skabs Side Pocket](./Images/001.003_PartDesign_skabsSide_Pocket_Sketch.png)

* Attachment  
  * Support: **XZ_Plane**  
* Ydre kant på pocket: 300mm - 10mm = 290mm
  * skabsdybde: **300mm**
  * bagbeklædning afstand fra bagkant: **10mm**
  * bagbeklæbnings tykkelse: **6mm**

### [![Pocket images](../../Images/PartDesign_Pocket.svg) PartDesign_Pocket - Pocket](https://wiki.freecad.org/PartDesign_Pocket) 

![Skabs Side Pocket](./Images/001.004_PartDesign_skabsSide_Pocket.png)

* Pocket parameter
  * Type: **Through all**
  * Offset to face:
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Update view: **Checked**

### [![PartDesign_Plane_Image](../../Images/PartDesign_Plane.svg) PartDesign_Plane - DatumPlane](https://wiki.freecad.org/PartDesign_Plane) 

![Skabs Side Datumplane](./Images/001.005_PartDesign_skabsSide_DatumPlane.png)

* Support: **XY_Plane**
* Attachment Offset
  * Position
    * x: **0,00mm**
    * y: **0,00mm**
    * z: **12,00mm**

### [![Sketcher_NewSketch_Image](../../Images/Sketcher_NewSketch.svg)](https://wiki.freecad.org/PartDesign_NewSketch) PartDesign NewSketch - Sketch002  

![Skabs Side Pocket001 Sketch002](./Images/001.006_PartDesign_skabsSide_Pocket001_Sketch002.png)

* Attachment  
  * Support: **DatumPlane**  
* Huller
  * Placer 3 huller lodret over hinanden, med samme afstand
    * Contrain Vertically
    * Constrain Symmetrical
  * Hulcenter afstand fra top eller bund: **50mm**
  * Hulcenter afstand fra forkant & Bagbeklædning: **30mm**
  * Hulcenter afstand mellem yderste huller :  **300-10-6-30-30 = 224mm**
  * HulDiameter: **3mm**

### [![PartDesign_Pocket_Images](../../Images/PartDesign_Pocket.svg) PartDesign_Pocket - Pocket001](https://wiki.freecad.org/PartDesign_Pocket) 

![Skabs Side Pocket001](./Images/001.007_PartDesign_skabsSide_Pocket001.png)

* Pocket parameter
  * Type: **Dimension**
  * Length: **6,5mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal: **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Not Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

### [![PartDesign LinearPattern_Image](../../Images/PartDesign_LinearPattern.svg) PartDesign_LinearPattern](https://wiki.freecad.org/PartDesign_LinearPattern)

![Skabs Side LinearPattern](./Images/001.008_PartDesign_skabsSide_LinearPattern.png)  

* LinearPattern parameters  
  * Feature: **Pocket001**  
  * Direction: **Horizontal sketch axis**
  * Reverse direction: **Not Checked**
  * Length: **500,00mm (600-50-50)**
  * Occurrences: **21**
  * Update view: **Checked**



## [![PartDesign_Body_Images](../../Images/PartDesign_Body.svg) PartDesign_Body - SkabsBund](https://wiki.freecad.org/PartDesign_Body)  

![PartDesign_skabsBund.png](./Images/001.100_PartDesign_skabsBund.png)

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Skech003](https://wiki.freecad.org/Sketcher_NewSketch)

![skabsBund](./Images/001.101_PartDesign_skabsBund_Sketch003.png)

* Attachment  
  * Support: **XZ_Plane001**  
* Skabs bredde: **300mm**
* plade tykelse: **12mm**
* vinkel i højre og venstre: **45°**

### [![PartDesign_Pad_Images](../../Images/PartDesign_Pad.svg) PartDesign_Pad - Pad001](https://wiki.freecad.org/PartDesign_Pad)

![](./Images/001.102_PartDesign_skabsBund_Pad001.png)

* Pad parameter
  * Type: **Dimention**
  * Length: **300mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal:  **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Sketch004](https://wiki.freecad.org/Sketcher_NewSketch)

![](./Images/001.103_PartDesign_skabsBund_Pocket002_Sketch004.png)

* Attachment  
  * Support: **XZ_Plane**  
* Ydre kant på pocket: 300mm - 10mm = 290mm
  * skabsdybde: **300mm**
  * bagbeklædning afstand fra bagkant: **10mm**
  * bagbeklæbnings tykkelse: **6mm**

### [![Pocket images](../../Images/PartDesign_Pocket.svg) PartDesign_Pocket - Pocket002](https://wiki.freecad.org/PartDesign_Pocket) 

![](./Images/001.104_PartDesign_skabsBund_Pocket002.png)

* Pocket parameter
  * Type: **Through all**
  * Offset to face:
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Update view: **Checked**

## [![PartDesign_Body_Images](../../Images/PartDesign_Body.svg) PartDesign_Body - SkabsBagbeklædning](https://wiki.freecad.org/PartDesign_Body)  

![SkabsBagbekl%C3%A6dning.png](./Images/001.200_PartDesign_SkabsBagbekl%C3%A6dning.png)

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Sketch005](https://wiki.freecad.org/Sketcher_NewSketch)

![](./Images/001.201_PartDesign_SkabsBagbekl%C3%A6dning_Pad002_Sketch005.png)

* Attachment  
  * Support: **XZ_Plane002**  
* Mål
  * Dybde: **288mm (300-6-6)**
  * Højde: **600mm (600-6-6)**

### [![PartDesign_Pad_Images](../../Images/PartDesign_Pad.svg) PartDesign_Pad - Pad002](https://wiki.freecad.org/PartDesign_Pad)

![Pad002.png](./Images/001.202_PartDesign_SkabsBagbekl%C3%A6dning_Pad002.png)

* Pad parameter
  * Type: **Dimention**
  * Length: **6,00mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal:  **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

## [![PartDesign_Body_Images](../../Images/PartDesign_Body.svg) PartDesign_Body - SkabsHylde](https://wiki.freecad.org/PartDesign_Body)  

![SkabsHylde.png](./Images/001.300_PartDesign_SkabsHylde.png)  

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign_NewSketch - Sketch006](https://wiki.freecad.org/Sketcher_NewSketch)

![Sketch006.png](./Images/001.301_PartDesign_SkabsHylde_Pad003_Sketch006.png)

* Attachment  
  * Support: **XZ_Plane003**  
* Mål
  * HyldeBedde: **276mm (300-12-12)**
  * HyldeDybde: **284mm (300-10-6)**

### [![PartDesign_Pad_Images](../../Images/PartDesign_Pad.svg) PartDesign_Pad - Pad003](https://wiki.freecad.org/PartDesign_Pad)

![](./Images/001.302_PartDesign_SkabsHylde_Pad003.png)

* Pad parameter
  * Type: **Dimention**
  * Length: **12,00mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal:  **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) PartDesign NewSketch - Sketch007](https://wiki.freecad.org/Sketcher_NewSketch)

![Sketch007.png](./Images/001.303_PartDesign_SkabsHylde_Pocket003_Sketch007.png)

* Attachment  
  * Support: **XZ_Plane003**  
* Mål
  * Slot Afstand fra Kant: **30mm**
  * Slot Diameter: **3,20mm**
  * Afstand mellem Slot: **224mm (300-10-6-30-30)**
  * Slot Afstand fra kant: **15mm ((300-12-12)/2-15)**

### [![Pocket images](../../Images/PartDesign_Pocket.svg) PartDesign_Pocket - Pocket003](https://wiki.freecad.org/PartDesign_Pocket) 

![](./Images/001.304_PartDesign_SkabsHylde_Pocket003.png)

* Pocket parameter
  * Type: **Dimension**
  * Length: **3,2mm**
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
    * Length along sketch normal: **Checked**
  * Symmetric to plane: **Not Checked**
  * Reversed: **Not Checked**
  * Taper angle: **0,00°**
  * Update view: **Checked**

### [![Mirrored_Images](../../Images/PartDesign_Mirrored.svg) PartDesign Mirrored - Mirrored](https://wiki.freecad.org/PartDesign_Mirrored)

![](./Images/001.305_PartDesign_SkabsHylde_Mirrored.png)

* Mirrored parameters
  * Feature: **Pocket003**
  * Plane: **Vertical sketch axis**
  * Update view: **Checked**
