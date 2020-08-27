# Flame Fractal Variations

| Variation | Description
| --- | ---
|[auger](waves/waves.md#auger) | Wave effect that gets stronger further from the origin
| |
|[bi_linear](linear/linear.md#bi_linear) | Swap x and y
|[blob](blobs/blobs.md#blob) | Pushes and pulls the plane using a radial sine wave to make it look like a blob
|[blob_fl](blobs/blobs.md#blob_fl) | "Fluid" version of blob; allows fractional values for waves
|[blob2](blobs/blobs.md#blob2) | Modulate a flame using radial sine waves
|[blob3D](blobs/blobs.md#blob3D) | A variant of blob that adds a 3D component
|[blur](shapes/shapes.md#blur) | Circle with a bright center
|[blur_circle](shapes/shapes.md#blur_circle) | Circle with even coloring
|[blur_heart](shapes/shapes.md#blur_heart) | Creates a heart from two ellipses
|[blur_linear](blurry/blurry.md#blur_linear) | Create a motion blur effect
|[blur_pixelize](blurry/blurry.md#blur_pixelize) | Averages colors in an area to make large square pixels
|[blur_zoom](blurry/blurry.md#blur_zoom) | Create a zoom blur effect
|[blur3D](shapes/shapes.md#blur3D--pre_blur3D) | Three dimensional Gaussian blur
|[boarders](boarders/boarders.md#boarders-1) | Divide the plane into squares with borders
|[boarders2](boarders/boarders.md#boarders2--pre_boarders2) | Divide the plane into squares with borders, with parameters
|[butterfly](reshapers/reshapers.md#butterfly) | Reshape squares centered at the origin into butterfly shapes
| |
|[cannabiscurve_wf](halfblurs/halfblurs.md#cannabiscurve_wf) | Shape resembling a cannabis leaf
|[chrysanthemum](shapes/shapes.md#chrysanthemum) | Chrysanthemum flower shaped curve
|[cloverleaf_wf](halfblurs/halfblurs.md#cloverleaf_wf) | Shape resembling a four leaf clover
|[circleblur](shapes/shapes.md#circleblur) | Circle with even coloring
|[circlize](reshapers/reshapers.md#circlize) | Reshape squares centered at the origin into circles
|[circlize2](reshapers/reshapers.md#circlize2) | Reshape squares centered at the origin into circles (scaled to work better with other variations)
|[clifford_js](attractors/attractors.md#clifford_js) | Strange attractor attributed to Cliff Pickover
|[conic/conic2](halfblurs/halfblurs.md#conic--conic2) | Conic section shape (ellipse, parabola, or hyperbola)
|[cpow](cpow/cpow.md#cpow) | Raise input point to a complex power specified by its real and imaginary parts
|[cpow2](cpow/cpow.md#cpow2) | Raise input point to a complex power specified in polar coordinates
|[cpow3](cpow/cpow.md#cpow3) | Raise input point to a complex power to produce a spiral
|[cpow3_wf](cpow/cpow.md#cpow3_wf) | Attempt to port cpow2 to JWildfire that "by happy accident became something else"
| |
|[d_spherical](inversion/inversion.md#d_spherical) | Combines spherical and linear
|[dc_boarders](boarders/boarders.md#dc_boarders) | Presumably, a direct color version of boarders, but it appears to be the same as boarders
|[dc_linear](linear/linear.md#dc_linear) | Direct color version of linear3D
|[droste](cpow/cpow.md#droste) | Implements Escher's map using logarithms; same effect as escher
| |
|[eJulia](julia/julia.md#eJulia) | Polynomial Julia sets in elliptic coordinates
|[epispiral](rosecurve/rosecurve.md#epispiral) | An inside-out rose curve, known as an epispiral curve
|[epispiral_wf](rosecurve/rosecurve.md#epispiral_wf) | Alternate version of epispiral
|[escher](cpow/cpow.md#escher) | Implements Escher’s Map
|[exblur](blurry/blurry.md#exblur) | Blur effect radiating from a point
|[extrude](zmanip/zmanip.md#extrude) | Extrude the other variations on the transform by stretching the z coordinate
| |
|[fan](flippers/flippers.md#fan) | Divides the plane into pie shaped wedges and rotates them (dependent variation)
|[fan2](flippers/flippers.md#fan2) | Divides the plane into pie shaped wedges and rotates them (parameter version)
|[flatten](zmanip/zmanip.md#flatten--zclear) | Flatten the flame by setting the z coordinate to 0
|[flipcircle](flippers/flippers.md#flipcircle) | Flips the points inside a circle centered at the origin top to bottom
|[flipy](flippers/flippers.md#flipy) | Flips the points on the right side of the y-axis top to bottom
|[flower](rosecurve/rosecurve.md#flower) | Filled-in rose curve; looks like a flower with petals
|[flower_db](blobs/blobs.md#flower_db) | Reshape a flame into a 3D flower
|[flower2](rosecurve/rosecurve.md#flower) | Filled-in rose curve; looks like a flower with petals
|[flower3D](rosecurve/rosecurve.md#flower3D) | Experimental 3D version of flower
| |
|[gaussian_blur](shapes/shapes.md#gaussian_blur) | Fuzzy circle with a bright center, made from a Gaussian distribution
|[gingerbread_man](attractors/attractors.md#gingerbread_man) | An attractor that resembles a gingerbread man
|[glitchy1](flippers/flippers.md#glitchy1) | Mix of lazysensen (divide flame into strips and flip them) and pixel_flow (blur to resemble flowing pixels)
|[gumowski_mira](attractors/attractors.md#gumowski_mira) | The strange attractor of Gumowski-Mira
| |
|[henon](attractors/attractors.md#henon) | Strange attractor discovered by Michel Hénon
|[hopalong](attractors/attractors.md#hopalong) | Hopalong attractor, also known as the Martin map
| |
|[inflateZ_1](zmanip/zmanip.md#inflateZ_1) | Set z to tilt the plane forward, basing z mostly on y, but with some distortion
|[inflateZ_2](zmanip/zmanip.md#inflateZ_2) | Set z to tilt the plane diagonally
|[inflateZ_3](zmanip/zmanip.md#inflateZ_3) | Warp z to give a strong three dimensional effect
|[inflateZ_4](zmanip/zmanip.md#inflateZ_4) | Set z to create interleaved helix shapes
|[inflateZ_5](zmanip/zmanip.md#inflateZ_5) | Set z to give a gentle three dimensional wave shape
|[inflateZ_6](zmanip/zmanip.md#inflateZ_6) | Set z to give a rolling shape
|[inversion](inversion/inversion.md#inversion-1) | Generalizes 2D circle inversion; same as spherical with the default parameters
|[invpolar](polar/polar.md#invpolar) | Treat the rectangular coordinates (x,y) of a point as polar coordinates (ρ,θ) (the inverse of polar)
|[isosfplot3d_wf](plotting/plotting.md#isosfplot3d_wf) | Isosurface plot (plots points where the value of a function is near zero)
| |
|[julia](julia/julia.md#julia-1) | Classic quadratic Julia set (deprecated; use julian with power=2)
|[julia3D](julia/julia.md#julia3D) | Classic polynomial Julia set with 3D extrusion
|[julia3D_fl](julia/julia.md#julia3D_fl) | "Fluid" version of julia3D; allows fractional values for power
|[julia3Dq](julia/julia.md#julia3Dq) | Julia set using a rational power with 3D extrusion
|[julia3Dz](julia/julia.md#julia3Dz) | Classic polynomial Julia set with 3D extrusion
|[julia3Dz_fl](julia/julia.md#julia3Dz_fl) | "Fluid" version of julia3Dz; allows fractional values for power
|[juliac](julia/julia.md#juliac) | Julia set using a complex power
|[juliacomplex](julia/julia.md#juliacomplex) | Julia set using a complex power
|[julian](julia/julia.md#julian) | Classic polynomial Julia set
|[julian_fl](julia/julia.md#julian_fl) | "Fluid" version of julian; allows fractional values for power
|[julian2](julia/julia.md#julian2) | Julian with an integrated affine transform
|[julian2dc](julia/julia.md#julian2dc) | Julian2 with direct color
|[julian3Dx](julia/julia.md#julian3Dx) | Julian2 with 3D wave effect
|[juliaNab](julia/julia.md#juliaNab) | Variant of julian with different parameters
|[juliaq](julia/julia.md#juliaq) | Julia set using a rational power
| |
|[lazysensen](flippers/flippers.md#lazysensen) | Divide the flame into strips and flip them
|[linear](linear/linear.md#linear-1) | Copy the input (x and y only)
|[linear3D](linear/linear.md#linear3D) | Copy the input (x, y, and z)
|[linearT](linear/linear.md#linearT) | Tweak of linear, adding an exponent for x and y
|[linearT3D](linear/linear.md#linearT3D) | Tweak of linear3D, adding an exponent for x, y, and z
|[lorenz_js](attractors/attractors.md#lorenz_js) | Strange attractor first studied by Edward Lorenz
|[lozi](attractors/attractors.md#lozi) | Strange attractor discovered by René Lozi
| |
|[macmillan](attractors/attractors.md#macmillan) | Perturbed McMillan map (studied by Edwin McMillan)
|[maurer_lines](maurerlines/maurerlines.md#maurer_lines) | Generalized string art
|[maurer_rose](rosecurve/rosecurve.md#maurer_rose) | String art on a rose curve
|[minkowscope](flippers/flippers.md#minkowscope) | Flip the plane in a wave shape based on the Minkowsky question-mark function across the origin
| |
|[nBlur](shapes/shapes.md#nBlur) | Polygon shaped blur
|[ngon](reshapers/reshapers.md#ngon) | Reshape circles centered at the origin into polygons, with an option for inversion
|[noise](blurry/blurry.md#noise) | Add noise as a blur effect
|[npolar](julia/julia.md#npolar) | Mashup of julian and polar2
| |
|[obj_mesh_primitive_wf](meshes/meshes.md#obj_mesh_primitive_wf) | Use a predefined object as a 3D mesh
|[obj_mesh_wf](meshes/meshes.md#obj_mesh_wf) | Load a 3D mesh from an OBJ format file
|[oscilloscope](flippers/flippers.md#oscilloscope) | Flip the plane in a sine wave shape across the x axis
|[oscilloscope2](flippers/flippers.md#oscilloscope2) | Flip the plane in a sine wave shape across the origin with perturbation
|[ovoid](inversion/inversion.md#ovoid) | Spherical with x and y scaling
|[ovoid3D](inversion/inversion.md#ovoid3D) | Spherical with x, y, and z scaling
| |
|[parplot2d_wf](plotting/plotting.md#parplot2d_wf) | Parametric equation surface plot (2D surface plotted in three dimensions)
|[pdj](attractors/attractors.md#pdj) | Peter de Jong attractor
|[phoenix_julia](julia/julia.md#phoenix_julia) | Julian with extra distortion parameters
|[pie](shapes/shapes.md#pie) | A circle with wedges missing, like pieces of pie
|[pie_fl](shapes/shapes.md#pie_fl) | Fluid version of pie, allows fractional value for slices
|[pie3D](shapes/shapes.md#pie3D) | Three dimensional version of pie
|[pixel_flow](blurry/blurry.md#pixel_flow) | Blur effect resembling flowing pixels
|[polar](polar/polar.md#polar-1) | Treat the polar coordinates (ρ,θ) of a point as rectangular coordinates (x,y)
|[polar2](polar/polar.md#polar2) | Treat the log-polar coordinates (ρ,θ) of a point as rectangular coordinates (x,y)
|[polar2_3D](polar/polar.md#polar2_3D) | Variant of polar2 with added 3D wave
|[polarplot2d_wf](plotting/plotting.md#polarplot2d_wf) | Plot, in polar coordinates, rho in terms of theta, with 3D extrusion
|[polarplot3d_wf](plotting/plotting.md#polarplot3d_wf) | Plot rho in terms of theta and phi (spherical coordinates) or theta and (cylindrical coordinates)
|[post_bumpmap_wf](zmanip/zmanip.md#post_bumpmap_wf) | Set z from an external bumpmap image
|[post_julia3Dq](julia/julia.md#julia3Dq) | Julia set using a rational power with 3D extrusion
|[post_julian2](julia/julia.md#julian2) | Julian with an integrated affine transform
|[post_juliaq](julia/julia.md#juliaq) | Julia set using a rational power
|[post_polar2](polar/polar.md#polar2) | Treat the log-polar coordinates (ρ,θ) of a point as rectangular coordinates (x,y)
|[post_spherical](inversion/inversion.md#spherical) | Reflects the plane across the unit circle
|[post_zscale](zmanip/zmanip.md#zscale) | Multiply the z value by the variation amount
|[post_ztranslate](zmanip/zmanip.md#ztranslate) | Add the variation amount to z, translating points up or down the z axis
|[pre_blur](shapes/shapes.md#pre_blur) | Pre version of gaussian_blur
|[pre_blur3D](shapes/shapes.md#blur3D--pre_blur3D) | Three dimensional Gaussian blur
|[pre_boarders2](boarders/boarders.md#boarders2--pre_boarders2) | Adds some parameters to boarders
|[pre_polar2](polar/polar.md#polar2) | Treat the log-polar coordinates (ρ,θ) of a point as rectangular coordinates (x,y)
|[pre_polar2_y](polar/polar.md#pre_polar2_y) | Flawed attempt at a pre version of polar2
|[pre_spherical](inversion/inversion.md#spherical) | Reflects the plane across the unit circle
|[pre_zscale](zmanip/zmanip.md#zscale) | Multiply the z value by the variation amount
|[pre_ztranslate](zmanip/zmanip.md#ztranslate) | Add the variation amount to z, translating points up or down the z axis
|[prepost_circlize](reshapers/reshapers.md#prepost_circlize) | Circlize before and uncirclize after other variations, or vice versa
|[primitives_wf](shapes/shapes.md#primitives_wf) | Blur with selectable two or three dimensional shape
|[pRose3D](rosecurve/rosecurve.md#pRose3D) | Rose curve with three dimensional shaping
| |
|[radial_blur](blurry/blurry.md#radial_blur) | Blur effect rotating around the origin
|[rectangles](flippers/flippers.md#rectangles) | Divide the plane into rectangles and flip each horizontally and vertically
|[rhodonea](rosecurve/rosecurve.md#rhodonea) | Advanced rose curve
|[rose](blobs/blobs.md#rose) | Modulate a flame using the rose curve
|[rose_wf](rosecurve/rosecurve.md#rose_wf) | Simple rose curve
| |
|[sattractor3D](meshes/meshes.md#sattractor3D) | Generate a 3D mesh from differential equations
|[sattractor_js](attractors/attractors.md#sattractor_js) | A strange attractor attributed to Roger Bagula
|[scrambly](flippers/flippers.md#scrambly) | Divide the central square into subsquares and scramble them
|[shape](halfblurs/halfblurs.md#shape) | General shape generator using the superformula
|[sineblur](shapes/shapes.md#sineblur) | A circle with a shading effect
|[sphereblur](shapes/shapes.md#sphereblur) | 3D version of sineblur
|[spherical](inversion/inversion.md#spherical) | Reflects the plane across the unit circle
|[spherical3D](inversion/inversion.md#spherical3D) | A 3D version of spherical
|[spherical3D_wf](inversion/inversion.md#spherical3D_wf) | A 3D version of spherical
|[split](flippers/flippers.md#split) | Split the plane into horizontal and vertical strips and flip alternate strips across the x and y axes
|[square](shapes/shapes.md#square) | Square shaped blur
|[square3D](shapes/shapes.md#square3D) | Cube shaped blur
|[squarize](reshapers/reshapers.md#squarize) | Reshape circles centered at the orgin into squares
|[starblur](shapes/shapes.md#starblur) | Star shaped blur
|[super_shape](reshapers/reshapers.md#super_shape) | Reshape (or create a shape) using the superformula
|[superShape3d](shapes/shapes.md#superShape3d) | General 3D shape generator using two superformula instances
|[svensson_js](attractors/attractors.md#svensson_js) | Johnny Svensson attractor
|[synth](synth/synth.md#synth-v2) | Combo variation (emulates several others) with added wave functions
| |
|[terrain3D](meshes/meshes.md#terrain3D) | Generate a random terrain surface mesh
|[threeply](attractors/attractors.md#threeply) | A strange attractor named Three Ply
|[tri_boarders2](boarders/boarders.md#tri_boarders2) | Divide the plane into hexagons with borders
|[triangle](shapes/shapes.md#triangle) | Triangular blur (3D)
| |
|[unpolar](polar/polar.md#unpolar) | Treat the rectangular coordinates (x,y) of a point as log-polar coordinates (ρ,θ) (the opposite of polar2)
| |
|[vibration](waves/waves.md#vibration) | Add sine waves in two arbitrary directions
|[vibration2](waves/waves.md#vibration2) | Add sine waves in two arbitrary directions with modulation
| |
|[waveblur_wf](shapes/shapes.md#waveblur_wf) | Creates waves, like ripples in a pond
|[waves](waves/waves.md#waves-1) | Add sine waves to x and y (dependent variation)
|[waves2](waves/waves.md#waves2) | Add sine waves to x and y
|[waves2_3D](waves/waves.md#waves2_3D) | Add sine waves to x and y with 3D addition
|[waves2_radial](waves/waves.md#waves2_radial) | Add sine waves to x and y outside a circle centered at the origin
|[waves2_wf](waves/waves.md#wavesD2--waves2_wf) | Add damped sine or cosine waves to x and y
|[waves22](waves/waves.md#waves22) | Add sine waves to x and y with power option
|[waves23](waves/waves.md#waves23) | Add triangular "waves" to x and y
|[waves2b](waves/waves.md#waves2b) | Add sine waves to x and y with scaling based on distance from center
|[waves3](waves/waves.md#waves3) | Add modulated sine waves to x and y
|[waves3_wf](waves/waves.md#wavesD3--waves3_wf) | Add damped squared sine or cosine waves to x and y
|[waves4](waves/waves.md#waves4) | Add sine waves to x and y with fracturing of horizontal wave
|[waves4_wf](waves/waves.md#wavesD4--waves4_wf) | Add damped cubed sine or cosine waves to x and y
|[waves42](waves/waves.md#waves42) | Add sine waves to x and y with fracturing of horizontal wave
|[wavesD2](waves/waves.md#wavesD2--waves2_wf) | Add damped sine or cosine waves to x and y
|[wavesD3](waves/waves.md#wavesD3--waves3_wf) | Add damped squared sine or cosine waves to x and y
|[wavesD4](waves/waves.md#wavesD4--waves4_wf) | Add damped cubed sine or cosine waves to x and y
|[wavesn](waves/waves.md#wavesn) | Add damped waves to polynomial Julia set (aka julian)
| |
|[xheart](reshapers/reshapers.md#xheart) | Reshape circles centered at the origin into hearts
|[xheart_blur_wf](shapes/shapes.md#xheart_blur_wf) | Heart shaped blur
|[xtrb](boarders/boarders.md#xtrb) | Divide the plane into hexagons with borders; tri_boarders2 with extra parameters
| |
|[yplot2d_wf](plotting/plotting.md#yplot2d_wf) | Plot y in terms of x, with 3D extrusion
|[yplot3d_wf](plotting/plotting.md#yplot3d_wf) | Plot y in terms of x and z
| |
|[zblur](shapes/shapes.md#zblur) | Gaussian blur for the z axis only (no effect on x or y)
|[zclear](zmanip/zmanip.md#flatten--zclear) | Flatten the flame by setting the z coordinate to 0
|[zcone](zmanip/zmanip.md#zcone) | Add the x-y distance of each point to z, thus transforming the plane into a cone
|[zscale](zmanip/zmanip.md#zscale) | Multiply the z value by the variation amount
|[ztranslate](zmanip/zmanip.md#ztranslate) | Add the variation amount to z, translating points up or down the z axis
|[Z_conic](halfblurs/halfblurs.md#conic--conic2) | Conic section shape (ellipse, parabola, or hyperbola)
|[Z_flower](rosecurve/rosecurve.md#flower) | Filled-in rose curve; looks like a flower with petals
