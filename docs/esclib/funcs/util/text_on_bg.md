---
title: "esclib.util:TextOnBG"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(bgCol, col_white, col_black)
```

## Arguments
1. {{types.color}} BackgroundColor
2. {{types.color}} BrightColor
3. {{types.color}} DarkColor

## Returns
1. {{types.color}} DecidedColor (`col_white` if `mean(bgCol)` < `127` else `col_black`)