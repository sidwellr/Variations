# Blobs
These variations deform the plane by pinching it towards the origin, making a blob-like shape. The math is similar to that of [rose curves](rosecurve/rosecurve.md), but these are standard variations, not blurs.

## blob
Pushes and pulls the plane using a radial sine wave to make it look like a blob.

Type: 2D  
Date: 4 Nov 2005

[![](blob-1.png)](blob-1.flame) [![](blob-2.png)](blob-2.flame)

| Parameter | Description |
| --- | --- |
| low | Proportional height of the troughs of the waves. It is typically set less than 1, though this is not required. If less than 0, the blob will extend through the origin and out the other side, doubling the number of waves. |
| high | Proportional height of the crests of the waves. It is typically set a bit larger than 1, though this is not required. |
| waves | Number of waves. Normally an integer; if not, one of the waves will be cut off. |

The version built-in to Apophysis requires waves to be an integer. To avoid this, or for versions of Apophysis that do not include blob, use the blob_fl plugin.

Setting low and high to the same value will just scale the flame by that amount, with no deformation. Blob is the same as linear when low and high are both 1.

https://www.jwfsanctuary.club/variation-information/blob/  

## blob_fl
"Fluid" version of blob; allows fractional values for waves.

Type: 2D  
Author: Fred E (morphapoph)  
Date: 8 Sep 2010

| Parameter | Description |
| --- | --- |
| low | Proportional height of the troughs of the waves. It is typically set less than 1, though this is not required. If less than 0, the blob will extend through the origin and out the other side, doubling the number of waves. |
| high | Proportional height of the crests of the waves. It is typically set a bit larger than 1, though this is not required. |
| waves | Number of waves. Normally an integer; if not, one of the waves will be cut off. |

https://www.deviantart.com/morphapoph/art/Apo-Anim-friendly-Plugins-178559281  

## blob2
Modulate a flame using radial sine waves.

Type: 2D  
Author: Anton Liasotskiy (zy0rg)  
Date: 26 Jul 2011  

[![](blob2-1.png)](blob2-1.flame) [![](blob2-2.png)](blob2-2.flame)

| Parameter | Description |
| --- | --- |
| mode | The direction of the radial waves<br>-1: inwards<br>0: both directions<br>1: outwards |
| n | Number of waves |
| radius | Minimum radius where waves start |
| prescale | Exponential scaling for the waves |
| postscale | Linear scaling for the waves |
| symmetry | Shifts the waves; negative for inwards, positive for outwards; range -1 to 1 |
| compensation | Compensation when scaling from symmetry and prescale is too big; range 0 (no compensation) to 1 |

Tips from the author:

* mode=1 works best for creating flower shapes
* use linear variation on the same xForm to see both inwards and outwards pointed waves (otherwise the inward-pointed waves are just "mirrored" from the 0.0 point)

https://www.deviantart.com/zy0rg/art/Blob2-244765425  

## blob3D
A variant of blob that adds a 3D component.

Type: 3D (sets z)  
Author: Andreas Maschke (thargor6)  
Date: 2011  

[![](blob3D-1.png)](blob3D-1.flame) [![](blob3D-2.png)](blob3D-2.flame)

| Parameter | Description |
| --- | --- |
| low | Proportional height of the troughs of the waves. It is typically set less than 1, though this is not required. If less than 0, the blob will extend through the origin and out the other side, doubling the number of waves. |
| high | Proportional height of the crests of the waves. It is typically set a bit larger than 1, though this is not required. |
| waves | Number of waves. Normally an integer; if not, one of the waves will be cut off. |
