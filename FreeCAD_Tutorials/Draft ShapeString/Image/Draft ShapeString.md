# Draft ShapeString tutorial

Source: [Draft ShapeString tutorial - FreeCAD Documentation](https://wiki.freecad.org/Draft_ShapeString_tutorial)

## Introduction

This tutorial was originally written by Roland Frank ( † 2017, r-
frank), and it was rewritten and re-illustrated by vocx. I will now rewrite it to fix for FreeCAD version 0.20.2 and make some change I find help the flow

This tutorial describes a method to create 3D text and use it with
solid objects in the Part Workbench. We will discuss how to

* insert outlined text with the Draft ShapeString tool,
* extrude it to be a 3D solid with Part Extrude ,
* position it in 3D space using placement, and Draft Move (it uses a sketch as auxiliary geometry), and 
* engrave the text by applying a boolean Part Cut .

To use ShapeStrings inside the PartDesign Workbench, the process is essentially the same as with the Part Workbench, but the ShapeString is placed inside the PartDesign Body to extrude it. Go to the end of this tutorial for more information.

## Setup

* Open FreeCAD, create a new empty document with File → New, and switch to the **Part Workbench**.
  * Press the **View isometric button**, or **press 0** in the numerical pad of your
keyboard, to change the view to isometric to visualize the 3D solids better.
  * Press the **View fit all button** whenever you add objects in order to pan and zoom
the 3D view so that all elements are seen in the view.
  * Hold **Ctrl while you click to select multiple items**. If you selected something wrong or want to de-select everything, just click on empty space in the 3D view.

## Insert the ShapeString

* Switch to the **Draft Workbench**.
  * Make sure nothing is selected in the tree view.
  * Establish the working plane to XY (Top) by clicking on Top (XY). SelectPlane and pressing
* Insert the text **"FreeCAD"**.
  * Click on **ShapeString** .
  * Change **String** to **FreeCAD**; change **Height** to **5mm**; change **Tracking to 0mm**.
  * Make sure Font file points to a valid font, for example, **/usr/share/fonts/truetype/dejavu/DejaVuSans.ttf**. Press the ellipsis **[...]** to open the operating system's dialog to find a font.
  * Press [Reset point].
  * Press [OK] . This will create a ShapeString object.
  * Recompute the document by pressing [Refresh] .
  * To see the ShapeString from above change the view by pressing [Top (XY)] , or [2] in the keyboard.
  * To restore the view to isometric, press [View isometric] , or [0} in the keyboard. Text created as a ShapeString, that is, as a collection of edges in a plane.

## Create the solid 3D text

* Switch back to the **Part Workbench**.
  * In the **tree view**, select **ShapeString**, then press **[Extrude]** .
  * In the **Extrude** task panel go to 
    * **Direction**, choose **Along normal**;
    * **Length**, set **Along** to 2 mm;
    * tick the **Create solid** option.
  * Press OK . This will create an Extrude object.
  * In the tree view, select Extrude, in the View tab change the value of Line Width to 2.0.

## Positioning the solid text in 3D space

* Switch to the Sketcher Workbench.
  * In the tree view, select Extrude, and press Space in the keyboard to make it visible.
  * With Extrude still selected, in the Data tab of the property editor, click on the Placement value so the ellipsis button ... appears on the right and click on that button.
    * Tick the option Apply incremental changes.
    * Change the Rotation to Rotation axis with angle; Axis to Z (by setting the X, Y and Z values of the axis inputboxes to 0, 0 and 1 respectively, Z is the third inputbox), and Angle to 90 deg, then click on Apply . This will apply a rotation around the Z-axis, and will reset the Angle field to zero.
    * Change the Rotation to Rotation axis with angle; Axis to Y (by setting the X, Y and Z values of the axis inputboxes to 0, 1 and 0 respectively), and Angle to 45 deg, then click on Apply . This will apply a rotation around the Y-axis, and will reset the Angle field to zero.
    * Click on OK to close the dialog.

## Create the basic shape

* Insert a primitive cube by clicking on Box .
  * Select Cube in the tree view.
  * Change the dimensions in the Data tab of the property editor.
  * Change Width to 31 mm.
* Create a chamfer.
  * Select the upper edge (Edge6) on the front face of the Cube in the 3D view.
  * Press Chamfer .
  * In the Chamfer edges task panel go to Selection, choose Select edges. As Chamfer type choose Equal distance, then set Length to 5 mm.
  * Press OK . This will create a Chamfer object.
  * In the tree view, select Chamfer, in the View tab change the value of Line Width to 2.0.