# Multiline strings

## esclib.text:Multiline
🟧 Client

``` lua
function esclib.text:Multiline(text, font, mWidth, interval)
```

### Arguments
1. {{types.string}} text
2. {{types.string}} font
3. {{types.number}} MinimumWidth
4. {{types.number}} IntervalBeetweenLines

### Returns
- {{types.table}} multiline_data

!!! tip "Convert to string"
    ``` lua
    function esclib.text:MultilineToString(multiline_data)
    ```

## Draw multiline data
🟧 Client
``` lua
function esclib.text:DrawMultiline(multiline_data, x, y, color, alignX, alignY)
```

### Arguments
1. {{types.table}} multiline_data
2. {{types.number}} x
3. {{types.number}} y
4. {{types.color}} color
5. {{types.text_align}} alignX
6. {{types.text_align}} alignY

!!! tip "To draw shadowed"
    ``` lua
    function esclib.text:DrawMultilineShadow(multiline_data, x, y, color, alignX, alignY, offsetx)
    ```