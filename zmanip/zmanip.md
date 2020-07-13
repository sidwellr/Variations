# Z Manipulation
Variations that manipulate only the z coordinate. All of these must be used with another variation to process x and y (even if linear to simply copy it).

## flatten / zclear
Flatten the other variations on the transform by setting the z coordinate to 0.

Type: 3D (sets z only)  
Author: Georg Kiehne (xyrus02)  
Date: 28 Jul 2013  

## extrude
Extrude the other variations on the transform by stretching the z coordinate.

Type: 3D (sets z only)  
Author: Georg Kiehne (xyrus02)  
Date: 26 Jul 2010  

[![](extrude-1.png)](extrude-1.flame)

| Parameter | Description |
| --- | --- |
| root_face | Density of the extruded face compared to the rest, from 0 (root face has no extra density) to 1 (only the root face) |

http://xyrus02.deviantart.com/art/Extrude-Plugin-for-Apophysis-172778628 (defunct)  

## inflateZ_1
Set z to tilt the plane forward, basing z mostly on y, but with some distortion.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

[![](inflateZ_1-1.png)](inflateZ_1-1.flame)

https://www.deviantart.com/aporev/art/3D-Plugins-Collection-One-138514007  

## inflateZ_2
Set z to tilt the plane diagonally.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

https://www.deviantart.com/aporev/art/3D-Plugins-Collection-One-138514007  

## inflateZ_3
Warp z to give a strong three dimensional effect.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

[![](inflateZ_3-1.png)](inflateZ_3-1.flame)

https://www.deviantart.com/aporev/art/3D-Plugins-Collection-One-138514007  

## inflateZ_4
Set z to create interleaved helix shapes.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

[![](inflateZ_4-1.png)](inflateZ_4-1.flame)

## inflateZ_5
Set z to give a gentle three dimensional wave shape.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

[![](inflateZ_5-1.png)](inflateZ_5-1.flame)

https://www.deviantart.com/aporev/art/3D-Plugins-Collection-One-138514007  

## inflateZ_6
Set z to give a rolling shape.

Type: 3D (sets z only)  
Author: Larry Berlin (aporev)  
Date: 28 Sep 2009  

[![](inflateZ_6-1.png)](inflateZ_6-1.flame)

https://www.deviantart.com/aporev/art/3D-Plugins-Collection-One-138514007  

## post_bumpmap_wf
Set z from an external bumpmap image.

Type: 3D (sets z only)  
Author: Andreas Maschke (thargor6)  
Date: 28 Feb 2012

[![](post_bumpmap_wf-1.png)](post_bumpmap_wf-1.flame)

| Parameter | Description |
| --- | --- |
| image_filename | Filename for the bumpmap image; it must exist with the same name whenever the flame is loaded |
| inlined_image | The bumpmap image, selected from a file like image_filename but the image itself is stored in the flame, making the flame larger but more portable |
| scale_x | Horizontal scaling factor for bumpmap |
| scale_y | Vertical scaling factor for bumpmap |
| scale_z | Scale for mapping the bumpmap value to z |
| offset_x | Horizontal offset for bumpmap |
| offset_y | Vertical offset for bumpmap |
| offset_z | Offset for mapping the bumpmap value to z |
| reset_z | 0: Add bumpmap to existing z value<br>1: Override existing z value with bumpmap |

[Bumpmap image](gray-and-black-marble-slab-1451474.jpg) used for above example, from [pexels.com](https://www.pexels.com/).

## zcone
Add the x-y distance of each point to z, thus transforming the plane into a cone.

Type: 3D (sets z only)  

## zscale
Multiply the z value by the variation amount.

Type: 3D (sets z only)  

Pre_zscale and post_zscale_wf also exist to scale z before or after the other variations.

## ztranslate
Add the variation amount to z, translating points up or down the z axis.

Type: 3D (sets z only)  

[![](ztranslate-1.png)](ztranslate-1.flame)

Pre_ztranslate and post_ztranslate_wf also exist to translate z before or after the other variations.
