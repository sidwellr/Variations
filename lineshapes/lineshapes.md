# Line Shapes
Shape variations made from lines. Like all shape variations, they ignore the input. Most are generated using parametric equations.

## arch
A double arch.

Type: 2D blur  
Author: Antonio Intrieri (gygrazok)  
Date: 9 Feb 2007  

The variation amount controls the extent of the arches. Use 2 for a full double arch; 1 gives the right half.

[![](arch-1.png)](arch-1.flame)

## butterfly_fay
A butterfly shaped curve discovered by Temple H Fay in 1989.

Type: 2D blur  
Author: Gregg Helt (cozyg)  
Date: 24 May 2015  

[![](butterfly_fay-1.png)](butterfly_fay-1.flame)

| Parameter | Description |
| --- | --- |
| offset | Value added to ρ (the distance from the origin) for each point; it expands some parts of the curve while contracting others (the points where ρ is negative) |
| unified_inner_outer | Whether "inner" and "outer" points should be treated the same:<br>0: Treat inner and outer points separately<br>1: Treat all points as outer points (inner parameters will have no effect) |
| outer_mode | Spread mode for outer points; 0 for no spread (outer_spread is ignored); 1, 2, 3, 4, or 5 for different spread effects |
| inner_mode | Spread mode for inner points; 0 for no spread (inner_spread is ignored); 1, 2, 3, 4, or 5 for different spread effects |
| outer_spread | Amount of spread for outer points (all points if unified_inner_outer is 1) |
| inner_spread | Amount of spread for inner points (ignored if unified_inner_outer is 1) |
| outer_spread_ratio | Ratio of horizontal to vertical spreading for outer points; 1 to spread evenly both directions |
| inner_spread_ratio | Ratio of horizontal to vertical spreading for inner points; 1 to spread evenly both directions |
| spread_split | Adjusts the threshold for distinguishing outer and inner points. For some modes, it also changes the spread. |
| cycles | Number of cycles to plot; 0 to calculate automatically |
| fill | Amount of fill to add; 0 for none |

[Wikipedia description](https://en.wikipedia.org/wiki/Butterfly_curve_%28transcendental%29)  
[Mathworld description](https://mathworld.wolfram.com/ButterflyCurve.html)  
[Description and examples by Paul Bourke](http://paulbourke.net/geometry/butterfly/)  

## chrysanthemum
Chrysanthemum flower shaped curve.

Type: 2D blur  
Author: Jesus Sosa  
Date: 1 Feb 2018  

[![](chrysanthemum-1.png)](chrysanthemum-1.flame)

[Description and examples by Paul Bourke](http://paulbourke.net/geometry/chrysanthemum/)  
