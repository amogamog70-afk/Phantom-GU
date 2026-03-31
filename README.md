# MyLib — Roblox UI Library

## Подключение
```lua
local MyLib = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/ТЫ/MyLib/main/source.lua"
))()
```

## Пример использования
```lua
local win = MyLib.new({ Title = "MyMenu", Subtitle = "v1.0", ConfigName = "cfg" })

local tab = win:AddTab("🎮 Игрок")
tab:AddSection("Движение")
tab:AddToggle({ Name = "Inf Jump",  Key = "infjump",  Default = false, Callback = function(v) end })
tab:AddSlider({ Name = "WalkSpeed", Key = "speed",    Min = 16, Max = 200, Default = 16, Callback = function(v)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
end })
tab:AddDropdown({ Name = "Team", Key = "team", Items = {"Red", "Blue", "Green"}, Callback = function(v) end })
tab:AddTextbox({ Name = "Имя игрока", Key = "targetname", Placeholder = "Введи ник..." })
tab:AddButton({ Name = "Телепорт", Callback = function() end })
```
