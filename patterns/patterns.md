# Patterns
Variations that create different kinds of patterns.

## checkerboard_wf
Generate a checkerboard pattern

Type: 3D direct color blur  
Author: Andreas Maschke (thargor6)  
Date: 7 Oct 2016  

[![](checkerboard_wf-1.png)](checkerboard_wf-1.flame)

| Parameter | Description |
| --- | --- |
| position | Position of the checkerboard along its perpendicular axis |
| size | Width and height of the (square) checkerboard (assuming variation amount is 1) |
| axis | 0: Checkerboard on XY plane<br>1: Checkerboard on YZ plane<br>2: Checkerboard on ZX plane |
| checker_size | Size of each square (as a fraction of size) |
| displ_amount | Thickness of the checkerboard |
| checker_color1, checker_color2 | Gradient index of the squares (between 0 and 1) |
| side_color | Gradient index of the square borders (if present) |
| with_sides | 0: No borders on the squares<br>1: Add borders to the squares (displ_amount must be non-zero) |

## dc_perlin
Generate a pattern based on fractal Brownian motion (fBm), also known as Perlin noise.

Type: 2D direct color blur  
Author: Neil Slater (slobo777)  
Date: 14 Nov 2010  

[![](dc_perlin-1.png)](dc_perlin-1.flame)

| Parameter | Description |
| --- | --- |
| shape | The shape to use:<br>0: Square<br>1: Disk (filled-in circle)<br>2: Blur disk (brighter in center, like the blur variation) |
| map | Mapping from the noise function to the shape:<br>0: Flat<br>1: Spherical (like the spherical variation, creates small features in the center)<br>2: Half-spherical (like spherical, but with less distortion)<br>3: Quarter-spherical (between 1 and 2)<br>4: Bubble (like the bubble variation; the result is still 2D, but has a 3D appearance)<br>5: Exaggerated bubble (like bubble but the effect is stronger) |
| select_centre, select_range | Noise values outside the range of select_centre±select_range create holes (transparent areas) in the pattern; increase select_range to eliminate unwanted holes |
| centre | The center gradient index value to use, between 0 and 1; works with range to determine the gradient color to use |
| range | The range of gradient values on each side of centre to use; 0.5 to use the entire gradient; larger values will use the gradient multiple times |
| edge | 0 for normal; positive values increase the size and create a ragged edge |
| scale | Scale factor for the noise function; increase for higher frequency noise (smaller features that are closer together) |
| octaves | Number of octaves to use for fBm, between 1 and 5 |
| amps | Value to divide the amplitude of each octave by; use 2 for normal fBm noise, but change for different effects (normally greater than 1, but this is not enforced) |
| freqs | Value to multiply the frequency of each octave by; use 2 for normal fBm noise, but change for different effects (normally greater than 1, but this is not enforced) |
| z | The z value for computing the noise; changing it changes the specific pattern but not the general appearance of the noise |
| select_bailout | Limits the number of retries when the random point hits a hole controlled by the select_centre, select_range, and edge parameters; the default of 10 is usually fine, but it can be increased if faint patterns show in the holes (this will slow down the variation) |

