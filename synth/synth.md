# Synth
Variations that emulate a number of other variations, adding wavy effects using a technique from audio synthesizers.

## synth v1
The first version of synth is still available, but superceded by synth V2. It doesn't have as many options, but works the same as the later version, so see its description below for details.

Type: 2D; blur with mode 2  
Author: Neil Slater  
Date: 24 Sep 2008  

https://www.deviantart.com/slobo777/art/Apo-plugin-Synth-98877432

## synth v2
Combo variation (emulates several others) with added wave functions.

Type: 2D; blur with modes 2, 3, 4, 12, and 13  
Author: Neil Slater  
Date: 7 Jul 2009  

Synth is complicated because it has so many parameters. Understanding the basic structure of the variation is helpful. Synth is made from six modules, named 'a' through 'f' that are mostly independent from each other. Module a takes the input point and transforms it like a typical variation; the mode parameter determines how it works. The output from Module a is passed into Modules b through f in turn, each of which superimposes a waveform. The output of the last module is the output of the variation.

### Main module (module a)
Module a applies a variation to the input; some match other variations, some are unique to synth. Parameter mode specifies the variation to use; the others modify it.

| Parameter | Description |
| --- | --- |
| a | The amount of the variation (normally 1) |
| mode | The variation to use (see next table) |
| power | Controls the power of the variation (not used by all modes) |
| mix | How much of the waveforms to mix in; 1 is normal, 0 ignores the waveforms |
| smooth | 0 to disable and 1 to enable smoothing (not used by all modes) |

The following table describes the modes.

| Mode/Direction | Example | Description |
| --- | --- | --- |
| 0: spherical<br>radial | [![](synth-0.png)](synth-0.flame) | Reflects the plane across the unit circle, like the spherical variation.<br>Power adjusts the effect; -2 to match the spherical variation, 0 to act like linear.<br>Smooth distorts the waveform if enabled.
| 1: bubble<br>radial | [![](synth-1.png)](synth-1.flame) | Maps the plane to a sphere, like the bubble variation but not 3D even in 3D flame programs.<br>Power is not used.<br>Smooth distorts the waveform if enabled.
| 2: blur (v1)<br>radial | [![](synth-2.png)](synth-2.flame) | A circle or disc; included for compatibility with synth version 1. Mode 3 works better (but power works differently).<br>Power adjusts the effect: -1 is a circle (not filled in); higher values fill in towards the center, lower values fill in away from the center (inside-out disc).<br>Smooth decreases the waveform effects away from the unit circle.
| 3: blur (v2)<br>radial | [![](synth-3.png)](synth-3.flame) | A circle or disc; improved version of mode 2.<br>Power adjusts the effect: 0 is a circle (not filled in); lower values fill in towards the center, higher values fill in away from the center (inside-out disc). -1 is similar to sineblur.<br>Smooth helps smooth out distortions if enabled.
| 4: zigzag blur<br>vertical | [![](synth-4.png)](synth-4.flame) | A horizontal line or bar; the waveforms will turn it into a zigzag shape. Useful for visualing the waveforms.<br>Power controls the thickness; 0 is the thinnest, increasing or decreasing it thickens it into a bar.<br>Smooth distorts the thickness if enabled; this is sometimes attractive.
| 5: raw circle<br>radial | [![](synth-5.png)](synth-5.flame) | Copy the input (like linear) to be modified by the waveforms radially. With a single waveform enabled, the effect is similar to blob.<br>Power is not used.<br>Smooth applies smoothing if enabled.
| 6: raw x<br>horizontal | [![](synth-6.png)](synth-6.flame) | Copy the input (like linear) to be modified by the waveforms horizontally.<br>Power is not used.<br>Smooth applies smoothing if enabled.
| 7: raw y<br>vertical | [![](synth-7.png)](synth-7.flame) | Copy the input (like linear) to be modified by the waveforms vertically.<br>Power is not used.<br>Smooth applies smoothing if enabled.
| 8: raw xy<br>horizontal and vertical | [![](synth-8.png)](synth-8.flame) | Copy the input (like linear) to be modified by the waveforms both horizontally and vertically.<br>Power is not used.<br>Smooth applies smoothing if enabled.


### Waveform modules (modules b, c, d, e, and f)
The five waveform modules are invoked in sequence, and, if enabled, apply a waveform. The parameters for each are the same.

| Parameter | Description |
| --- | --- |
| b, c, d, e, f | Amplitude of the waveform for the given module; 0 to disable the module |
| x_type | Shape of the wave<br>0: sine<br>1: cosine<br>2: square<br>3: sawtooth<br>4: triangle<br>5: concave<br>6: convex<br>7: triangle |
| x_freq | Frequency of the wave (1 repeats once around the circle); fractional values are allowed, but create a discontinuity |
| x_skew | Skew effect, between -1 and 1; 0 for normal, -1 for just the left half, 1 for just the right half |
| x_phs | Phase of the wave in radians; 0 for normal |
| x_layer | How this waveform combines with the input:<br>0: add<br>1: multiply<br>2: maximum<br>3: minimum |

### Using synth

### Resources
https://www.deviantart.com/slobo777/art/Synth-V2-128594088  
http://jwildfire.org/forum/viewtopic.php?f=11&t=1219  
https://www.deviantart.com/slobo777/art/Apophysis-Synth-Pack-106698622  
https://www.deviantart.com/anystasia/art/The-Beginnings-Tutorial-131305834  
https://www.dropbox.com/sh/bt7se699hhfcx8v/AACGi-yoJllws_A1Lf2XJzvza/JWILDFIRE%20JULIA%20N_S%20SCARY%20SYNTH%20TUTORIAL.ppsx?dl=0   
https://www.youtube.com/watch?v=QRwUowpLx1Y  
https://www.deviantart.com/fractal-resources/art/BC-and-BDs-Synth-Gardens-2-107145254  
https://www.deviantart.com/fractal-resources/art/BD-s-Curled-Synth-Script-105586976  
https://www.deviantart.com/fractal-resources/art/BD-s-3D-Curled-Synth-106005764  
http://jwildfire.org/forum/viewtopic.php?f=17&t=1861  
https://www.deviantart.com/zweezwyy/art/Simply-Synthfull-128453759  
http://jwildfire.org/forum/viewtopic.php?f=17&t=2087  
http://jwildfire.org/forum/viewtopic.php?f=17&t=2604  
http://jwildfire.org/forum/viewtopic.php?f=17&t=2584  
