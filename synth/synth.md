# Synth
Variations that emulate a number of other variations, adding wavy effects using a technique from audio synthesizers.

## synth v1
The first version of synth is still available, but superceded by synth V2. It doesn't have as many options, but otherwise works the same as the later version, so see its description below for details.

Type: 2D; blur with mode 2  
Author: Neil Slater  
Date: 24 Sep 2008  

[Apophysis plugin](https://www.deviantart.com/slobo777/art/Apo-plugin-Synth-98877432)

## synth v2
Combo variation (emulates several others) with added wave functions.

Type: 2D; blur with modes 2, 3, 4, 12, and 13  
Author: Neil Slater  
Date: 7 Jul 2009  

Synth is complicated because it has so many parameters. Understanding the basic structure of the variation is helpful. Synth is divided into a main module and five waveform modules, named 'b' through 'f'. The main module takes the input point and transforms it like a typical variation; the mode parameter determines how it works. The waveform modules each generate a waveform based on the input point and the mode and apply it to the output of the previous module (module b uses parameter a as the input); mode determines the direction (radial, horizontal, etc.). The outputs of the main module and the final waveform module are then combined to produce the final output.

### Main module
The main module applies a variation to the input point; some match other variations, some are unique to synth. Parameter mode specifies the variation to use; the others modify it.

| Parameter | Description |
| --- | --- |
| a | The baseline for the waveform (normally 1) |
| mode | Selects the variation to use, the wave direction, and how the waveform is applied (see next table) |
| power | For modes that use the distance of the point from the origin (the "radius"), power controls how this is done (it isn't the power itself, but used to calculate it). For other modes, it is a parameter for the variation. For the rest, it is ignored.
| mix | How much of the final waveform to mix in; 1 is normal, 0 ignores the waveforms, values between 0 and 1 interpolate, values outside that range extrapolate |
| smooth | For some modes, 0 uses normal linear mapping and 1 uses quadratic Bezier mapping that makes it less aggressive near the origin or away from the unit circle, smoothing the effect. For some modes, 0 selects multiply and 1 selects mixing to apply the waveform. For some modes, smooth is ignored (linear mapping is always used).

The following table describes the modes.

| Example | Mode, Direction, Application, and Description |
| --- | --- |
| [![](synth-0.png)](synth-0.flame) | 0: spherical, radial, multiply<br>Reflects the plane across the unit circle, like the spherical variation.<br>Power adjusts the radius calculation; -2 to match the spherical variation, 0 to act like linear.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-1.png)](synth-1.flame) | 1: bubble, radial, multiply<br>Maps the plane to a sphere, like the bubble variation but not 3D even in 3D flame programs.<br>Power is not used.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-2.png)](synth-2.flame) | 2: blur (v1), radial, multiply<br>A circle or disc; included for compatibility with synth version 1. Mode 3 works better (but power works differently).<br>Power adjusts the effect: -1 is a circle (not filled in); higher values fill in towards the center, lower values fill in away from the center (inside-out disc).<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-3.png)](synth-3.flame) | 3: blur (v2), radial, multiply<br>A circle or disc; improved version of mode 2.<br>Power adjusts the effect: 0 is a circle (not filled in); lower values fill in towards the center, higher values fill in away from the center (inside-out disc). -1 is similar to sineblur.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-4.png)](synth-4.flame) | 4: zigzag blur, vertical, multiply<br>A horizontal line or bar; the waveforms will turn it into a zigzag shape. Useful for visualing the waveforms.<br>Power controls the thickness; 0 is the thinnest, increasing or decreasing it thickens it into a bar.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-5.png)](synth-5.flame) | 5: raw circle, radial, multiply<br>Pass the input (like linear) to be multiplied by the waveforms radially. With a single waveform enabled, the effect is similar to blob.<br>Power is not used.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-6.png)](synth-6.flame) | 6: raw x, horizontal, multiply<br>Pass the input (like linear) to be multiplied by the waveforms horizontally.<br>Power is not used.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-7.png)](synth-7.flame) | 7: raw y, vertical, multiply<br>Pass the input (like linear) to be multiplied by the waveforms vertically.<br>Power is not used.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-8.png)](synth-8.flame) | 8: raw x and y, horizontal and vertical, multiply<br>Pass the input (like linear) to be multiplied by the waveforms both horizontally and vertically.<br>Power is not used.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-9.png)](synth-9.flame) | 9: shift x, horizontal, add<br>Pass the input (like linear) to be added to the waveforms horizontally.<br>Power and smooth are not used.
| [![](synth-10.png)](synth-10.flame) | 10: shift y, vertical, add<br>Pass the input (like linear) to be added to the waveforms vertically.<br>Power and smooth are not used.
| [![](synth-11.png)](synth-11.flame) | 11: shift x and y, horizontal and vertical, add<br>Pass the input (like linear) to be added to the waveforms horizontally and vertically.<br>Power and smooth are not used.
|  [![](synth-12.png)](synth-12.flame) | 12: blur ring, radial, multiply<br>A circle or ring.<br>Power controls the thickness; 0 is the thinnest, increasing or decreasing it thickens it into a ring.<br>Smooth selects between linear (0) and Bezier (1) mapping.
| [![](synth-13.png)](synth-13.flame) | 13: blur ring 2, radial, multiply<br>A circle with a different intensity distribution than mode 12.<br>Power controls the thickness; 0 is the thinnest, positive values thicken it towards the inside, negative values thicken it towards the outside.<br>Smooth is not used.
| [![](synth-14.png)](synth-14.flame) | 14: spherical swirl, circular, add<br>Reflects the plane across the unit circle, like the spherical variation and add the waveform to rotate it, giving a swirling effect.<br>Power adjusts the radius calculation; -1 to match the spherical variation, 1 to act like linear.<br>Smooth is not used.
| [![](synth-15.png)](synth-15.flame) | 15: shift tangent, tangential, add<br>Pass the input (like linear) to be added tangentially to the waveforms.<br>Power modifies the waveform, but not the input.<br>Smooth is not used.
| [![](synth-16.png)](synth-16.flame) | 16: shift theta, circular, add<br>Pass the input (like linear) to be rotated by the waveforms, giving a swirling effect.<br>Power modifies the waveform, but not the input; same as mode 14 when power is 1.<br>Smooth is not used.
| [![](synth-17.png)](synth-17.flame) | 17: mirror x, vertical, add<br>Mirror the input across the x axis and add the waveform vertically.<br>Power and smooth are not used.
| [![](synth-18.png)](synth-18.flame) | 18: mirror xy, horizontal and vertical, add<br>Mirror the input across both the x and y axes (same as rotating 180°).<br>Power and smooth are not used.
| [![](synth-19.png)](synth-19.flame) | 19: spherical 2, radial, multiply<br>Reflects the plane across the unit circle, like the spherical variation, but applies the waveform differently from mode 0.<br>Power adjusts the radius calculation; -1 to match the spherical variation, 1 to act like linear.<br>Smooth selects between linear (0) and Bezier (1) mapping.

