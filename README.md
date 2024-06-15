local OrionLib = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Orion/main/source'))()

local Window = OrionLib:MakeWindow({
    Name = "Adopt V1",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "OrionTest"
})

local Tab = Window:MakeTab({
    Name = "Auto Farm",
    Icon = "rbxassetid://17616325905",
    PremiumOnly = false
})

local Section = Tab:AddSection({
    Name = "Section"
})

OrionLib:MakeNotification({
    Name = "Title!",
    Content = "Notification content... what will it say??",
    Image = "rbxassetid://4483345998",
    Time = 5
})

Tab:AddLabel("City Farm")

local toggleLoop = false

Tab:AddToggle({
    Name = "Hoop V1",
    Default = false,
    Callback = function(Value)
        toggleLoop = Value
        while toggleLoop do
            local rootpart = game.Players.LocalPlayer.Character.HumanoidRootPart
            for i, v in pairs(workspace.Hoops:GetChildren()) do 
                rootpart.CFrame = v.CFrame 
                wait(0.2) 
            end
        end
    end
})

Tab:AddButton({
    Name = "City Red Orb",
    Callback = function()
        _G.loop = true
        while _G.loop do
            wait()
            for i = 1, 200 do
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City")
            end
        end
    end
})

Tab:AddButton({
    Name = "City Orange Orb",
    Callback = function()
        _G.loop = true
        while _G.loop do
            wait()
            for i = 1, 200 do
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Orange Orb", "City")
            end
        end
    end
})

Tab:AddLabel("Magma Farm")

Tab:AddButton({
    Name = "Magma City Red Orb",
    Callback = function()
        _G.loop = true
        while _G.loop do
            wait()
            for i = 1, 200 do
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "Magma City")
            end
        end
    end
})

Tab:AddButton({
    Name = "Magma City Orange Orb",
    Callback = function()
        _G.loop = true
        while _G.loop do
            wait()
            for i = 1, 200 do
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Orange Orb", "Magma City")
            end
        end
    end
})

local Tab = Window:MakeTab({
	Name = "Anti Kick",
	Icon = "rbxassetid://17621843829",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Anti Kick",
	Callback = function()
      		wait(0.5)local ba=Instance.new("ScreenGui")
local ca=Instance.new("TextLabel")local da=Instance.new("Frame")
local _b=Instance.new("TextLabel")local ab=Instance.new("TextLabel")ba.Parent=game.CoreGui
ba.ZIndexBehavior=Enum.ZIndexBehavior.Sibling;ca.Parent=ba;ca.Active=true
ca.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ca.Draggable=true
ca.Position=UDim2.new(0.698610067,0,0.098096624,0)ca.Size=UDim2.new(0,370,0,52)
ca.Font=Enum.Font.SourceSansSemibold;ca.Text="Anti AFK Script"ca.TextColor3=Color3.new(0,1,1)
ca.TextSize=22;da.Parent=ca
da.BackgroundColor3=Color3.new(0.196078,0.196078,0.196078)da.Position=UDim2.new(0,0,1.0192306,0)
da.Size=UDim2.new(0,370,0,107)_b.Parent=da
_b.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)_b.Position=UDim2.new(0,0,0.800455689,0)
_b.Size=UDim2.new(0,370,0,21)_b.Font=Enum.Font.Arial;_b.Text=" O97 ON YT "
_b.TextColor3=Color3.new(0,1,1)_b.TextSize=20;ab.Parent=da
ab.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ab.Position=UDim2.new(0,0,0.158377,0)
ab.Size=UDim2.new(0,370,0,44)ab.Font=Enum.Font.ArialBold;ab.Text="Status: Active"
ab.TextColor3=Color3.new(0,1,1)ab.TextSize=20;local bb=game:service'VirtualUser'
game:service'Players'.LocalPlayer.Idled:connect(function()
bb:CaptureController()bb:ClickButton2(Vector2.new())
ab.Text="Roblox tried to kick u but i kicked him instead"wait(2)ab.Text="Status : Active"end)
        end    
})

local Tab = Window:MakeTab({
	Name = "Auto Race",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})


Tab:AddButton({
	Name = "Auto Finish Race",
	Callback = function()
while true do
wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=CFrame.new(48.3109131, 36.3147125, -8680.45312, -1, 0, 0, 0, 1, 0, 0, 0, -1)
wait()
  	end
end    
})
