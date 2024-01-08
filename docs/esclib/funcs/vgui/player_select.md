---
func_name: esclib:PlayerSelectWindow
---
# {{func_name}}
🟧 Client

``` lua
function {{func_name}}(title,multi,hide_self,callback,custom_filter)
```

## Arguments
1. {{types.string}} title
2. {{types.bool}} | {{types.number}} multi - Number to be selected
4. {{types.bool}} hide_self
5. {{types.function}} callback( selected_item )
6. {{types.function}} custom_filter

## Returns
- {{types.panel}} GeneratedPanel