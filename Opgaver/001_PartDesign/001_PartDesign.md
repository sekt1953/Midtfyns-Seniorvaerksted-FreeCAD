# Opgave 001 Part Design  

## SkabsSide  

### Sketch

![Skabs Side Sketch](./Images/001.001_PartDesign_skabsSide_Sketch.png)

* Attachment  
  * Support: **XZ_Plane**  
* Skabs højde: 600mm
* plade tykelse: 12mm
* vinkel i top og bund: 90 degre

### Pad

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
  * Taper angle: **0,00 degree**
  * Update view: **Checked**

### Pocket Sketch001

![Skabs Side Pocket](./Images/001.003_PartDesign_skabsSide_Pocket_Sketch.png)

* Attachment  
  * Support: **XZ_Plane**  
* Ydre kant på pocket: 300mm - 10mm = 290mm
  * 300mm skabsdybde
  * 10mm bagbeklædning forsænkelse
  * 6 mm bagbeklæbnings tykkelse

### Pocket  

![Skabs Side Pocket](./Images/001.004_PartDesign_skabsSide_Pocket.png)

* Pocket parameter
  * Type: **Through all**
  * Offset to face: 
  * Direction
    * Direction/egde: **Sketch normal**
    * Show direction: **Not Checked**
  * Symmetric to plane:
  * Reversed: **Checked**
  * Face:
  * Update view: **Checked**

### DatumPlane  

![Skabs Side Datumplane](./Images/001.005_PartDesign_skabsSide_DatumPlane.png)
* Support: **XY_Plane**
* Attachment Offset
  * Position
    * x: **0,00mm**
    * y: **0,00mm**
    * z: **12,00mm**

### Pocket001 Sketch002  

![Skabs Side Pocket001](./Images/001.006_PartDesign_skabsSide_Pocket001_Sketch002.png)

* Attachment  
  * Support: **DatumPlane**  
* Huller
  * Placer 3 huller lodret over hinanden, med samme afstand
    * Contrain Vertically
    * Constrain Symmetrical
  * Hulcenter afstand fra top eller bund: **50mm**
  * Hulcenter afstand fra forkant & Bagbeklædning: **30mm**
  * Hulcenter afstand mellem yderste huller :  **300-10-6-30 = 224mm**
  * HulDiameter: **3mm**

### Pocket001  

![]()
*