# Opgave 007 - Simple fully parametric design with named constraints

Kilde: https://forum.freecadweb.org/viewtopic.php?t=51668

## Slutresultat
![Slutresultat](./Images/Slutresultat_2022-12-08%2019-19-12.png)

## Sketch
![Sketch](./Images/Sketch_2022-12-08_19-27-14.png)  

### Sketch_rod_radius 

* Diameter: 20,00 mm
* Name: rod_radius  
* ![Sketch_rod_radius](./Images/Sketch_rod_radius_2022-12-08_19-30-04.png)  

### Sketch_outer_ring_thickness

* Diameter: .Constraints.rod_radius / 4
* Name: outer_ring_thickness  
* ![Sketch_outer_ring_thickness](./Images/Sketch_outer_ring_thickness_2022-12-08_19-21-46.png)

## Sketch lodret højde

* Length: .Constraints.rod_radius / 2
* Name: lodret_hight  
* ![Pad](./Images/Sketch_lodret_hight_2022-12-08_19-24-17.png)

## Sketch001

![Sketch001_width](./Images/Sketch001_2022-12-08_19-38-28.png)

## Sketch001_Bredde

* Length: Sketch.Constraints.rod_radius + Sketch.Constraints.outer_ring_thickness * 2 + Sketch.Constraints.outer_ring_thickness * 3 / 2 + 2mm
* Name: bredde
* ![Fillet](./Images/Sketch001_bredde_2022-12-08_19-40-44.png)

## Sketch001_Højde

* Length: (Sketch.Constraints.rod_radius + Sketch.Constraints.outer_ring_thickness) * 2
* Name: hight
* ![Fillet001](./Images/Sketch001_hight_2022-12-08_19-43-51.png)

## Sketch001_Fillet

Radius: Sketch.Constraints.outer_ring_thickness / 4
![](./Images/Fillet_2022-12-08_19-49-30.png)
