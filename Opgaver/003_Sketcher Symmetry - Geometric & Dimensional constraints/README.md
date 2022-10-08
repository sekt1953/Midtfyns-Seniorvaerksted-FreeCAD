# ![Sketcher_Symmetry.svg](./Images/Icon64/Sketcher_Symmetry.png) Sketcher Symmetry - Geometric & Dimensional constraints

## ![Sketcher_Symmetry.svg](./Images/Icon32/Sketcher_Symmetry.png) [Sketcher Symmetry](https://wiki.freecadweb.org/Sketcher_Symmetry)

* Menuens placering: **Sketch → Sketcher tools → Symmetry**
* Standard genvej: **[Z],[S]**
* Beskrivelse: Spejler skitserer geometri med reference til en valgt linje eller skitseakse.
* Brug: 
  1. Vælg den geometri, der skal kopieres, og derefter en linje- eller skitseakse, der skal bruges som symmetriaksen.
  2. Tryk på Sketcher Symmetry-knappen eller vælg: **Sketch → Sketcher-værktøjer → Sketcher Symmetry** fra topmenuen.
  3. Den valgte geometri vil blive kopieret symmetrisk til den valgte linje eller skitseakse.  
  !! Bemærk, at der ikke tilføjes nogen ekstra symmetribegrænsning.

## Sketcher Tools, Geometries, Constraints brugt i denne opgave

