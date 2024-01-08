# Addon meta

## Creating new addon

``` lua title="🟧🟦 meta.lua"
your_name = your_name or {} -- create global table with your addon

your_name.addon = esclib:Addon("YOUR_ADDON_UID")
your_name.addon:SetName("YOUR_ADDON_NAME") --visible name
your_name.addon:SetBranch("YOUR_BRANCH_NAME") --(f.e main or dev)
your_name.addon:SetVersion(0.1) --float or string
your_name.addon:SetDescription("Chat for Gmod")
```

---
## Themes

``` lua title="🟧 theme.lua"
local skin = {}
skin.name = "Blackout" --theme name
skin.color = Color(13,13,13) --theme color in settings menu
skin.colors = {}
skin.colors.main = {
	bg = Color(26, 27, 30, 250),
	bg2 = Color(14, 17, 14),

	button = Color(1, 10, 25),
	button_hover = Color(20, 30, 45),
	accent = Color(153,0,255),
	scrollbar = Color(57, 57, 59),
	text_entry = Color(14, 17, 14),

	text = Color(255,255,255),
	text_gray = Color(160,160,160),
	text_selection = Color(92, 79, 238),
}

your_name.addon:RegisterSkin("blackout", skin)
```

!!! tip "Setting default skin"
    ``` lua
    your_name.addon:SetDefaultSkin("blackout")
    ```

---
## Languages

``` lua title="🟧🟦 languages.lua"

local langs = {
	["en"] = {
		__name__ = "English", --name in game
		__code__ = "US", --Language code: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2

        text_example = "Text example",
	},
	["ru"] = {
		__name__ = "Russian",
		__code__ = "RU",

		text_example = "Пример текста",
	}
}

your_name.addon:RegisterLanguages(langs)

-- if GetConVar("gmod_language") not in languages table, sets this language
your_name.addon:SetDefaultLanguage("en")
```

To get var, simple use:

``` lua
your_name.addon:Translate("text_example")
```

---
## Settings

### Var types
| Type        | Description                          |
| :---------: | :----------------------------------: |
| `bool`      | Simple true/false clickable button   |
| `numslider` | Numeric slider |
| `float` | Same as numslider but different look |
| `choicelist`| Select from list |


### Example
``` lua title="🟧🟦 ingame_config.lua"
local settings = esclib:InitSettings("echat")

--tab creating
local tab = settings:AddTab("modules") --uid
tab:SetNameTranslateKey("tab_modules") --key in language file
tab:SetPosition(1) --postion

--adding vars
local var = tab:AddVar("module_hud_leftbot", "bool")
var:SetNameTranslateKey("s_mainhud_name") --key in language file
var:SetValue(true)

--Animation time slider
local var = tab:AddVar("animtime", "numslider")
var:SetNameTranslateKey("s_animspeed_name")
var:SetValue(0.2)
var:SetMin(0.01)
var:SetMax(3)
var:SetDecimals(2)
var:SetStep(0.1)

settings:End()
```