# KingRua Library
This is the stable release of KingRua Library

## Creating the Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/RileyDoesCode/KingRua-Library/refs/heads/main/source.lua"))()
```

## Creating a Window
Create a window to load the ui and change the ui configuration
```lua
local Window = Library:NewWindow({
    Title = "KingRua Library",
    Description = "Welcome",
    Icon = "rbxassetid://124762714875426",
    UITheme = Color3.fromRGB(255, 0, 0),
    ConfigFolder = "KingRuaFolder"
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Icon | ``string`` |
| UITheme | ``Color3.fromRGB`` |
| ConfigFolder | ``string`` |

---

## Creating a Mobile Toggle
Create a mobile toggle to toggle the UI
```lua
local MobileToggle = Library:MobileT({
    Size = UDim2.new(0, 50, 0, 50),
    Icon = "rbxassetid://124762714875426",
    UIStroke = Color3.fromRGB(255, 0, 0),
    UICorner = UDim.new(1, 0)
})
```

| API | Type |
|------|------|
| Size | ``number`` |
| Icon | ``string`` |
| UIStroke | ``Color3.fromRGB`` |
| UICorner | ``number`` |

---

## Creating a Tab
Create a tab to create elements
```lua
local Tab = Window:T("Tab")
```

| API | Type |
|------|------|
| Title | ``string`` |

---

## Creating a Section
Create a section to organize elements
```lua
local Section = Tab:AddSection("Section")
```

| API | Type |
|------|------|
| Title | ``string`` |

---

## Creating a Toggle
Create a toggle to make function/script work
```lua
Section:AddToggle({
    Title = "Toggle",
    Description = "This is a toggle",
    Default = false,
    Flag = "toggle1",
    Callback = function(value)
        -- ...
    end
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Default | ``boolean`` |
| Flag | ``string`` |
| Callback | ``function`` |

---

## Creating a Button
Create a button to make function/script work
```lua
Section:AddButton({
    Title = "Click me!",
    Description = "This is an button",
    Callback = function()
        -- ...
    end
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Callback | ``function`` |

---

## Creating a Slider
Create a Slider to make function/script work
```lua
Section:AddSlider({
    Title = "Slider",
    Description = "This is a Slider",
    Min = 16,
    Max = 100,
    Increment = 1,
    Default = 16,
    Callback = function(value)
        -- ...
    end
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Min | ``number`` |
| Max | ``number`` |
| Increment | ``number`` |
| Default | ``number`` |
| Callback | ``function`` |

---

## Creating a Dropdown
Create a dropdown to make function/script work
```lua
Section:AddDropdown({
    Title = "Dropdown",
    Description = "This is a Dropdown",
    Values = {"One", "Two", "Three", "Four"},
    Default = "One",
    Multi = false,
    Callback = function(value)
        -- ...
    end
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Values | ``table`` |
| Default | ``string`` |
| Multi | ``boolean`` |
| Callback | ``function`` |

---

## Creating a Input
Create a input to make function/script work
```lua
Section:AddInput({
    Title = "Adaptive Input",
    Description = "Input your text here",
    PlaceHolder = "Type here...",
    Default = "Hi",
    Callback = function(value)
        -- ...
    end
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Description | ``string`` |
| Placeholder | ``string`` |
| Default | ``string`` |
| Callback | ``function`` |

---

## Creating a Paragraph
Create a paragraph to input informations and text
```lua
local Paragraph = Section:AddParagraph({
    Title = "Paragraph Title",
    Content = "This is an Description"
})
```

| API | Type |
|------|------|
| Title | ``string`` |
| Content | ``string`` |

---

# Update Functions

## Update Paragraph Title
```lua
Paragraph:SetTitle("Updated Title")
```

## Update Paragraph Content
```lua
Paragraph:SetDesc("Updated Description")
```

# Configuration System

## Save Configuration
```lua
Library:SaveConfig("MySettings")
```

## Load Configuration
```lua
Library:LoadConfig("MySettings")
```
