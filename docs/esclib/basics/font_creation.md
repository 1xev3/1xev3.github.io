# Fonts

### Set current font name
``` lua
esclib:SetFontName(string)
```

### Select font from system:
``` lua
esclib:SetFont(string) --font name in system
```

### Create new font
``` lua
esclib:Font(int size, int weight)
```
#### Returns:
- [string](https://wiki.facepunch.com/gmod/string) fontname

### Example
``` lua title="fonts.lua"
esclib:SetFontName("esclib") --font name
esclib:SetFont("Amsterdam")
esclib:Font(30,500) --es_esclib_30_500
esclib:Font(26,500)
esclib:Font(24,500)
esclib:Font(22,500)
esclib:Font(20,500)
esclib:Font(18,500)
esclib:Font(16,500)
esclib:Font(10,500)
```