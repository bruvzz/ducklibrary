# Duck Library
Welcome to the Documentation of Duck Library! Here is step-by-step guide on how to use different features with the user-interface.

## Creating the Library
```lua
local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/bruvzz/ducklibrary/main/src.lua")()
```

## Creating a Window
```lua
local Win = lib:Window("Your Title Here", Color3.fromRGB(44, 120, 224), Enum.KeyCode) -- (text, color, Enum.KeyCode) --
-- Please keep "Enum.KeyCode" as stated or else library could break. --
```

## Creating a Tab
```lua
local Tab_1 = Win:Tab('Tab 1')
```

## Create a Button
```lua
Tab_1:Button('This is a Button!', function() -- (text, callback) --

    print("Clicked!")

end)
```

## Create a Toggle
```lua
Tab_1:Toggle('This is a Toggle', false, function(value) -- (text, default, callback) --

    print(value)

end)
```

## Create a Slider
```lua
Tab_1:Slider('This is a Slider!', 0, 20, 0, function(value) -- (text, minimum, maximum, start, callback) --

    print(value)

end)
```

## Create a Dropdown
```lua
Tab_1:Dropdown("This is a Dropdown!", {"test 1", "test 2", "test 3", "test 4"}, function(v) -- (text, list, callback) --

    print(v)

end)
```

## Create a Textbox
```lua
Tab_1:Textbox("This is a Textbox!", false, function(value) -- (text, dissapear, callback) --

print(value)
    
end)
```

## Create a Colorpicker
```lua
Tab_1:Colorpicker("Change UI Color",Color3.fromRGB(44, 120, 224), function(t) -- (text, color, callback) --
    lib:ChangePresetColor(Color3.fromRGB(t.R * 255, t.G * 255, t.B * 255))
end)
```

## Create a Label
```lua
Tab_1:Label('This is a Label!') -- (text) --
```

## Make a Notification
```lua
lib:Notification("Success", "Clicked!", "Close") -- (header, text, closebutton) --
```
