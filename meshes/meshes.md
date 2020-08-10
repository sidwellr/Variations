# Meshes
Variations that generate meshes, three dimensional shapes made from connected triangles. These are all blur variations that ignore their inputs. They are most useful for solid renders, though they work for normal flames as well.

The mesh variations can perform subdivision surface smoothing. This can be helpful for some meshes to create a smoother surface. But it deforms meshes that aren't designed to be smoothed. For example, smoothing an icosahedron will make it a sphere. This is done by first subdividing each triangle into four triangles, then performing Taubin smoothing on each triangle. This process is repeated the number of times specified by subdiv_level (set it to 0 to disable smoothing).

For each subdivision level, each triangle in the mesh is subdivided into four triangles and Taubin smoothing is done on each resulting triangle. Taubin smoothing is done with multiple passes, with two smoothing steps done on each pass. The first step uses the lambda parameter to smooth the mesh, but this also shrinks it. The second step uses the mu parameter (which should be a negative value) to counteract the shrinking.

## obj_mesh_primitive_wf
Use a predefined object as a 3D mesh.

Type: 3D mesh  
Author: Andreas Maschke (thargor6)   
Date: 29 Nov 2016  

[![](obj_mesh_primitive_wf-1.png)](obj_mesh_primitive_wf-1.flame)

| Parameter | Description |
| --- | --- |
| colormap_filename | The file containing a color map to apply to the mesh |
| displ_map_filename | The file containing the displacement map |
| primitive | The object to use:<br>0: Ball<br>1: Capsule<br>2: Cone<br>3: Diamond<br>4: Torus<br>5: Box<br>6: Gear (15 teeth)<br>7: Icosahedron<br>8: Tetrahedron<br>9: Octahedron<br>10: Dodecahedron<br>11: Cylinder with a hole<br>12: Icosidodecahedron<br>13: Cubeoctahedron<br>14: Gear (6 teeth)<br>15: Smooth gear (6 teeth)<br>16: Gear (8 teeth)<br>17: Smooth gear (8 teeth)<br>18: Gear (12 teeth)<br>19: Smooth gear (12 teeth)<br>20: Gear (16 teeth)<br>21: Smooth gear (16 teeth)<br>22: Gear (24 teeth)<br>23: Smooth gear (24 teeth)<br>24: Mandelbulb<br>25: Drop
| scale_x, scale_y, scale_z | Scale factors for x, y, and z |
| offset_x, offset_y, offset_z | Shift the mesh in the x, y, and z directions |
| subdiv_level | The number of levels of subdivision to perform; it must be an integer between 0 (to disable smoothing) and 6. Note each level used will dramatically increase both render time and memory needed. |
| subdiv_smooth_passes | The number of Taubin smoothing passes to apply to each subdivision level; it must be an integer between 0 and 24. |
| subdiv_smooth_lambda | The lambda value used for the first step of each pass; it should be a positive number between 0 and 1. |
| subdiv_smooth_mu | The mu value used for the second step of tach pass; it should be a negative number between 0 and -1, and is usually a bit less than -lambda). |
| blend_colormap | Whether to blend colormap colors with surrounding colors (color_mode 0 only)<br>0: Don't blend colors<br>1: Blend colors |
| displ_amount | Scaling for the displacement map; 0 to disable displacement |
| blend_displ_map | Whether to blend values from the displacement map<br>0: Don't blend values<br>1: Blend values |
| receive_only_shadows | If set to 1, and solid rendering is enabled, the mesh will be invisible but will show shadows that fall on it (hard shadows must be enabled to see any) |

## obj_mesh_wf
Load a 3D mesh from an OBJ format file.

Type: 3D mesh  
Author: Andreas Maschke (thargor6)   
Date: 29 Nov 2016  

[![](obj_mesh_wf-1.png)](obj_mesh_wf-1.flame)

The OBJ object file format was developed by Wavefront Technologies but is open and supported by many 3D graphics programs. It defines the XYZ position of each vertex and the faces that make each polygon in the mesh as a list of vertices. It can optionally define UV texture map coordinates for each face, used to map a 2D image to the mesh's surface. These are used by the color and displacement map features. If the OBJ file does not include texture map coordinates, the color and displacement maps are ignored.

