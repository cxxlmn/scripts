local library = {}

function library:CreateWindow(Name)
    local UI = Instance.new("ScreenGui")
    local Main = Instance.new("ImageLabel")
    local title = Instance.new("TextLabel")
    local togglesandbuttons = Instance.new("ScrollingFrame")
    local UIGridLayout = Instance.new("UIGridLayout")

    UI.Name = "UI"
    UI.Parent = game:WaitForChild("CoreGui")

    Main.Name = "Main"
    Main.Parent = UI
    Main.BackgroundColor3 = Color3.fromRGB(48, 48, 48)
    Main.BackgroundTransparency = 1.000
    Main.Position = UDim2.new(0.455151469, -75, 0.580545306, -37)
    Main.Size = UDim2.new(0, 409, 0, 259)
    Main.Image = "rbxassetid://3570695787"
    Main.ImageColor3 = Color3.fromRGB(48, 48, 48)
    Main.ScaleType = Enum.ScaleType.Slice
    Main.SliceCenter = Rect.new(100, 100, 100, 100)
    Main.SliceScale = 0.120
    Main.Draggable = true
    Main.Active = true
    Main.Selectable = true

    title.Name = "title"
    title.Parent = Main
    title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    title.BackgroundTransparency = 1.000
    title.Position = UDim2.new(0.253381252, 0, 0.0386100374, 0)
    title.Size = UDim2.new(0, 200, 0, 44)
    title.Font = Enum.Font.GothamBold
    title.Text = Name
    title.TextColor3 = Color3.fromRGB(148, 148, 148)
    title.TextSize = 22.000

    togglesandbuttons.Name = "togglesandbuttons"
    togglesandbuttons.Parent = Main
    togglesandbuttons.Active = true
    togglesandbuttons.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    togglesandbuttons.BackgroundTransparency = 1.000
    togglesandbuttons.BorderSizePixel = 0
    togglesandbuttons.Position = UDim2.new(0.0705885738, 0, 0.232102796, 0)
    togglesandbuttons.Size = UDim2.new(0, 368, 0, 198)

    UIGridLayout.Parent = togglesandbuttons
    UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
    UIGridLayout.CellSize = UDim2.new(0, 352, 0, 39)

    local lib = {}

    function lib:CreateToggle(name, callback)
        local actions = {}
        local enabled = false
        name = name or "Name"
        callback = callback or function() end
    
        local togglename = Instance.new("ImageLabel")
        local Toggle = Instance.new("ImageLabel")
        local Button = Instance.new("TextButton")
        local Circle = Instance.new("ImageLabel")
        local titletgl = Instance.new("TextLabel")
    
        togglename.Name = name
        togglename.Parent = togglesandbuttons
        togglename.BackgroundColor3 = Color3.fromRGB(48, 48, 48)
        togglename.BackgroundTransparency = 1.000
        togglename.Position = UDim2.new(0.22854352, -75, 0.374959946, -37)
        togglename.Size = UDim2.new(0, 352, 0, 39)
        togglename.Image = "rbxassetid://3570695787"
        togglename.ImageColor3 = Color3.fromRGB(58, 58, 58)
        togglename.ScaleType = Enum.ScaleType.Slice
        togglename.SliceCenter = Rect.new(100, 100, 100, 100)
        togglename.SliceScale = 0.120
    
        Toggle.Name = "Toggle"
        Toggle.Parent = togglename
        Toggle.BackgroundColor3 = Color3.fromRGB(200, 200, 200)
        Toggle.BackgroundTransparency = 1.000
        Toggle.Position = UDim2.new(0.896413743, -23, 0.5, -11)
        Toggle.Size = UDim2.new(0, 46, 0, 22)
        Toggle.Image = "rbxassetid://3570695787"
        Toggle.ImageColor3 = Color3.fromRGB(200, 200, 200)
        Toggle.ScaleType = Enum.ScaleType.Slice
        Toggle.SliceCenter = Rect.new(100, 100, 100, 100)
        Toggle.SliceScale = 0.120
    
        Button.Name = "Button"
        Button.Parent = Toggle
        Button.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Button.BackgroundTransparency = 1.000
        Button.Size = UDim2.new(1, 0, 1, 0)
        Button.Font = Enum.Font.SourceSans
        Button.TextColor3 = Color3.fromRGB(0, 0, 0)
        Button.TextSize = 14.000
        Button.TextTransparency = 1.000
        --[[Button.MouseButton1Click:Connect(function()
            if shared[name] == true then
                game:GetService("TweenService"):Create(Toggle, TweenInfo.new(0.25), {ImageColor3 = Color3.fromRGB(200, 200, 200)}):Play()
                game:GetService("TweenService"):Create(Circle, TweenInfo.new(0.25), {Position = UDim2.new(0,2,0,2)}):Play()
                shared[name] = false
            elseif shared[name] == false then
                game:GetService("TweenService"):Create(Toggle, TweenInfo.new(0.25), {ImageColor3 = Color3.fromRGB(64, 200, 114)}):Play()
                game:GetService("TweenService"):Create(Circle, TweenInfo.new(0.25), {Position = UDim2.new(1,-20,0,2)}):Play()
                shared[name] = true
            end
        end)]]
    
        local function Fire()
            enabled = not enabled
            if enabled == true then
                game:GetService("TweenService"):Create(Toggle, TweenInfo.new(0.25), {ImageColor3 = Color3.fromRGB(64, 200, 114)}):Play()
                game:GetService("TweenService"):Create(Circle, TweenInfo.new(0.25), {Position = UDim2.new(1,-20,0,2)}):Play()
            elseif enabled == false then
                game:GetService("TweenService"):Create(Toggle, TweenInfo.new(0.25), {ImageColor3 = Color3.fromRGB(200, 200, 200)}):Play()
                game:GetService("TweenService"):Create(Circle, TweenInfo.new(0.25), {Position = UDim2.new(0,2,0,2)}):Play()
            end
            pcall(callback, enabled)
        end
    
        Button.MouseButton1Click:Connect(Fire)
    
        function actions:Set(arg)
            pcall(callback, arg)
        end
        
        Circle.Name = "Circle"
        Circle.Parent = Toggle
        Circle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Circle.BackgroundTransparency = 1.000
        Circle.Position = UDim2.new(0, 2, 0, 2)
        Circle.Size = UDim2.new(0, 18, 0, 18)
        Circle.Image = "rbxassetid://3570695787"
        Circle.ScaleType = Enum.ScaleType.Slice
        Circle.SliceCenter = Rect.new(100, 100, 100, 100)
        Circle.SliceScale = 0.120
        
        titletgl.Name = "titletgl"
        titletgl.Parent = togglename
        titletgl.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        titletgl.BackgroundTransparency = 1.000
        titletgl.Position = UDim2.new(0.0380009711, 0, 0.119394161, 0)
        titletgl.Size = UDim2.new(0, 200, 0, 29)
        titletgl.Font = Enum.Font.GothamBold
        titletgl.Text = name
        titletgl.TextColor3 = Color3.fromRGB(148, 148, 148)
        titletgl.TextSize = 15.000
        titletgl.TextXAlignment = Enum.TextXAlignment.Left
    end
    
    function lib:CreateButton(name,callback)
        local callback = callback or function() end

        local buttonname = Instance.new("ImageLabel")
        local titlebtn = Instance.new("TextLabel")
        local Button_2 = Instance.new("TextButton")
        
        buttonname.Name = "buttonname"
        buttonname.Parent = togglesandbuttons
        buttonname.BackgroundColor3 = Color3.fromRGB(48, 48, 48)
        buttonname.BackgroundTransparency = 1.000
        buttonname.Position = UDim2.new(0.22854352, -75, 0.374959946, -37)
        buttonname.Size = UDim2.new(0, 352, 0, 39)
        buttonname.Image = "rbxassetid://3570695787"
        buttonname.ImageColor3 = Color3.fromRGB(58, 58, 58)
        buttonname.ScaleType = Enum.ScaleType.Slice
        buttonname.SliceCenter = Rect.new(100, 100, 100, 100)
        buttonname.SliceScale = 0.120
    
        titlebtn.Name = "titlebtn"
        titlebtn.Parent = buttonname
        titlebtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        titlebtn.BackgroundTransparency = 1.000
        titlebtn.Position = UDim2.new(0.214137331, 0, 0.119394161, 0)
        titlebtn.Size = UDim2.new(0, 200, 0, 29)
        titlebtn.Font = Enum.Font.GothamBold
        titlebtn.Text = name
        titlebtn.TextColor3 = Color3.fromRGB(148, 148, 148)
        titlebtn.TextSize = 15.000
    
        Button_2.Name = "Button"
        Button_2.Parent = buttonname
        Button_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Button_2.BackgroundTransparency = 1.000
        Button_2.Size = UDim2.new(1, 0, 1, 0)
        Button_2.Font = Enum.Font.SourceSans
        Button_2.TextColor3 = Color3.fromRGB(0, 0, 0)
        Button_2.TextSize = 14.000
        Button_2.TextTransparency = 1.000
        Button_2.MouseButton1Click:Connect(function()
            pcall(callback)
        end)
    end

    return lib

end

return library
