# Importers
Variations that import a flame, image, etc. from elsewhere.

## obj_mesh_wf
Load a 3D mesh from an OBJ format file.

Type: 3D mesh  
Author: Andreas Maschke (thargor6)   
Date: 29 Nov 2016  

[![](obj_mesh_wf-1.png)](obj_mesh_wf-1.flame)

The OBJ object file format was developed by Wavefront Technologies but is open and supported by many 3D graphics programs. It defines the XYZ position of each vertex and the faces that make each polygon in the mesh as a list of vertices. It can optionally define UV texture map coordinates for each face, used to map a 2D image to the mesh's surface. These are used by the color and displacement map features. If the OBJ file does not include texture map coordinates, the color and displacement maps are ignored.

| Parameter | Description |
| --- | --- |
| obj_filename | The file containing the mesh; set the default path with the preference tinaMeshPath |
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
[Working with Mesh Objects video tutorial](https://www.youtube.com/watch?v=j470dOB4ksM)  

## subflame_wf
Use a flame as a shape.

Type: 3D blur  
Author: Andreas Maschke (thargor6)  
Date: 22 Jan 2012  

[![](subflame_wf-1.png)](subflame_wf-1.flame)

Subflame_wf includes a flame (the subflame) inside another flame (the main flame). Transforms in the main flame can manipulate the subflame, but don't affect the subflame itself.

To set the flame, select the flame parameter and click the gear icon to its right. Then delete the existing flame text and paste in the desired flame. Alternatively, select the flame_filename parameter, click the gear icon to its right, and select the file containing the desired flame.

Subflame_wf supports animation. The easiest way to include animated subflames in an animated flame is to use motion curves when preparing the subflame. An alternate method is to use the JWildfire Easy move maker to save an animated flame as a sequence of flames (select FLAMES as the output type). Then set flame_filename to the first flame in the sequence, set flame_is_sequence to 1, and set the other flame_sequence parameters.

| Parameter | Description |
| --- | --- |
| flame | The flame to import as a subflame (copy the flame to the clipboard, edit the flame parameter by clicking the gear icon, delete the existing flame, and paste the new flame) |
| flame_filename | An alternate to flame, the name of the file containing the subflame (or first flame in a sequence of flames) |
| scale | Adjust the size of the subflame |
| angle | Adjust the rotation angle of the subflame in degrees |
| offset_x, offset_y, offset_z | Adjust the position of the subflame |
| colorscale_z | Multiply the flame's gradient index by this and add to z (like colorscale_wf) |
| color_mode | How to treat subflame colors:<br>-2: True color - Use the original subflame colors<br>-1: Ignore subflame colors (use the coloring type of the transform containing subflame_wf)<br>0: Direct color; use the gradient index of the subflame, but the gradient of the main flame<br>1: Red - set the gradient index to the amount of red in the subflame<br>2: Green - set the gradient index to the amount of green in the subflame<br>3: Blue - set the gradient index to the amount of blue in the subflame<br>4: Brightness - set the gradient index to the brightness of the subflame
| flame_is_sequence | 0 for a single flame, 1 for a sequence of flames (flame_filename must be set to the first file in the sequence) |
| flame_sequence_start | Starting sequence number |
| flame_sequence_end | Ending sequence number (0 for none) |
| flame_sequence_repeat | Sequence number to start repeating at after flame_sequence_end is reached |
| flame_sequence_digits | Number of digits in the sequence numbers (for example, 4 means sequence numbers are 0001, 0002, etc.) |

[Subflame tutorial](http://www.andreas-maschke.de/java/jwildfire_tutorial05.pdf)  
[Description on Fractal Formulas](https://fractalformulas.wordpress.com/flame-variations/subflame/)  
[Subflame tutorial on JWildfire Sanctuary](https://fractalformulas.wordpress.com/flame-variations/subflame/)  
[JWildfire subflame cylinder technique video](https://www.youtube.com/watch?v=PmVlSLAmi30)  
