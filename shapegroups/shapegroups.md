# Shape Groups
Variations that generate groups of shapes.

## circleRand
Random size circles in a grid.

Type: 2D blur  
Author: Alexey Ermushev (eralex61)  
Date: 17 Jun 2009  

[![](circleRand-1.png)](circleRand-1.flame)

| Parameter | Description |
| --- | --- |
| Sc | Overall scale for the circles |
| Dens | Circle density (0 to 1) |
| X, Y | Size of the grid; if Sc is 1, this will be the number of circles horizontally and vertically |
| Seed | Random number seed |

[Apophysis variation](https://www.deviantart.com/eralex61/art/Circles-Plugins-126273412)  

## gpattern
A grid pattern of polygons.

Type: 2D direct color blur  
Author: Jesus Sosa, inspired by a program by Lucia Tokárová  
Date: 15 May 2018  

[![](gpattern-1.png)](gpattern-1.flame) [![](gpattern-2.png)](gpattern-2.flame)

| Parameter | Description |
| --- | --- |
| string | Type of polygons to use for each row as a comma-separated list of numbers (3 for triange, 4 for square, etc.); the list will be repeated to fill all the rows |
| seed | Random number seed |
| width, height | Width and height of the grid to use |
| lineheight | Controls the size (both width and height) of the polygons |
| angle | Angle to rotate each polygon, in degrees |
| randPos | Maximum amount to randomly move each polygon left to right |
| randSize | Maximum amount to randomly shrink or enlarge each polygon |
| fill | 0: Do not fill polygons (outline only if outline is 1)<br>1: Fill polygons |
| outline | 0: Omit polygon outlines<br>1: Draw polygon outlines |
| fill color | Start color (gradient index) for filling polygons, between 0 and 1 |
| fill color speed | Maximum amount to randomly vary fill color, between 0 (single color) and 1 (use full gradient) |
| outline color | Outline color (gradient index), between 0 and 1 |
