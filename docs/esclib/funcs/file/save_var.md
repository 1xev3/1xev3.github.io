---
title: "esclib.file:SaveVar"
---
# {{title}}
🟧 Client / 🟦 Server

``` lua
function {{title}}(path,content)
```

Creates a file and saves table to it

## Arguments
1. {{types.string}} path
1. {{types.table}} content

## Example
``` lua
esclib.file:SaveVar("ehud/savedvars.txt",{["hello"]={"214151","215161664",""}})
print(esclib.file:ReadVar("ehud/savedvars.txt","hello")) --{"214151","215161664"}
```