| Parameter | Description |
| --- | --- |
| obj_filename | The file containing the mesh |
| colormap_filename | The file containing a color map to apply to the mesh |
| displ_map_filename | The file containing the displacement map |
| scale_x, scale_y, scale_z | Scale factors for x, y, and z |
| offset_x, offset_y, offset_z | Shift the mesh in the x, y, and z directions |
| subdiv_level | The number of levels of subdivision to perform; it must be an integer between 0 (to disable smoothing) and 6. Note each level used will dramatically increase both render time and memory needed. |
| subdiv_smooth_passes | The number of Taubin smoothing passes to apply to each subdivision level; it must be an integer between 0 and 24. |
| subdiv_smooth_lambda | The lambda value used for the first step of each pass; it should be a positive number between 0 and 1. |
| subdiv_smooth_mu | The mu value used for the second step of tach pass; it should be a negative number between 0 and -1, and is usually a bit less than -lambda). |
| blend_colormap | Whether to blend colormap colors with surrounding colors (color_mode 0 only)<br>0: Don't blend colors<br>1: Blend colors |
| displ_amount | Scaling for the displacement map; 0 to disable displacement |
| blend_displ_map | Whether to blend values from the displacement map<br>0: Don't blend values<br>1: Blend values |
| receive_only_shadows | If set to 1, and solid rendering is enabled, the mesh will be invisible but will show shadows that fall on it (hard shadows must be enabled to see any) |

[Teapot mesh](teapot.obj) used for above example.

## sattractor3D
Generate a 3D mesh from differential equations.

Type: 3D mesh  
Author: Jesus Sosa  
Data: 21 Feb 2018

[![](sattractor3D-1.png)](sattractor3D-1.flame) [![](sattractor3D-2.png)](sattractor3D-2.flame)

| Parameter | Description |
| --- | --- |
| xformula | The formula to use for dx for the attractor differential equation; it returns the value for dx, and can use "x", "y", "z", and "param_a" through "param_h" as well as constants and standard math functions. Changing presetId will overwrite it with the preset formula. |
| yformula | The formula to use for dy for the attractor differential equation |
| zformula | The formula to use for dz for the attractor differential equation |
| presetId | The preset to use; set to -1 to not use a preset<br>0: Aizawa Attractor<br>1: Anishchenko-Astakhov Attractor<br>2: Arneodo Attractor<br>3: Second Bouali Attractor<br>4: Bourke-Shaw Attractor<br>5: Chen Celikovsky Attractor<br>6: Chen Lee Attractor<br>7: Chua Attractor<br>8: Chen Attractor<br>9: Lotka Volterra Equations<br>10: Rikitake Attractor<br>11: Three Scroll Unified Chaotic System Attractor 1 (TSUCS 1)<br>12: Dequan Li Attractor<br>13: Halvorsen Attractor<br>14: Finnance Attractor<br>15: Newton Leipnik System<br>16: Nose-Hoover Attractor<br>17: Sprott-Linz Attractor<br>18: Thomas Attractor<br>19: Three Scroll Unified Chaotic System Attractor 2 (TSUCS 2)<br>20: Dadras Attractor |
| steps | Number of thousands of steps to use in the curve |
| radius | Thickness of the curve |
| stepTime | Delta time for computing the curve |
| facets | Number of sides in the attractor curve |
| start_x, start_y, start_z | Initial values for x, y, and z |
| warmup | Number of steps to skip before plotting the attractor |
| param_a - param_h | Value for param_a through param_h in the formulas |
| scale_x, scale_y, scale_z | Scale factors for x, y, and z |
| offset_x, offset_y, offset_z | Offset for the attractor curve |
| subdiv_level, subdiv_smooth_passes, subdiv_smooth_lambda, subdiv_smooth_mu | Not used |
| blend_colormap | Not used |
| displ_amount | Not used |
| blend_displ_map | Not used |
| receive_only_shadows | If set to 1, and solid rendering is enabled, the mesh will be invisible but will show shadows that fall on it (hard shadows must be enabled to see any) |

https://jwildfire-forum.overwhale.com/viewtopic.php?f=23&t=2607  
https://github.com/thargor6/JWildfire/blob/master/src/org/jwildfire/create/tina/variation/plot/sattractor3d_wf_presets.txt  

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

https://jwildfire-forum.overwhale.com/viewtopic.php?f=23&t=2626  
