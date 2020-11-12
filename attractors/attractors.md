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

[Description and examples by Paul Bourke](http://paulbourke.net/fractals/clifford/)  

## gingerbread_man
An attractor that resembles a gingerbread man.

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](gingerbread_man-1.png)](gingerbread_man-1.flame)

[MathWorld description](https://mathworld.wolfram.com/GingerbreadmanMap.html)  

## gumowski_mira
The strange attractor of Gumowski-Mira.

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](gumowski_mira-1.png)](gumowski_mira-1.flame)

[Processing sketch by David Burnett](https://www.openprocessing.org/sketch/195425/)  
[Wolfram interactive demonstration](https://demonstrations.wolfram.com/StrangeAttractorOfGumowskiMira/)  

## henon
Strange attractor discovered by Michel Hénon.

Type: 2D  
Author: Chris Johns (TyrantWave)  
Date: 6 Jun 2009

[![](henon-1.png)](henon-1.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor; set c to 1 for the classic Hénon map |

[Apophysis plugin](https://www.deviantart.com/tyrantwave/art/Henon-and-Lozi-Apo-Plugins-125039554)  
[MathWorld description](https://mathworld.wolfram.com/HenonMap.html)  
[Wikipedia description](https://en.wikipedia.org/wiki/H%C3%A9non_map)  

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

[Description at Fraktelwelt](http://www.fraktalwelt.de/myhome/simpiter2.html)  
[Video by Paul Nathan](https://www.youtube.com/watch?v=JhHugpABjDo)  

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

[Description and examples by Paul Bourke](http://paulbourke.net/fractals/lorenz/)  
[Wikipedia description](https://en.wikipedia.org/wiki/Lorenz_system)  
[Euler method on Wikipedia](https://en.wikipedia.org/wiki/Euler_method)  

## lozi
Strange attractor discovered by René Lozi.

Type: 2D  
Author: Chris Johns (TyrantWave)  
Date: 6 Jun 2009

[![](lozi-1.png)](lozi-1.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor; set c to 1 for the classic Lozi map |

[Apophysis plugin](https://www.deviantart.com/tyrantwave/art/Henon-and-Lozi-Apo-Plugins-125039554)  
[Description on the Piecewise Affine Dynamics wiki](http://padyn.wikidot.com/lozi-maps)  
[MathWorld description](https://mathworld.wolfram.com/LoziMap.html)  

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

[Description by Jürgen Meier](http://www.3d-meier.de/tut19/Seite158.html) (German)  

## pdj
Peter de Jong attractor

Type: 2D
Author: Scott Draves  
Date: Sept 2003  

[![](pdj-1.png)](pdj-1.flame)

| Parameter | Description |
| --- | --- |
| a - d | Variables that define the attractor |

[Description and examples by Paul Bourke](http://paulbourke.net/fractals/peterdejong/)  
[Article by Greg Cope](https://www.algosome.com/articles/strange-attractors-de-jong.html)  

## sattractor_js
A strange attractor attributed to Roger Bagula.

Type: 2D  
Author: Jesus Sosa  
Date: 21 Dec 2017

[![](sattractor-1.png)](sattractor-1.flame) [![](sattractor-2.png)](sattractor-2.flame)

| Parameter | Description |
| --- | --- |
| m | Symmetry of the attractor, integer between 2 and 12 |

[Examples by Paul Bourke](http://paulbourke.net/fractals/henonattractor/)  

## svensson_js
Johnny Svensson attractor, based on the Peter de Jong attractor.

Type: 2D  
Author: Jesus Sosa  
Date: 12 Dec 2017  

[![](svensson-1.png)](svensson-1.flame)

| Parameter | Description |
| --- | --- |
| a - d | Variables that define the attractor |

[Description](http://paulbourke.net/fractals/peterdejong/) (scroll to very bottom)  

## threeply
A strange attractor named Three Ply

Type: 2D Blur  
Author: Jesus Sosa  
Date: 7 May 2020  

[![](threeply-1.png)](threeply-1.flame) [![](threeply-2.png)](threeply-2.flame)

| Parameter | Description |
| --- | --- |
| a - c | Variables that define the attractor |

[Description and Java applet by James Henstridge](http://www.jamesh.id.au/fractals/orbit/threeply.html)  
