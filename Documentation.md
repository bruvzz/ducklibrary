# Duck Library
Welcome to the Documentation of Duck Library! Here is step-by-step guide on how to use different features with the user-interface.

## Creating the Library
```lua
local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/bruvzz/ducklibrary/main/src.lua")()
```

## Creating a Window
```lua
local Win = lib:Window("Your Title Here",Color3.fromRGB(44, 120, 224), Enum.KeyCode)
-- If you would like to have a Rainbow Title, put 'PresetColor' in between the set of parenthesis --
```

## Creating a Tab
```lua
local Tab_1 = Window:Tab('Tab 1')
```

## Create a Button
```lua
Tab_1:Button('This is a Button!', function()

    print("Clicked!")

end)
```

## Create a Toggle
```lua
Tab_1:Toggle('This is a Toggle', function(value)

print(value)

end)
```

## Create a Slider
```lua
Tab_1:Slider('This is a Slider!', 0, 20, 0, function(value)

    print(value)

end)
```

## Create a Dropdown
```lua
Tab_1:Dropdown("This is a Dropdown!", {"test 1", "test 2", "test 3", "test 4"}, function(v)

print(v)

end)
```

## Create a Colorpicker
```lua
Tab_1:Colorpicker("Change UI Color",Color3.fromRGB(44, 120, 224), function(t)
    lib:ChangePresetColor(Color3.fromRGB(t.R * 255, t.G * 255, t.B * 255))
end)
```

## Create a Label
```lua
Tab_1:Label('This is a Label!')
```
