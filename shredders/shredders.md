# Shredders
Variations that shred the plane in various ways.

## checks
Divides the flame into a checkerboard and shifts half of the squares up and left and the other half down and right.

Type: 2D  
Author: Keeps Spencer (gossamer-light)  
Date: 19 Nov 2007  

[![](checks-1.png)](checks-1.flame)

| Parameter | Description |
| --- | --- |
| x | Horizontal shift amount |
| y | Vertical shift amount |
| size | Size of the squares which checks divides the flame into |
| rnd | Amount of randomness to add (horizontal for half the squares, vertical for the rest) |

[Archive of Apophysis plugin](https://web.archive.org/web/20101229095529/https://xyrus02.deviantart.com/art/Checks-The-fixed-version-138967784) (Wayback Machine)

## rings
Divide the flame into concentric rings and vary the size and width of each (obsolete).

Type: 2D  
Author: Scott Draves  
Date: 1 Dec 2004  

Rings is an early variation added before parameters were supported. It uses the O1 value from the pre-affine transform to control its operation. This also affects the flame, making it difficult to control. So it is recommended to use rings2 instead of rings for new flames.

## rings2
Divide the flame into concentric rings and vary the size and width of each.

Type: 2D  
Author: Scott Draves  
Date: 4 Nov 2005  

[![](rings2-1.png)](rings2-1.flame)

When val is 1.2247, the width of each ring matches the size of its neighbors so the rings touch without overlapping.

| Parameter | Description |
| --- | --- |
| val | Controls the size and width of the concentric rings:<br>0: Don't change the rings (makes rings2 the same as linear)<br>0-1: Each ring is shrunk but the width increases, making the rings overlap<br>1: Width of each ring is the same, but size is 0, making superimposed circles<br>>1: Rings are reflected across the origin and width decreases |

[Cpow/ring2 Tutorial](https://www.deviantart.com/guagapunyaimel/art/cpow-ring2-tutorial-192002748)  
[Julian Rings Tutorial](https://mfcreative.co.uk/apophysis/apophysis-tutorials/julian-rings-tutorial/)  
[Rings2 and Julian Guide](https://www.deviantart.com/clairejones/art/The-Rings2-and-Julian-Guide-62854687)  
[Rings2 and Curl Tutorial](https://www.deviantart.com/one-tough-one/art/Rings-2-and-Curl-Tutorial-52457896)  
[Julian Rings Apophysis Script](https://www.deviantart.com/cabintom/art/Julian-Rings-Script-65218145)  

## shredded
Shreds the flame into strips in the x, y, and z directions and scrambles them.

Type: 3D  
Author: Brad Stefanov  
Date: 14 Sep 2019  

[![](shredded-1.png)](shredded-1.flame)

| Parameter | Description |
| --- | --- |
| x1 | Scale for x before shredding |
| x2 | Scale for x after shredding |
| x3 | Scale for x after scrambling |
| x_blur_amount | Amount of x blur to add if blur is 1 |
| y1 | Scale for y before shredding |
| y2 | Scale for y after shredding |
| y3 | Scale for y after scrambling |
| y_blur_amount | Amount of y blur to add if blur is 1 |
| z1 | Scale for z before shredding |
| z2 | Scale for z after shredding |
| z3 | Scale for z after scrambling |
| z_blur_amount | Amount of z blur to add if blur is 1 |
| type | Selects the type of shredding to perform; allowed values are 0, 1, and 2 |
| blur | 0: Don't add blur (ignore _blur_amount parameters)<br>1: Add blur; the amount is controlled by the _blur_amount parameters |

[JWildfire forum post](https://jwildfire-forum.overwhale.com/viewtopic.php?f=23&t=2789)  

## shredlin
Divides the plane into horizontal and vertical strips and shrinks them.

Type: 2D  
Author: Anton Liasotskiy (zy0rg)  
Date: 15 Jul 2011  

[![](shredlin-1.png)](shredlin-1.flame)

| Parameter | Description |
| --- | --- |
| xdistance | Width of vertical strips before shrinking |
| xwidth | Shrink factor for vertical strips; 1 for no shrinking, negative to reverse them |
| ydistance | Height of horizontal strips before shrinking |
| ywidth | Shrink factor for horizontal strips; 1 for no shrinking, negative to reverse them |

[Apophysis plugin](https://www.deviantart.com/zy0rg/art/ShredLin-228579947)  

## shredrad
Divides the plane into wedges and shrinks them

Type: 2D  
Author: Anton Liasotskiy (zy0rg)  
Date: 15 Jul 2011  

[![](shredrad-1.png)](shredrad-1.flame)

| Parameter | Description |
| --- | --- |
| n | Number of wedges |
| width | Shrink factor for each wedge; 1 for no shrinking, negative to reverse them |

[Apophysis plugin](https://www.deviantart.com/zy0rg/art/ShredRad-228572887)
