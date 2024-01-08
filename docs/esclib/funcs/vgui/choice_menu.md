---
func_name: esclib:ChoiceMenu
---
# {{func_name}}
🟧 Client

``` lua
function {{func_name}}(title,items,max_selections,item_paint,callback,custom_filter,need_search, selected_values)
```

## Arguments
1. {{types.string}}  title
2. {{types.table}} items
3. {{types.bool}} | {{types.number}} max_selections
4. {{types.function}} item_paint
5. {{types.function}} callback( selected_item )
6. {{types.function}} custom_filter
7. {{types.bool}} need_search
8. {{types.table}} selected_values - Already selected values

## Returns
- {{types.panel}}  GeneratedPanel