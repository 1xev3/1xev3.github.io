---
title: "esclib.util:IsRestrictedChar"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(str)
```

## Arguments
1. {{types.string}} string to check

## Returns
1. {{types.bool}} Is restricted?

## Restricted list
``` lua
esclib.restricted_chars = {
	["\\"] = true,
	["/"] = true,
	[":"] = true,
	["*"] = true,
	["?"] = true,
	['"'] = true,
	["'"] = true,
	["<"] = true,
	[">"] = true,
	["|"] = true,
	["CON"] = true,
	["PRN"] = true,
	["AUX"] = true,
	["NUL"] = true,
	["COM"] = true,
	["LPT"] = true,
}
```