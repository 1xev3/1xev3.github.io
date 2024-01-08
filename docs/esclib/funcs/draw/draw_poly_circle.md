---
title: "esclib.draw:PolyCircle"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(x, y, r, col, v)
```

!!! danger "Vertices are created at each rendering frame"
    If the number of vertices is large, I do not recommend to use this function in drawing functions.

## Arguments
1. {{types.number}} x
1. {{types.number}} y
1. {{types.number}} radius
1. {{types.color}} circle color
1. {{types.number}} number of vertices