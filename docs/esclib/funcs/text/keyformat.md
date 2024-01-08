---
func_name: esclib.text:KeyFormat
---
# {{func_name}}
🟧 Client

``` lua
function {{func_name}}(str, replacements)
```

## Arguments
1. {{types.string}} str
2. {{types.table}} replacements

## Returns
- {{types.string}} ReplacedString

## Example
``` lua
local to_format_str = "Hello {rank}"
local formated_str = {{func_name}}(to_format_str, {
    ["rank"] = "MyUniqueRank",
})
print(formated_str) -- Will be Hello MyUniqueRank
```