[Apophysis 7X variation](https://www.deviantart.com/slobo777/art/dc-perlin-Apophysis-Plugin-186190256)  
[Dc_perlin description at Fractal Formulas](https://fractalformulas.wordpress.com/flame-variations/dc_perlin/)  
[Coherent Noise explanation](https://fractalformulas.wordpress.com/2019/08/19/coherent-noise/)  
[Wikipedia description of Perlin noise](https://en.wikipedia.org/wiki/Perlin_noise)  
[Roz Scripts (for Apophysis)](https://www.deviantart.com/rozrr/art/Roz-Scripts-321285804)  

## dla3d_wf
Create a 3D Diffusion Limited Aggregation (DLA) mesh.

Type: 3D direct color blur  
Author: Andreas Maschke (thargor6)  
Date: 12 March 2017  

[![](dla3d_wf-1.png)](dla3d_wf-1.flame) [![](dla3d_wf-2.png)](dla3d_wf-2.flame)

| Parameter | Description |
| --- | --- |
| node_obj_filename | Name of file containing the mesh object used for nodes; default is a sphere |
| node_colormap_filename | Name of file containing the colormap used for nodes |
| junct_obj_filename | Name of file containing the mesh object used for junctions; default is a cylinder |
| junct_colormap_filename | Name of file containing the colormap used for junctions |
| max_iter | Maximum number of iterations to use; larger values create a larger, more intricate pattern. To animate DLA growth, set single_thread to 1, then start with a small value for max_iter, and increasing it as the animation progresses |
| seed | Random number seed |
| inner_blur_radius | Radius for elements closest to center; normally larger than outer_blur_radius, but this is not required |
| outer_blur_radius | Radius for elements furthest from center; very small values will make them pointed |
| junction_scale | Scale factor for nodes |
| dc_color | 0: Standard variation coloring; don't modify the gradient color index directly<br>1: Direct color; set the gradient color index according to the distance from the center |
| glue_radius | Radius for adding new nodes; small values tend to clump the nodes together; larger values spread them apart |
| force_x, force_y, force_z | Values added to x, y, and z, respectively, when adding new nodes |
| display_nodes | 1 to display nodes; 0 to hide them |
| display_junctions | 1 to display junctions; 0 to hide them |
| single_thread | 0: Use multiple threads for DLA generation; this is faster, but less predictable<br>1: Use a single thread for DLA generation |
| node_sdiv_level | Number of levels of subdivision smoothing to perform on node meshes; 0 to disable |
| node_sdiv_smooth_passes | Number of smoothing passes to perform for each subdivision level for nodes |
| node_sdiv_smooth_lambda | Smoothing parameter for first step for each node smoothing pass (should be positive) |
| node_sdiv_smooth_mu | Smoothing parameter for second step for each node smoothing pass (should be negative) |
| blend_colormap | Whether to blend node colormap colors with surrounding colors<br>0: Don't blend colors<br>1: Blend colors |
| node_mesh_scale | Scale factor for node meshes |
| junct_sdiv_level | Number of levels of subdivision smoothing to perform on junction meshes; 0 to disable |
| junct_sdiv_smooth_passes | Number of smoothing passes to perform for each subdivision level for junctions |
| junct_sdiv_smooth_lambda | Smoothing parameter for first step for each junction smoothing pass (should be positive) |
| junct_sdiv_smooth_mu | Smoothing parameter for second step for each junction smoothing pass (should be negative) |
| blend_colormap | Whether to blend junction colormap colors with surrounding colors<br>0: Don't blend colors<br>1: Blend colors |
| junct_mesh_scale | Scale factor for junction meshes |

[Wikipedia article on DLA](https://en.wikipedia.org/wiki/Diffusion-limited_aggregation)
[Paul Bourke article on DLA](http://paulbourke.net/fractals/dla/)  

## dla_wf
Create a simple Diffusion Limited Aggregation (DLA) pattern.

Type: 2D blur  
Author: Andreas Maschke (thargor6)  
Date: 26 May 2014  

[![](dla_wf-1.png)](dla_wf-1.flame)

| Parameter | Description |
| --- | --- |
| buffer_size | Number of points per side of the square buffer used to store the generated points |
| max_iter | Maximum number of iterations to use; larger values create a larger, more intricate pattern. Animate DLA growth by starting with a small value, and increasing max_iter as the animation progresses. |
| seed | Random number generator seed; different seeds create different patterns |
| scale | Scale factor |
| jitter | Controls the random offset of the dots creating the pattern; 0 makes the dots line up perfectly, which can be distracting |

[Wikipedia article on DLA](https://en.wikipedia.org/wiki/Diffusion-limited_aggregation)
[Paul Bourke article on DLA](http://paulbourke.net/fractals/dla/)  

## mandala
Generate a fractal kaleidoscope pattern based on rotation transformations and rounding errors.

Type: 2D blur, true color or direct color  
Authors: Jesus Sosa and Steve Witham  
Date: 14 Sep 2018  

[![](mandala-1.png)](mandala-1.flame)

| Parameter | Description |
| --- | --- |
| width | Number of points to use for both the width and height of the pattern; large values give a higher resolution pattern, but slow down the variation |
| size | Size of each point, between 0 and 1 |
| num | Numerator of the rotation angle as a fraction of 360 degrees |
| denom | Denominator of the rotation angle as a fraction of 360 degrees |
| minsky | 0: Circular mandala<br>1: Elliptical mandala |
| wobble | Varies the mandala calculation by a small amount, which disturbs the pattern (some fractions are more sensitive to wobble than others); an integer between 0 and 8, 0 for none |
| wrap_range | If not 0, includes a wrapping effect in the mandala calculation; an integer between 0 and 8, 0 for none |
| hskew | If not 0, the point is shifted to the right by some amount after each rotation step, often resulting in interesting effects; an integer between 0 and 22 |
| color id | 0: True color: colors are set directly, ignoring the gradient<br>1: Direct color: sets the gradient index so gradient colors are used |

[Mandala description](http://www.mac-guyver.com/switham/2005/03/Mandala/index.html) (by Steve Witham, author of the mandala program the variation is based on)

## snowflake_wf
Generate a snowflake shape using a cellular automaton.

Type: 2D direct color blur  
Author: Andreas Maschke (thargor6)  
Date: 10 Jan 2021  

[![](snowflake_wf-1.png)](snowflake_wf-1.flame) [![](snowflake_wf-2.png)](snowflake_wf-2.flame)

To animate snowflake growth, start with a low value for max_iter at the beginning of the animation and increase it as the animation progresses. [Samples (pdf)](snowflake-samples.pdf)

| Parameter | Description |
| --- | --- |
| buffer_size | Controls the number of cells (dots) in the generated snowflake |
| max_iter | Number of times to iterate snowflake generation; larger values make larger, more intricate patterns, but take longer and require a larger buffer_size value |
| bg_freeze_level | The base starting value for the cells |
| fg_freeze_speed | How fast cells next to frozen cells (with value at least 1) freeze |
| diffusion_speed | How fast cells not next to frozen cells freeze |
| diffusion_asymmetry | Controls the weighting for averaging cell values |
| rnd_bg_noise | Amount of noise added to base starting value for the cells; 0 for completely symmetrical snowflakes |
| threshold | Threshold value to display cells in final snowflake; if background dots appear, increase threshold to remove them |
| seed | The random number seed; different seeds will generate similar but different results |
| scale | Scale factor for the result |
| jitter | Controls the random offset of the dots creating the snowflake; 0 makes the dots line up perfectly, which can be distracting |
| dc_color | 0: Standard variation coloring; don't modify the gradient color index directly<br>1: Direct color; set the gradient color index according to the point intensity |
| dc_color_scale | Scale factor for the point intensity (most points will have intensity between the threshold parameter and 1) |
| dc_color_offset | Lowest color index to use (0 for leftmost gradient color) |

[A local cellular model for snow crystal growth](http://patarnott.com/pdf/SnowCrystalGrowth.pdf) (description of the algorithm)  
[Interactive online version](https://snowflake.overwhale.com/)  

## sunflower
Generate a spiral of small polygons that can resemble the center of a sunflower.

Type: 2D direct color blur  
Author: Jesus Sosa  
Date: 8 Jul 2018  

[![](sunflower-1.png)](sunflower-1.flame) [![](sunflower-2.png)](sunflower-2.flame) [![](sunflower-3.png)](sunflower-3.flame)

| Parameter | Description |
| --- | --- |
| nPoints | Number of polygons to generate |
| shape | Number of sides of each polygon (3 to 20) |
| scale | Size of largest polygons |
| angle | Controls the angle of the spiral; adjusted so 180 gives the "golden angle", the angle between successive florets in sunflowers |
| color | Not used |
| F.filling | Amount to fill the shapes, from 0 (filled) to 1 (hollow) |
| invert | 0: Center of spiral has largest polygons with color index 1<br>1: Center of spiral has smallest polygons with color index 0 |

[The Golden Ratio](https://www.youtube.com/watch?v=sj8Sg8qnjOg) (Numberphile video that shows how the sunflower variation works)
[Nature, The Golden Ratio, and Fibonacci too](https://www.mathsisfun.com/numbers/nature-golden-ratio-fibonacci.html)

## szubieta
Fractal patterns by Santiago Zubieta: circle squares and square tile.

Type: 2D direct color blur  
Author: Jesus Sosa  
Date: 16 Aug 2018  

[![](szubieta-1.png)](szubieta-1.flame) [![](szubieta-2.png)](szubieta-2.flame)

| Parameter | Description |
| --- | --- |
| width | Number of circles horizontally |
| height | Number of circles vertically |
| type | 0: Circle squares pattern (first example)<br>1: Square tile pattern (second example) |
| scale | Size of the circles |

[Circle squares fractal](http://paulbourke.net/fractals/circlesquares/)  
[Square tile fractal](http://paulbourke.net/fractals/squaretile/)  

## terrain3D
Generate a random terrain surface mesh.

Type: 3D mesh  
Author: Jesus Sosa  
Date: 14 Apr 2018  

[![](terrain3D-1.png)](terrain3D-1.flame)

| Parameter | Description |
| --- | --- |
| roughness | Surface roughness; 0.5 is average, smaller is smoother |
| z_exaggeration | Altitude scale; larger values exaggerate the altitude |
| Size (N PowersOf 2) | The number of cells per side used to generate the terrain, as a power of 2; for example a value of 5 would use 2^5=32 cells per side (for a total of 1024) |
| seed | The random number seed; changing this number will change the terrain generated |
| dc | 0: Use the transform color<br>1: Use direct color; the color of a point is based on its altitude |
| scale_x, scale_y, scale_z | Scale factors for x, y, and z |
| offset_x, offset_y, offset_z | Shift the mesh in the x, y, and z directions |
| subdiv_level | The number of levels of subdivision to perform; it must be an integer between 0 (to disable smoothing) and 6. Note each level used will dramatically increase both render time and memory needed. |
| subdiv_smooth_passes | The number of Taubin smoothing passes to apply to each subdivision level; it must be an integer between 0 and 24. |
| subdiv_smooth_lambda | The lambda value used for the first step of each pass; it should be a positive number between 0 and 1. |
| subdiv_smooth_mu | The mu value used for the second step of tach pass; it should be a negative number between 0 and -1, and is usually a bit less than -lambda). |
| blend_colormap | Not used |
| displ_amount | Not used |
| blend_displ_map | Not used |
| receive_only_shadows | If set to 1, and solid rendering is enabled, the mesh will be invisible but will show shadows that fall on it (hard shadows must be enabled to see any) |

[JWildfire forum post](https://jwildfire-forum.overwhale.com/viewtopic.php?f=23&t=2626)  

## wangtiles
Generate a (possibly repeating) pattern from a 12x8 set of Wang tiles.

Type: 3D blur  
Author: Jesus Sosa  
Tile artist: Guy Walker  
Date: 29 Apr 2018  

[![](wangtiles-1.png)](wangtiles-1.flame) [![](wangtiles-2.png)](wangtiles-2.flame)

The core Wang tiling is always 12 wide and 8 high, so the tiles are elongated vertically. This is why the vertical pipes in the first example are thinner than the horizontal pipes. To use square tiles, set scale_x to 1.5 (and optionally square to 0 and offset_x to -0.25).

The wangtiles variation will also set z based on the color of the point, like [colorscale_wf](zmanip/zmanip.md#colorscale_wf). This is not a bump map for the tile, so it won't make the result an accurate 3D tiling.

| Parameter | Description |
| --- | --- |
| id | The id of the Wang tile set to use, from 0 to 104 ([pdf index](wangtiles-ids.pdf)) |
| seed | The random seed; changes the pattern of the tiles |
| square | 0: Make the overall wangtiles shape a rectangle<br>1: Make the overall wangtiles shape a square |
| scale_x, scale_y | Horizontal and vertical scale factors for the Wang tiles |
| scale_z | Scale factor for z colorscale setting; 0 to disable |
| offset_x, offset_y | Horizontal and vertical offsets for the Wang tiles |
| offset_z | Offset added to the z value of each point |
| tile_x | 0: Don't tile horizontally (space outside the 12x8 Wang tile set will be black)<br>1: Tile the Wang tile set horizontally |
| tile_y | 0: Don't tile vertically (space outside the 12x8 Wang tile set will be black)<br>1: Tile the Wang tile set vertically |
| reset_z | 0: Add the color index to existing z value<br>1: Override existing z value with the color index |

[Wang tile on Wikipedia](https://en.wikipedia.org/wiki/Wang_tile)  
[Source for tiles used in this variation (under Gallery)](http://www.cr31.co.uk/stagecast/wang/intro.html)  
