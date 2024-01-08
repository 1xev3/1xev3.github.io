---
title: "esclib.draw:Mask"
---
# {{title}}
🟧 Client

``` lua
function {{title}}(func, drawfunc, inverse, reference)
```

## Arguments
1. {{types.function}} function
1. {{types.function}} draw function
1. {{types.bool}} inverse
1. {{types.number}} reference

## Example
This example draws circle avatar
``` lua
function PANEL:Init()
	self.vertices = 360
	self.offset = 0
	self.circle = esclib.draw:GenCircle(self:GetWide()*0.5, self:GetTall()*0.5, self:GetTall()*0.5-self.offset, self.vertices)
	self.clr = Color(60,60,60,200)

	self.avatar = self:Add("AvatarImage")
	local avatar = self.avatar
	avatar:SetSize(self:GetWide(), self:GetTall())
	avatar:SetPlayer(LocalPlayer(), 128)
end

function PANEL:Paint(w,h)
	esclib.draw:Circle(w*0.5,h*0.5, h*0.5, self.clr)

	esclib.draw:Mask(function()
	    draw.NoTexture()
	    surface.SetDrawColor(color_white)
	    surface.DrawPoly(self.circle)
	end,
	function()
		self.avatar:SetPaintedManually(false)
	    self.avatar:PaintManual()
	    self.avatar:SetPaintedManually(true)
	end)
end
```