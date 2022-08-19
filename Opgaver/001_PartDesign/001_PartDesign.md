# Opgave 001 Part Design  

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

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) Sketcher_New - Sketch](https://wiki.freecad.org/Sketcher_NewSketch)

![Skabs Side Sketch](./Images/001.001_PartDesign_skabsSide_Sketch.png)

* Attachment  
  * Support: **XZ_Plane**  
* Skabs højde: 600mm
* plade tykelse: 12mm
* vinkel i top og bund: 45°

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

### [![Sketcher_NewSketch_Image](../../Images/Sketcher_NewSketch.svg) Sketcher_NewSketch - Pocket_Sketch001](https://wiki.freecad.org/Sketcher_NewSketch)

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

### [![Sketcher_NewSketch_Image](../../Images/Sketcher_NewSketch.svg)](https://wiki.freecad.org/PartDesign_NewSketch) Sketcher_NewSketch - Pocket001_Sketch002  

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

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) Sketcher_New - Skech003](https://wiki.freecad.org/Sketcher_NewSketch)

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

### [![Sketcher image](../../Images/Sketcher_NewSketch.svg) Sketcher_New - Pocket002 Sketch004](https://wiki.freecad.org/Sketcher_NewSketch)

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

## Body_SkabsBagbeklædning

![](./Images/001.200_PartDesign_SkabsBagbekl%C3%A6dning.png)

### Pad002 Sketch005

![](./Images/001.201_PartDesign_SkabsBagbekl%C3%A6dning_Pad002_Sketch005.png)

* Attachment  
  * Support: **XZ_Plane002**  
* Mål
  * Dybde: **288mm (300-6-6)**
  * Højde: **600mm (600-6-6)**

### Pad002

![](./Images/001.202_PartDesign_SkabsBagbekl%C3%A6dning_Pad002.png)

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

## Body_SkabsHylde

![](./Images/001.300_PartDesign_SkabsHylde.png)  

### Pad002 Sketch005

![](./Images/001.301_PartDesign_SkabsHylde_Pad003_Sketch006.png)

* Attachment  
  * Support: **XZ_Plane003**  
* Mål
  * HyldeBedde: **276mm (300-12-12)**
  * HyldeDybde: **284mm (300-10-6)**

### Pad003

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

### Pocket003 Sketch007

![](./Images/001.303_PartDesign_SkabsHylde_Pocket003_Sketch007.png
)

* Attachment  
  * Support: **XZ_Plane003**  
* Mål
  * Slot Afstand fra Kant: **30mm**
  * Slot Diameter: **3,20mm**
  * Afstand mellem Slot: **224mm (300-10-6-30-30)**
  * Slot Afstand fra kant: **15mm ((300-12-12)/2-15)**

### Pocket003

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

### Mirrored

![](./Images/001.305_PartDesign_SkabsHylde_Mirrored.png)

* Mirrored parameters
  * Feature: **Pocket003**
  * Plane: **Vertical sketch axis**
  * Update view: **Checked**
