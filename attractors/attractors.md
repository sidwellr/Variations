# Attractors
These variations use the formulas for strange attractors. They are mostly normal variations, not blurs, and will produce the actual attractor when used on a single transform by themselves with no affine transforms, as is done with all of the examples shown here. But their use is, of course, not restricted to this. The parameters mostly define the attractor and have no specific meaning.

## clifford_js
Strange attractor attributed to Cliff Pickover.

Type: 2D  
Author: Jesus Sosa  
Date:  4 Nov 2017  

[![](clifford-1.png)](clifford-1.flame)

| Parameter | Description |
| --- | --- |
| a - d | Variables that define the attractor |

http://paulbourke.net/fractals/clifford/  

## gingerbread_man
An attractor that resembles a gingerbread man.

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](gingerbread_man-1.png)](gingerbread_man-1.flame)

https://mathworld.wolfram.com/GingerbreadmanMap.html  

## gumowski_mira
The strange attractor of Gumowski-Mira.

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](gumowski_mira-1.png)](gumowski_mira-1.flame)

https://www.openprocessing.org/sketch/195425/  
https://demonstrations.wolfram.com/StrangeAttractorOfGumowskiMira/  

## henon
Strange attractor discovered by Michel Hénon.

Type: 2D  
Author: Chris Johns (TyrantWave)  
Date: 6 Jun 2009

[![](henon-1.png)](henon-1.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor; set c to 1 for the classic Hénon map |

https://www.deviantart.com/tyrantwave/art/Henon-and-Lozi-Apo-Plugins-125039554  
https://mathworld.wolfram.com/HenonMap.html  
https://en.wikipedia.org/wiki/H%C3%A9non_map  

## hopalong
Hopalong attractor, also known as the Martin map.

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](hopalong-1.png)](hopalong-1.flame) [![](hopalong-2.png)](hopalong-2.flame)

| Parameter | Description |
| --- | --- |
| random | Setting random changes the other parameters to random values (the values will be the same for any value of random)
| a - c | Variables that define the attractor |
| startx, starty | Starting values for plotting the attractor

http://www.fraktalwelt.de/myhome/simpiter2.html  
https://www.youtube.com/watch?v=JhHugpABjDo  

## lorenz_js
Strange attractor first studied by Edward Lorenz.

Type: 3D Direct Color  
Author: Jesus Sosa  
Date: 12 Dec 2017  

[![](lorenz-1.png)](lorenz-1.flame)

Lorenz uses Euler's method to solve the Lorenz system of ordinary differential equations. Coloring is based on the resulting x and y values.

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor; a is sometimes known as the Prandtl number and b the Rayleigh number |
| h | Step size for the Euler approximation |
| centerx, centery | Offset for direct coloring |
| scale | Scale for direct coloring |

http://paulbourke.net/fractals/lorenz/  
https://en.wikipedia.org/wiki/Lorenz_system  
https://en.wikipedia.org/wiki/Euler_method  

## lozi
Strange attractor discovered by René Lozi.

Type: 2D  
Author: Chris Johns (TyrantWave)  
Date: 6 Jun 2009

[![](lozi-1.png)](lozi-1.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor; set c to 1 for the classic Lozi map |

https://www.deviantart.com/tyrantwave/art/Henon-and-Lozi-Apo-Plugins-125039554  
http://padyn.wikidot.com/lozi-maps  
https://mathworld.wolfram.com/LoziMap.html  

## macmillan
Perturbed McMillan map (studied by Edwin McMillan)

Type: 2D blur  
Author: Jesus Sosa  
Date: 29 Mar 2018  

[![](macmillan-1.png)](macmillan-1.flame)

| Parameter | Description |
| --- | --- |
| a - b | Variables that define the attractor |
| startx, starty | Starting point |

http://www.3d-meier.de/tut19/Seite158.html  

## pdj
Peter de Jong attractor

Type: 2D
Author: Scott Draves  
Date: Sept 2003  

[![](pdj-1.png)](pdj-1.flame)

| Parameter | Description |
| --- | --- |
| a - d | Variables that define the attractor |

http://paulbourke.net/fractals/peterdejong/  
https://www.algosome.com/articles/strange-attractors-de-jong.html  

## sattractor3D
Generate a 3D mesh from differential equations.

Type: 3D blur  
Author: Jesus Sosa  
Data: 21 Feb 2018

[![](sattractor3D-1.png)](sattractor3D-1.flame) [![](sattractor3D-2.png)](sattractor3D-2.flame)

| Parameter | Description |
| --- | --- |
| xformula | The formula to use for dx for the attractor differential equation; it returns the value for dx, and can use "x", "y", "z", and "param_a" through "param_h" as well as constants and standard math functions. Changing presetId will overwrite it with the preset formula. |
| yformula | The formula to use for dy for the attractor differential equation |
| zformula | The formula to use for dz for the attractor differential equation |
| presetId | The preset to use; set to -1 to not use a preset |
| steps | Number of thousands of steps to use in the curve |
| radius | Thickness of the curve |
| stepTime | Delta time for computing the curve |
| facets | Number of sides in the attractor curve |
| start_x, start_y, start_z | Initial values for x, y, and z |
| warmup | Number of steps to skip before plotting the attractor |
| param_a - param_h | Value for param_a through param_h in the formulas |
| scale_x, scale_y, scale_z | Scale factors for x, y, and z |
| offset_x, offset_y, offset_z | Offset for the attractor curve |
| subdiv_level |
| subdiv_smooth_passes |
| subdiv_smooth_lambda |
| subdiv_smooth_mu |
| blend_colormap | Not used |
| displ_amount | Not used |
| blend_displ_map | Not used |
| receive_only_shadows |

http://jwildfire.org/forum/viewtopic.php?f=23&t=2607  
https://github.com/thargor6/JWildfire/blob/master/src/org/jwildfire/create/tina/variation/plot/sattractor3d_wf_presets.txt  

## sattractor_js
A strange attractor attributed to Roger Bagula.

Type: 2D  
Author: Jesus Sosa  
Date: 21 Dec 2017

[![](sattractor-1.png)](sattractor-1.flame) [![](sattractor-2.png)](sattractor-2.flame)

| Parameter | Description |
| --- | --- |
| m | Symmetry of the attractor, integer between 2 and 12 |

http://paulbourke.net/fractals/henonattractor/  

## svensson_js
Johnny Svensson attractor, based on the Peter de Jong attractor.

Type: 2D  
Author: Jesus Sosa  
Date: 12 Dec 2017  

[![](svensson-1.png)](svensson-1.flame)

| Parameter | Description |
| --- | --- |
| a - d | Variables that define the attractor |

http://paulbourke.net/fractals/peterdejong/  

## threeply
A strange attractor named Three Ply

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](threeply-1.png)](threeply-1.flame) [![](threeply-2.png)](threeply-2.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor |

http://www.jamesh.id.au/fractals/orbit/threeply.html  