Modes above 1000 are labeled "failed experiments" by the author. But he kept them available so that others could try them out.

| Example | Mode, Direction, Application, and Description |
| --- | --- |
| [![](synth-1001.png)](synth-1001.flame) | 1001: sinusoidal, horizontal and vertical, mix<br>Transforms the plane like the sinusoidal variation and mixes the result with the waveform, controlled by the mix parameter: 0 is pure sinusoidal, 1 is pure waveform.<br>Power and smooth are not used.
| [![](synth-1002.png)](synth-1002.flame) | 1002: swirl, circular, multiply/mix<br>Transforms the plane like the swirl variation and applies the waveform.<br>Power adjusts the radius calculation; 2 to match the swirl variation, 0 is like linear<br>Smooth selects between multiply (0) and mix (1).
| [![](synth-1003.png)](synth-1003.flame) | 1003: hyperbolic, radial, multiply/mix<br>Transforms the plane like the hyperbolic variation and applies the waveform.<br>Power adjusts the radius calculation; 1 to match the hyperbolic variation.<br>Smooth selects between multiply (0) and mix (1).
| [![](synth-1004.png)](synth-1004.flame) | 1004: julia, radial, multiply/mix<br>Transforms the plane like the julia variation and applies the waveform.<br>Power adjusts the radius calculation; 1 to match the julia variation (it is not like the julian power parameter).<brSmooth selects between multiply (0) and mix (1).
| [![](synth-1005.png)](synth-1005.flame) | 1005: disc, radial, multiply/mix<br>Transforms the plane like the disc variation and applies the waveform.<br>Power adjusts the radius calculation; 1 to match the disc variation.<br>Smooth selects between multiply (0) and mix (1).
| [![](synth-1006.png)](synth-1006.flame) | 1006: rings, radial, multiply/mix<br>Transforms the plane like the rings2 variation and applies the waveform.<br>Power works like the rings2 val parameter except when it is 0.<br>Smooth selects between multiply (0) and mix (1).
| [![](synth-1007.png)](synth-1007.flame) | 1007: cylinder, horizontal, multiply/mix<br>Transforms the plane like the cylinder variation (2D only) and applies the waveform.<br>Power adjusts the radius calculation; 0 to match the cylinder variation.<br>Smooth selects between multiply (0) and mix (1).


