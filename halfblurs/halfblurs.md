# Half Blurs
Variations that generate specific shapes using polar coordinates. Unlike normal blurs, which ignore the input point, half blurs take the angle of the input point (theta) and compute a random distance (rho) within the shape. This allows some flexibility in coloring. They can be substituted for normal blurs in many flames; if it doesn't work, try adding some pre_blur to the transform to generate random angles (this is done for the examples here).

## cannabiscurve_wf
Shape resembling a cannabis leaf.

Type: 2D half blur  
Author: Andreas Maschke (thargor6)  
Date: 15 Jan 2012

[![](cannabiscurve-1.png)](cannabiscurve-1.flame)

| Parameter | Description |
| --- | --- |
| filled | 0 for an outline, 1 to fill in the shape |

https://mathworld.wolfram.com/CannabisCurve.html  

## cloverleaf_wf
Shape resembling a four leaf clover.

Type: 2D half blur  
Author: Andreas Maschke (thargor6)  
Date: 15 Jan 2012

[![](cloverleaf-1.png)](cloverleaf-1.flame)

| Parameter | Description |
| --- | --- |
| filled | 0 for an outline, 1 to fill in the shape |

## conic / conic2
Conic section shape (ellipse, parabola, or hyperbola)

Type: 2D half bluf  
Author: cyberxaos  
Date: 28 Jan 2007  

[![](conic-1.png)](conic-1.flame) [![](conic-2.png)](conic-2.flame)

Note that there is a different variation named "conic" which different from this one. This is probably why the Apophysis plugin is named conic2 (the variation is named "conic" in Apophysis versions where is it built-in, as well as JWildfire). There is also a variation named "Z_conic" which is the same as this one.

| Parameter | Description |
| --- | --- |
| eccentricity | Determines the conic section type: 1 for a parabola, less for an ellipse, more for a hyperbola. |
| holes | Set to 0.5 to generate two shapes, the main one on the left and one turned 180° on the right (a hyperbola naturally includes both). Set to 0 or 1 to show only the left or right shape. Go past 0 or 1 to create a hole. |

https://en.wikipedia.org/wiki/Conic_section  
https://www.youtube.com/watch?v=80Rd-fifUOE  
https://www.deviantart.com/morphapoph/art/Apo-Anim-friendly-Plugins-178559281  

## shape
General shape generator using the superformula.

Type: 2D half blur  
Author: cyberxaos  
Date: 18 Feb 2007  

[![](shape-1.png)](shape-1.flame) [![](shape-2.png)](shape-2.flame)

| Parameter | Description |
| --- | --- |
| m | Number of corners |
| n1, n2, n3 | Shaping variables |
| a, b | Stretch or contract the shape |
| holes | Puts a hole in the center if less than 0. (Although the default is 1, it works best to use 0 for no hole and a negative value to add a hole.) |

https://en.wikipedia.org/wiki/Superformula  
http://paulbourke.net/geometry/supershape/  
https://www.deviantart.com/fractal-resources/art/BD-s-Lazysusan-Shape-Script-102963146  
