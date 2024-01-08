---
title: "esclib.util:NumberLimit"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(number, min, max, str_format)
```

## Arguments
1. {{types.number}} number
2. {{types.number}} minimum to be formated
3. {{types.number}} maximum to be formated
4. `Optional` {{types.string}} format string

## Returns
1. {{types.string}} Formatted string

## Example
``` lua
print(esclib.util:NumberLimit(500, 200, 300)) --will be 300+
print(esclib.util:NumberLimit(100, 200, 300)) --will be <200
```