* Tools
  * ![Sketcher_Symmetry.png](./Images/Icon32/Sketcher_Symmetry.png) [Symmetry:](https://wiki.freecadweb.org/Sketcher_Symmetry)  Kopierer et skitseelement symmetrisk til en valgt linje.
* Geometries
  * ![Sketcher_CreateLine.png](./Images/Icon32/Sketcher_CreateLine.png) [Line:](https://wiki.freecadweb.org/Sketcher_CreateLine)  Tegner et linjestykke mellem 2 punkter. Linjer er uendelige med hensyn til visse begrænsninger.
  * ![Sketcher_CompCreateArc.png](./Images/Icon32/Sketcher_CreateArc.png) [Create an arc](https://wiki.freecadweb.org/Sketcher_CompCreateArc) Tegner et buesegment fra centrum, radius, startvinkel og slutvinkel.
  * ![Sketcher_CreatePolyline.png](./Images/Icon32/Sketcher_CreatePolyline.png) [Polyline](https://wiki.freecadweb.org/Sketcher_CreatePolyline) Tegner en linje lavet af flere linjestykker.
  * ![Sketcher_ToggleConstruction.png](./Images/Icon32/Sketcher_ToggleConstruction.png) [Toggle construction geometry:](https://wiki.freecadweb.org/Sketcher_ToggleConstruction) Skifter skitsegeometri fra/til konstruktionstilstand. Konstruktionsgeometri er vist i blåt og kasseres uden for skitseredigeringstilstand.

* Geometric constraints
  * ![Sketcher_ConstrainCoincident.png](./Images/Icon32/Sketcher_ConstrainCoincident.png) [Coincident:](https://wiki.freecadweb.org/Sketcher_ConstrainCoincident) Sætter et punkt på (sammenfaldende med) et eller flere andre punkter.
  * ![Sketcher_ConstrainPointOnObject.png](./Images/Icon32/Sketcher_ConstrainPointOnObject.png) [Point on Object:](https://wiki.freecadweb.org/Sketcher_ConstrainPointOnObject) Sætter et punkt på et andet objekt såsom en linje, bue eller akse.
  * ![Sketcher_ConstrainVertical.png](./Images/Icon32/Sketcher_ConstrainVertical.png) [Vertical](https://wiki.freecadweb.org/Sketcher_ConstrainVertical) Begrænser de valgte linjer eller polylinjeelementer til en ægte lodret orientering. Mere end ét objekt kan vælges, før denne begrænsning anvendes.
  * ![Sketcher_ConstrainHorizontal.png](./Images/Icon32/Sketcher_ConstrainHorizontal.png) [Horizontal](https://wiki.freecadweb.org/Sketcher_ConstrainHorizontal) Begrænser de valgte linjer eller polylinjeelementer til en ægte vandret orientering. Mere end ét objekt kan vælges, før denne begrænsning anvendes.
  * ![Sketcher_ConstrainParallel.png](./Images/Icon32/Sketcher_ConstrainParallel.png) [Parallel](https://wiki.freecadweb.org/Sketcher_ConstrainParallel) Constrains two or more lines parallel to one another.
  * ![Sketcher_ConstrainPerpendicular.png](./Images/Icon32/Sketcher_ConstrainPerpendicular.png) [Perpendicular](https://wiki.freecadweb.org/Sketcher_ConstrainPerpendicular) Constrains two lines perpendicular to one another, or constrains a line perpendicular to an arc endpoint.
  * ![Sketcher_ConstrainBlock.png](./Images/Icon32/Sketcher_ConstrainBlock.png) [Block:](https://wiki.freecadweb.org/Sketcher_ConstrainBlock) it blocks an edge from moving, that is, it prevents its vertices from changing their current positions. It should be particularly useful to fix the position of B-Splines. 
* Dimensional constraints
  * ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceX.png) [Horizontal Distance:](https://wiki.freecadweb.org/Sketcher_ConstrainDistanceX) Fixer den vandrette afstand mellem to punkter eller linjeslutpunkter. Hvis kun ét element er valgt, indstilles afstanden til oprindelsen.
  * ![Sketcher_ConstrainDistanceY.png](./Images/Icon32/Sketcher_ConstrainDistanceY.png) [Vertical Distance:](https://wiki.freecadweb.org/Sketcher_ConstrainDistanceY) Fixer den lodrette afstand mellem 2 punkter eller linjeslutpunkter. Hvis kun ét element er valgt, indstilles afstanden til oprindelsen.
  * ![Sketcher_ConstrainDistance.png](./Images/Icon32/Sketcher_ConstrainDistance.png) [Distance:](https://wiki.freecadweb.org/Sketcher_ConstrainDistance) Definerer afstanden af en valgt linje ved at begrænse dens længde, eller definerer afstanden mellem to punkter ved at begrænse afstanden mellem dem.
  * ![Sketcher_ConstrainDiameter.png](./Images/Icon32/Sketcher_ConstrainDiameter.png) [Diameter:](https://wiki.freecadweb.org/Sketcher_ConstrainDiameter) Definerer diameteren af en valgt bue eller cirkel ved at begrænse diameteren.
  * ![Sketcher_ConstrainAngle.png](./Images/Icon32/Sketcher_ConstrainAngle.png) [Angle:](https://wiki.freecadweb.org/Sketcher_ConstrainAngle) Definerer den indre vinkel mellem to valgte linjer.

<hr>

## Her er billeder af de to typer Alu-Profiler som vi skal prøve at tegne

* 20x20x100mm Profil
* 20x40x100mm Profil

På de to tegninger herunder, har jeg indtastet de mål, vi har taget med en skydelærer, ud fra dem skulle det være en smal sag at tegne disse profiler. Som det fremgår at tegningerne er der rigtig mange symetri linier i profilerne, så lad os udnytte dette.


| Profil | Sketch | Pad |
| ---  | --- | --- |
|20x20 | ![20x20_Sketch.png](./Images/Sketch002/20x20_Sketch.png)| ![20x20_pad.png](./Images/Sketch002/20x20_pad.png) |
|20x40 | ![0x40_Sketch.png](./Images/Sketch002/20x40_Sketch.png) | ![20x40_Pad.png](./Images/Sketch002/20x40_Pad.png) |

## Konstruktionsgeometri

Vi skal starte med at tegne et 45deg udsnit af vores Alu-profil, så derfor opretter vi et par konstruktions linier. Senere kan vi så spejle vores tegning over denne linie.

* Vi starter med at tegne 2 construction linier
  1. Klik ![Sketcher_ToggleConstruction.png](./Images/Icon32/Sketcher_ToggleConstruction.png) så skifter skitsegeometri fra/til konstruktionstilstand. Konstruktionsgeometri er vist i **blåt** og kasseres uden for skitseredigeringstilstand.
  2. vælg ![Sketcher_CreateLine.png](./Images/Icon32/Sketcher_CreateLine.png) Line geometries tool til at tegne Konstruktionslinierne med med.
  3. Den første linie skla gå fra nul punkt (0.0,0.0) til ca. (15.0, 135.0 deg).
  4. næste linie skal starte ca. i (-4.0, 5.0), og slutte med vinkelret på den første line. Brug ![Sketcher_ConstrainPerpendicular.png](./Images/Icon32/Sketcher_ConstrainPerpendicular.png) Perpendicular constrain til at låse linien.
  5. Se billedet **Konstruktionsgeometri** herunder til venstre.

|Konstruktionsgeometri Combo View -> Task -> Constrains|
| --- |
|![Sketch-Symmetry-20x20_001.png](./Images/Sketch002/Sketch-Symmetry-20x20_001.png)|

## Sketch Start

* Klik ![Sketcher_ToggleConstruction.png](./Images/Icon32/Sketcher_ToggleConstruction.png) så skifter skitsegeometri fra konstruktionstilstand. 
  * Brug nu ![Sketcher_CreatePolyline.png](./Images/Icon32/Sketcher_CreatePolyline.png) og ![Sketcher_CreateArc.png](./Images/Icon32/Sketcher_CreateArc.png), til at tegne et 45 graders udsnit af vores Alu-Profile.
  * Se **Sketch Start** herunder

|Sketch Start|
| --- |
|![Sketch-Symmetry-20x20_002a.png](./Images/Sketch002/Sketch-Symmetry-20x20_002.png)|

## Geometric ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceX.png) Horizontal constraints & ![Sketcher_ConstrainDistanceY.png](./Images/Icon32/Sketcher_ConstrainDistanceY.png) Vertical constraints

* 3 Horizontal & 1 Vertical constraints
  * Brug nu ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceX.png) Horizontal constraints  & ![Sketcher_ConstrainDistanceY.png](./Images/Icon32/Sketcher_ConstrainDistanceY.png) Vertical constraints, så vi får låst alle vandrette og lodrette linier.
  * Se billedet herunder til venstre:

|Geometric constraints: (3 Horizontal, 1 Vertical)
|--- |
|![Sketch-Symmetry-20x20_003.png](./Images/Sketch002/Sketch-Symmetry-20x20_003.png)

## Geometric ![Sketcher_ConstrainParallel.png](./Images/Icon32/Sketcher_ConstrainParallel.png) Parallel constraints

* 2 Parallel constraints
  * brug nu ![Sketcher_ConstrainParallel.png](./Images/Icon32/Sketcher_ConstrainParallel.png) Parallel constraints til at få styr på de to skrå linier.
  * Se billedet herunder til højre:

|Geometric constraints: (2 Parallel)
|--- |
|![Sketch-Symmetry-20x20_004.png](./Images/Sketch002/Sketch-Symmetry-20x20_004.png)

## Geometric ![Sketcher_ConstrainCoincident.png](./Images/Icon32/Sketcher_ConstrainCoincident.png) Coincident constraints

* 2 Coincident  constraints
  * Brug nu ![Sketcher_ConstrainCoincident.png](./Images/Icon32/Sketcher_ConstrainCoincident.png) **Coincident  constraints** til at låse 3 punkter.
  * Se billedet herunder til venstre:

|Geometric constraints: (2 Coincident)|
|--- |
|![Sketch-Symmetry-20x20_005.png](./Images/Sketch002/Sketch-Symmetry-20x20_005.png)|

## Geometric ![Sketcher_ConstrainPointOnObject.png](./Images/Icon32/Sketcher_ConstrainPointOnObject.png) Point on object constraints

* 4 Point on object
  * Brug nu ![Sketcher_ConstrainPointOnObject.png](./Images/Icon32/Sketcher_ConstrainPointOnObject.png)  til at få låst de sidste 4 punkter.
  * Se billedet herunder til højre:

|Geometric constraints: (4 Point on object)|
|--- |
|![Sketch-Symmetry-20x20_006.png](./Images/Sketch002/Sketch-Symmetry-20x20_006.png)|

## Datums ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistance.png) Distance Constraints

* 1 Datum Distance (1,5mm / 2) Constrain
  * Brug nu ![Sketcher_ConstrainDistance.png](./Images/Icon32/Sketcher_ConstrainDistance.png) **Distance Constrain**

|Datum Distance Constraints: (1,5mm / 2)|
|--- |
|![Sketch-Symmetry-20x20_007.png](./Images/Sketch002/Sketch-Symmetry-20x20_007.png)|

## Datums ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceX.png) Horizontal Distance Constraints

* 2 Horizontal distance (6,4mm / 2) & (10,4mm / 2)
  * Brug nu ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceX.png) **Horizontal Distance Constrain**

|Datum Horizontal distance constraints (6,4mm / 2) & (10,4mm / 2)|
|--- |
|![Sketch-Symmetry-20x20_008.png](./Images/Sketch002/Sketch-Symmetry-20x20_008.png)|

## Datums ![Sketcher_ConstrainDistanceY.png](./Images/Icon32/Sketcher_ConstrainDistanceY.png) Vertical Distance Constraints

* 3 Datum Vertical Distance Constrain på 1,6mm & 5,0mm & 10,0mm
  * Brug nu ![Sketcher_ConstrainDistanceX.png](./Images/Icon32/Sketcher_ConstrainDistanceY.png) **Vertical Distance Constrain**

|Datum Vertical distance constraints på 1,6mm & 5mm & 10mm|
|--- |
|![Sketch-Symmetry-20x20_009.png](./Images/Sketch002/Sketch-Symmetry-20x20_009.png)|

## Datums ![Sketcher_ConstrainDiameter.png](./Images/Icon32/Sketcher_ConstrainDiameter.png) Diameter constraints

* 1 Datum Diameter Constrain på 4mm
  * Brug nu ![Sketcher_ConstrainDiameter.png](./Images/Icon32/Sketcher_ConstrainDiameter.png) **Diameter Constrain**

|Datum Diameter Constraints på 4mm|
|--- |
|![Sketch-Symmetry-20x20_010.png](./Images/Sketch002/Sketch-Symmetry-20x20_010.png)|

## Datum ![](./Images/Icon32/Sketcher_ConstrainAngle.png) Angle Constrain

* Lås nu konstruktions linien med ![Sketcher_ConstrainAngle.png](./Images/Icon32/Sketcher_ConstrainAngle.png) **Angle constrain** til en vinklen på 45deg i forhold til Y_Axis.  

|Datum Angle Constraints på 45deg|
|--- |
|![Sketch-Symmetry-20x20_011.png](./Images/Sketch002/Sketch-Symmetry-20x20_011.png)|

## Geometric Block constraints

* 9 Block
  * Brug nu ![Sketcher_ConstrainBlock.png](./Images/Icon32/Sketcher_ConstrainBlock.png) **Block Constrain**, vi skal bruge Block constrain for at holde vore sketh fully constrain efter Sketcher_Symmetry værktøjet.

|Datums 9 Block Constraints|
|--- |
|![Sketch-Symmetry-20x20_012.png](./Images/Sketch002/Sketch-Symmetry-20x20_012.png)|

<hr>

## Sketcher_Symmetry 20x20x100 Profile

|Fully Constrained<br> & Selected sketch|Sketcher_Symmetry<br>over Konstruktionslinie<br> Sketch->Sketcher Tools->Symmetry [Z],[S]|
| --- | --- |
|![Sketch-Symmetry-20x20_013a.png](./Images/Sketch002/Sketch-Symmetry-20x20_013a.png)|![Sketch-Symmetry-20x20_013b.png](./Images/Sketch002/Sketch-Symmetry-20x20_013b.png)||

|Symmetry over Y_Axis|
| --- |
|![Sketch-Symmetry-20x20_014.png](./Images/Sketch002/Sketch-Symmetry-20x20_014.png)|


|Symmetry over X_Axis|
| --- |
![Sketch-Symmetry-20x20_015.png](./Images/Sketch002/Sketch-Symmetry-20x20_015.png)|


|Symmetry 20x20x100 Pad|
| --- |
|![20x20_pad.png](./Images/Sketch002/20x20_pad.png)|

<hr>

## Sketcher_Symmetry 20x40x100 Profile

|Fully Constrained<br> & Selected sketch|Sketcher_Symmetry<br>over Konstruktionslinie<br> Sketch->Sketcher Tools->Symmetry [Z],[S]|
| --- | --- |
|![Sketch-Symmetry-20x20_013a.png](./Images/Sketch002/Sketch-Symmetry-20x20_013a.png)|![Sketch-Symmetry-20x20_013b.png](./Images/Sketch002/Sketch-Symmetry-20x20_013b.png)||

|Symmetry over Y_Axis|
| --- |
|![Sketch-Symmetry-20x20_014.png](./Images/Sketch002/Sketch-Symmetry-20x20_014.png)|

## Ret i Sketch, Slet liner og opret nye

|Slettet Linier|
| --- |
|![Sketch-Symmetry-20x40_01a.png](./Images/Sketch002/Sketch-Symmetry-20x40_01a.png)|

|Nye Linier|
| --- |
|![Sketch-Symmetry-20x40_01b.png](./Images/Sketch002/Sketch-Symmetry-20x40_01b.png)|

|Symmetry over X_Axis|
| --- |
|![Sketch-Symmetry-20x20_002.png](./Images/Sketch002/Sketch-Symmetry-20x40_002.png)|

|Symmetry over konstruktions linie|
| --- |
|![Sketch-Symmetry-20x20_003.png](./Images/Sketch002/Sketch-Symmetry-20x40_003.png)|

## Pad

|Symmetry 20x40x100 Pad|
| --- |
|![20x40_Pad.png](./Images/Sketch002/20x40_Pad.png)|

<hr>
