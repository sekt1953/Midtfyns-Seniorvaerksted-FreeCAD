# Tegn en box for din elektronik

## Nyttige link

### Youtube Video: 
* [FreeCAD 0.20 For Beginners | 24 | Lid & Box / Enclosure | Threaded Holes Cross File Sub Shape Binder](https://www.youtube.com/watch?v=KzLWKKBtnxU&list=PLWuyJLVUNtc0UszswD0oD5q4VeWTrK7JC&index=26)

### FreeCAD using mathematical expressions
* [expressions](https://wiki.freecadweb.org/Expressions)
  * [Floor and ceiling functions](https://en.wikipedia.org/wiki/Floor_and_ceiling_functions)

## Body_PCB

|Sketch|
|:---:|
|![Sketch](./Images/Body_PCB/Body_PCB_2022-11-1_%2020-42-18.png)|


|Pad parameters|Pad|
|:---:|:---:| 
|![Pad parameters](./Images/Body_PCB/Body_PCB_2022-11-19_20-51-36.png)|![Pad](./Images/Body_PCB/Body_PCB_2022-11-19_20-43-08.png)|

|Combo View|
|:---:|
|![Application](./Images/Body_PCB/Body_PCB_2022-11-19_20-55-58.png)|

## Body_BOX

### Binder & Pad

|Sketch|
|:---:|
|![Sketch](./Images/Body_BOX/Body_BOX_2022-11-19_21-11-38.png)|

|Pad parameters|Pad|
|:---:|:---:| 
|![Pad parameters](./Images/Body_BOX/Body_BOX_2022-11-19_21-13-30.png)|![Pad](./Images/Body_BOX/Body_BOX_2022-11-19_21-16-40.png)|

|Combo View|
|:---:|
|![Application](./Images/Body_BOX/Body_BOX_2022-11-19_21-08-38.png)|

### AdditivePipe

|Sketch|
|:---:|
|![Sketch](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-29-17.png)|
|![Sketch](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-29-53.png)|
|![Sketch](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-35-27.png)|

|Pipe parameters|AdditivePipe|
|:---:|:---:| 
|![Pad parameters](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-38-14.png)|![Pad](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-35-44.png)|

|Combo View|
|:---:|
|![Application](./Images/Body_BOX/Body_BOX_Pipe_2022-11-19_21-37-57.png)|

### LinearPattern

|LinearPattern parameters|LinearPattern|
|:---:|:---:| 
|![Pad parameters](./Images/Body_BOX/Body_BOX_Linear_2022-11-19_22-08-23.png)|![Pad](./Images/Body_BOX/Body_BOX_Linear_2022-11-19_21-53-13.png)|

|Formula Length|Formula Occurrences|
|:---:|:---:| 
|![Pad parameters](./Images/Body_BOX/Body_BOX_Linear_2022-11-19_21-53-41.png)|![Pad](./Images/Body_BOX/Body_BOX_Linear_2022-11-19_21-53-57.png)|

|Combo View|
|:---:|
|![Application](./Images/Body_BOX/Body_BOX_Linear_2022-11-19_21-54-17.png)|

* Parameters:
  * Add feature: AdditivePipe
  * Direction: Base Z axis  
  * Reverse direction: True  
  * Length: 60,00 mm
    * Formula editor: Pad.Length
  * Occurrences: 4
    * Formula editor: ceil(Pad.Length / 15mm)

### Pocket

|Sketch|
|:---:|
|![Sketch](./Images/Body_BOX/Body_BOX_Pocket_2022-11-19_22-20-11.png)|

|Pocket parameters|Pocket|
|:---:|:---:| 
|![Pad parameters](./Images/Body_BOX/Body_BOX_Pocket_2022-11-19_22-21-03.png)|![Pad](./Images/Body_BOX/Body_BOX_Pocket_2022-11-19_22-20-50.png)|

|Combo View|
|:---:|
|![Application](./Images/Body_BOX/Body_BOX_Pocket_2022-11-19_22-24-38.png)|
