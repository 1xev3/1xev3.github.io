# Using esclib loader

## An example of one of my addons
``` lua
echat = echat or {} -- initialize
echat.Materials = echat.Materials or {}

local function loader()
	print("[echat loader]")
	--Using esclib loader system
	esclib.loader:New("echat","echat/",function(load)
		--fonts used in addon
		load:Resource("resource/fonts/inter_regular.ttf")
		load:Resource("resource/fonts/robotomono_regular.ttf")

		load:MaterialFolder("materials/echat",false,true)
		table.Merge(echat.Materials, load.Materials)

		--CONFIGS
		load:Shared("config/meta.lua") -- creating addon instance
		load:Shared("config/config.lua")
		load:Shared("config/ingame_config.lua")
		load:Client("config/themes.lua")
		load:Client("config/languages.lua")

		--VGUI
		load:ClientFolder("vgui")

		--MAIN FILES
		load:Shared("core/tools/fonts.lua")
		load:Client("core/tools/module_loader.lua")
		load:Shared("core/tools/parsers_core.lua")
		load:Client("core/tools/auto_complete.lua")
		load:Server("core/tools/server_funcs.lua")
		
		load:Shared("core/parsers.lua")
		load:Client("core/complete_helpers.lua")

		--load all files from modules folder
		load:SharedFolder("core/modules")

		--Main app
		load:Client("core/__core__.lua")

	end)
end

--lua refresh compat
if esclib && esclib.loader then
	if esclib.loader:IsLoaded("echat") then
		loader()
	end
end

--adding hook to watch
hook.Add("esclib_loaded", "echat_load", function()
	loader()
end)
```