### Waveform modules (modules b, c, d, e, and f)
The five waveform modules are invoked in sequence, and, if enabled, apply a waveform. The parameters for each are the same.

| Parameter | Description |
| --- | --- |
| b, c, d, e, f | Amplitude of the waveform for the given module; 0 to disable the module |
| x_type | Shape of the wave<br>0: sine<br>1: cosine<br>2: square<br>3: sawtooth<br>4: triangle<br>5: concave<br>6: convex<br>7: ngon (x_freq is the number of sides)<br>8: inverse ngon |
| x_freq | Frequency of the wave (1 repeats once around the circle if radial, or once per unit otherwise); fractional values are allowed, but create a discontinuity |
| x_skew | Skew effect, between -1 and 1; 0 for normal, -1 for just the left half, 1 for just the right half |
| x_phs | Phase of the wave in radians; 0 for normal |
| x_layer | How this waveform combines with the input:<br>0: add<br>1: multiply<br>2: maximum<br>3: minimum |

### Resources
[Apophysis plugin](https://www.deviantart.com/slobo777/art/Synth-V2-128594088)  
[Synth Variation Explained](https://jwildfire-forum.overwhale.com/viewtopic.php?f=11&t=1219)  
[Flame pack of shapes using synth](https://www.deviantart.com/slobo777/art/Apophysis-Synth-Pack-106698622)  
[The Beginnings tutorial](https://www.deviantart.com/anystasia/art/The-Beginnings-Tutorial-131305834)  
[JWildfire Julian Scary Synth tutorial](https://www.dropbox.com/sh/bt7se699hhfcx8v/AACGi-yoJllws_A1Lf2XJzvza/JWILDFIRE%20JULIA%20N_S%20SCARY%20SYNTH%20TUTORIAL.ppsx?dl=0)   
[Synth Cut Painting video tutorial](https://www.youtube.com/watch?v=QRwUowpLx1Y)  
[Simply Synthfull](https://www.deviantart.com/zweezwyy/art/Simply-Synthfull-128453759)  
[Synth Gardens Apophysis script](https://www.deviantart.com/fractal-resources/art/BC-and-BDs-Synth-Gardens-2-107145254)  
[Curled Synth Apophysis script](https://www.deviantart.com/fractal-resources/art/BD-s-Curled-Synth-Script-105586976)  
[3D Curled Synth Apophysis script](https://www.deviantart.com/fractal-resources/art/BD-s-3D-Curled-Synth-106005764)  
[3D Curled Synth JWildfire script](https://jwildfire-forum.overwhale.com/viewtopic.php?f=17&t=1861)  
[Synth Tiling JWildfire script](https://jwildfire-forum.overwhale.com/viewtopic.php?f=17&t=2087)  
[Inversion Synth JWildfire script](http://jwildfire.org/forum/viewtopic.php?f=17&t=2604)  
[Snarly JWildfire script](http://jwildfire.org/forum/viewtopic.php?f=17&t=2584)  
