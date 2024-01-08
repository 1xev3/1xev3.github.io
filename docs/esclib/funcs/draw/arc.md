---
title: "esclib.draw:Arc"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(cx,cy,radius,thickness,startang,endang,roughness,color,bClockwise)
```

!!! danger "Vertices are created at each rendering frame"
    If the number of vertices is large, I do not recommend to use this function in drawing functions.

## Arguments
1. {{types.number}} center x
1. {{types.number}} center y
1. {{types.number}} arc radius
1. {{types.number}} thickness
1. {{types.number}} start angle
1. {{types.number}} end angle
1. {{types.number}} roughness
1. {{types.number}} color
1. {{types.bool}} clockwise?

