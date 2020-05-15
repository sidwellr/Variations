# Boarders
Divide the plane into squares or hexagons with borders.

## boarders
Divide the plane into squares with borders.

Type: 2D   
Author: Joel and Michael Faber   
Date: 16 Sep 2007   

Divide the plane into squares of size 1, and make a copy of each. Shrink one copy to half size and keep it in place. Poke a square hole in the other and expand it to make a frame around the first.

https://sourceforge.net/projects/apo-plugins/files/apo-plugins/80810/   
http://tyrantwave.deviantart.com/art/Apophysis-3D-Baseforms-Pack-113871861   

## boarders2 / pre_boarders2
Divide the plane into squares with borders, with parameters.

Type: 2D  
Author: Georg Kiehne (xyrus02)  
Date: 31 Jul 2010  

![](boarders2-1.png)

Divide the plane into squares of size 1, and make a copy of each. Scale both copies by parameter c, and keep one copy in place. Poke a square hole in the other, dividing it into four trapezoids meeting at the corners to form a frame. Move each trapezoid away from the center a distance specified by parameter left, expanding them to maintain a solid frame.

To imitate boarders, set all parameters to 0.5. To imitate linear, set c=1 and left=0.

| Parameter | Description |
| --- | --- |
| c | Scale factor, normally less than one to shrink the squares. |
| left | Offset value for the trapezoids that form the frame. |
| right | A density balancing factor for the square in the middle vs the frame. High values emphasize the frame (and may make the middle disappear completely); low values emphasize the square. |

http://xyrus02.deviantart.com/art/Boarders2-plugin-for-Apophysis-173427128    (defunct)

## dc_boarders
Presumably, a direct color version of boarders, but it appears to be the same as boarders.

Type: 2D, direct color  
Author: Georg Kiehne (xyrus02)  
Date: 30 Jun 2010  

http://xyrus-02.deviantart.com/art/DC-Collection-169594950 (defunct)   
https://sourceforge.net/p/apo-plugins/code/HEAD/tree/personal/georgkiehne/   

## tri_boarders2
Divide the plane into hexagons with borders.

Type: 2D  
Author: Alexey Ermushev (eralex61)  
Date: Early 2008  

Divide the plane into hexagons and make a copy of each. Shrink one copy and keep it in place. Poke a hexagonal hole in the other and expand it to make a frame around the first.

| Parameter | Description |
| --- | --- |
| radius | Radius of the hexagons  |
| width | Scale factor for the in-place hexagon |

https://eralex61.deviantart.com/art/Some-Plugins-76087119/ (defunct)   
http://nightmares06.deviantart.com/art/Bubble-Triboarders-Tutorial-99317545   
https://www.deviantart.com/djeaton3162/art/Glossy-TriBoarders-Script-76820857   
https://www.deviantart.com/djeaton3162/art/Tiled-Tri-Boarders-Script-76868935   

## xtrb
Divide the plane into hexagons with borders, with julian feature.

Type: 2D  
Author: Georg Kiehne (xyrus02)  
Date: 17 Nov 2012  

![](xtrb-1.png)

Xtrb is a cross between tri_boarders2 and julian. To imitate tri_boarders2, set power, dist, a, and b to 1 and the amount to the square root of the tri_boarders2 amount.

| Parameter | Description |
| --- | --- |
| power | Julian power (see [julian](../julia/julia.md#julian)) |
| radius | Radius of the hexagons |
| width | Scale factor for the in-place hexagons |
| dist | Distortion factor; increase to stretch the result |
| a and b | Control the angles in the hexagon shape calculation; change to use non-hexagon shapes  |

Bug: The amount is multiplied twice, which may cause unexpected results. To work around, set the amount to the square root of what would normally be used.

http://xyrus02.deviantart.com/art/XTrb-Plugin-for-Apophysis-136800563 (defunct)   
https://www.deviantart.com/bpclarke/art/BC-BDs-Spher-Loonie-Bwraps-Xtrb-Projective-Batch-2-310446818   
