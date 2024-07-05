--Criminality

local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Moon Hub",
    SubTitle = "by Official",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true, -- The blur may be detectable, setting this to false disables blur entirely
    Theme = "Rose",
    MinimizeKey = Enum.KeyCode.RightShift-- Used when theres no MinimizeKeybind
})

--Fluent provides Lucide Icons https://lucide.dev/icons/ for the tabs, icons are optional
local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "menu" }),
    ESPs = Window:AddTab({ Title = "ESP's", Icon = "eye" }),
    Fun = Window:AddTab({ Title = "Fun/Troll", Icon = "ghost"}),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" }),
    Paid = Window:AddTab({ Title = "Paid Client", Icon = "dollar-sign"})
}

local Options = Fluent.Options

do
    Fluent:Notify({
        Title = "Moon Hub",
        Content = "Script By Official",
        SubContent = "be good not bad - wise man", -- Optional
        Duration = 15 -- Set to nil to make the notification not disappear
    })

    Tabs.Paid:AddButton({
        Title = "Paid Access",
        Description = "If you want Paid Access, DM hitmancrim on Discord.",
        Callback = function(sabfe)
			print("DM hitmancrim on Discord, if you want the paid access.")
            Fluent:Notify({
                Title = "Paid Access",
                Content = "DM hitmancrim on Discord",
                SubContent = "", -- Optional
                Duration = 10 -- Set to nil to make the notification not disappear
            })
        end
    })
    
    Tabs.ESPs:AddButton({
        Title = "Safe / Register Esp",
        Description = "Shows you the non-broken registers / safes (can be stopped by rejoining)",
        Callback = function(safe)
			loadstring(game:HttpGet("https://pastebin.com/raw/UecuQPfV"))()
        end
    })

    Tabs.ESPs:AddButton({
        Title = "Normal Dealer Esp",
        Description = "Shows you the dealers around the map (Green = Normal / Blue = Armory)",
        Callback = function(NDealer)
			loadstring(game:HttpGet("https://pastebin.com/raw/Nwd0fp0U"))()
        end
    })

    Tabs.ESPs:AddButton({
        Title = "Rebel Dealer Esp",
        Description = "Shows you the rebel dealear's location (if spawned)",
        Callback = function(RDealer)
			loadstring(game:HttpGet("https://pastebin.com/raw/mnfA9Z3p"))()
        end
    })

    Tabs.ESPs:AddButton({
        Title = "Trash pile esp",
        Description = "Shows you the trash piles spawned around you",
        Callback = function(trash)
			loadstring(game:HttpGet("https://pastebin.com/raw/4ddw3JcM"))()
        end
    })

    Tabs.Fun:AddButton({
        Title = "Fling",
        Description = "Run into people to fling them",
        Callback = function(fling)
			loadstring(game:HttpGet('https://raw.githubusercontent.com/sauga77kjk/RobloxExploitRepository/main/TouchFLING'))()
        end
    })

    --Tabs.ESPs:AddButton({
       -- Title = "Spawned/Dropped tools Esp",
        --Description = "Shows you the dropped / spawned tools around you. (can be guns)",
        --Callback = function(tool)
			--loadstring(game:HttpGet("https://pastebin.com/raw/GV8Vu3kj"))()
        --end
    --})

    --local Slider = Tabs.Fun:AddSlider("Slider", {
		--Title = "Spinbot",
		--Description = "Speed (To stop it make the speed 0, if it doesnt work just reset ur character)",
		--Default = 0,
		--Min = 0,
		--Max = 100,
		--Rounding = 1,
		--Callback = function(Spin)
			--local speed = Spin

            --local plr = game:GetService("Players").LocalPlayer
            --repeat task.wait() until plr.Character
            --local humRoot = plr.Character:WaitForChild("HumanoidRootPart")
            --plr.Character:WaitForChild("Humanoid").AutoRotate = false
            --local velocity = Instance.new("AngularVelocity")
            --velocity.Attachment0 = humRoot:WaitForChild("RootAttachment")
            --velocity.MaxTorque = math.huge
            --velocity.AngularVelocity = Vector3.new(0, speed, 0)
            --velocity.Parent = humRoot
            --velocity.Name = "Spinbot"
		--end
	--})

    Tabs.Main:AddButton({
        Title = "Aimlock (Aimbot)",
        Description = "Locks to persons parts (Right Click) ('X' to toggle)",
        Callback = function(Aimlock)
			loadstring(game:HttpGet("https://pastebin.com/raw/hTW4SLHN"))()
        end
    })

    Tabs.Main:AddButton({
        Title = "Wallbang",
        Description = "Lets you shoot people thru walls (2 max)",
        Callback = function(Wallbang)
            game:service[[Workspace]]:FindFirstChild('Map'):FindFirstChild('Parts'):FindFirstChild('M_Parts').Parent = game:service[[Workspace]]:FindFirstChild('Characters')
        end
    })

	Tabs.Main:AddButton({
        Title = "ESP",
        Description = "Esp",
        Callback = function(esp)
			loadstring(game:HttpGet('https://pastebin.com/raw/4HGLYvaH'))()
        end
    })

    Tabs.Main:AddButton({
        Title = "Tool Esp",
        Description = "Shows what tool the player is holding (To toggle it click P)",
        Callback = function(tol)
			loadstring(game:HttpGet('https://pastebin.com/raw/4JWGJLqD'))()
        end
    })


	--local Camera = game.Workspace.CurrentCamera

	--local Slider = Tabs.Main:AddSlider("Slider", {
		--Title = "FOV changer",
		--Description = "FOV",
		--Default = 60,
		--Min = 60,
		--Max = 120,
		--Rounding = 1,
		--Callback = function(Value)
		--	Camera.FieldOfView = Value
		--end
	--})

    Tabs.Main:AddButton({
        Title = "Normal Flight",
        Description = "Fly using 'z'. (dont fly for long periods of time or the AC will flag you) (re-execute on death or reset)",
        Callback = function(flight)
			loadstring(game:HttpGet("https://pastebin.com/raw/DnBbHNSC"))()
        end
    })

    Tabs.Main:AddButton({
        Title = "Glide Fly",
        Description = "Flight Bind: B - Fly/Speed; U - Only Speed",
        Callback = function(esp)
			togglekey = "b"  -- fly toggle
upkey = "="      -- makes speed faster
downkey = "-"    -- makes speed slower
enablepart = "u" -- enables part fly
speed = -0.5     -- changes set speed
updown = false   -- true if you want to go up
notify = true    -- true if you want notifcations
flypart = true   -- true for part fly
local user = game:GetService("UserInputService")
local player = game:GetService("Players").LocalPlayer
local GuiService = game:GetService("StarterGui")
local mouse = game.Players.LocalPlayer:GetMouse()
local holdingWKey = false
local holdingSKey = false
local holdingAKey = false
local holdingDKey = false
local holdingSpaceKey = false
local holdingShiftKey = false
local check = false
GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Script made by Zurewrath";})
mouse.KeyDown:connect(function(key)
   if key == enablepart then
       if flypart then
           flypart = false
           if notify then
               GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Disabled part fly";})
           end
       else
           flypart = true
           if notify then
               GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Enabled part fly";})
           end
       end
   end
end)
mouse.KeyDown:connect(function(key)
   if key == upkey then
       speed = speed + -0.1
       if notify then
           GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Speed is now set to " .. speed;})
       end
   end
end)
mouse.KeyDown:connect(function(key)
   if key == downkey then
       speed = speed - -0.1
       if notify then
           GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Speed is now set to " .. speed;})
       end
   end
end)
mouse.KeyDown:connect(function(key)
   if key == togglekey then
       if check  == true then
           check = false
           if notify then
               GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Speed is now disabled";})
           end
           game.Workspace.fly:Destroy()
       else
           check = true
           if notify then
               GuiService:SetCore("SendNotification", {Title = "Speed", Text = "Speed is now enabled";})
           end
           if flypart then
               local brick = Instance.new("Part", workspace)
               brick.Size = Vector3.new(8, 2, 8)
               brick.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame + Vector3.new(0, -4, 0)
               brick.Transparency = 1 brick.Anchored = true brick.Name = "fly"
               game:GetService('RunService').Stepped:connect(function()
                   brick.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame + Vector3.new(0, -4, 0)
                   brick.Size = Vector3.new(8+-speed, 2, 8+-speed)
               end)
           end
       end
   end
end)
game:GetService('RunService').Stepped:connect(function()
   if check then
       if holdingWKey == true then
         game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,speed)
       end
       if holdingSKey == true then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-speed)
   end
       if holdingAKey == true then
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(speed,0,0)
   end
       if holdingDKey == true then
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(-speed,0,0)
       end
       if holdingShiftKey == true then
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,speed,0)
       end
       if updown then
           if holdingSpaceKey == true then
               game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,-speed,0)
           end
       end
   end
end)
user.InputBegan:Connect(function(inputObject)
   if (inputObject.KeyCode == Enum.KeyCode.W) then
       holdingWKey = true
   end
   if (inputObject.KeyCode == Enum.KeyCode.S) then
       holdingSKey = true
   end
   if (inputObject.KeyCode == Enum.KeyCode.A) then
       holdingAKey = true
   end
   if (inputObject.KeyCode == Enum.KeyCode.D) then
       holdingDKey = true
   end
   if (inputObject.KeyCode == Enum.KeyCode.LeftControl) then
       holdingShiftKey = true
   end
   if (inputObject.KeyCode == Enum.KeyCode.Space) then
       holdingSpaceKey = true
   end
end)
user.InputEnded:Connect(function(inputObject)
   if (inputObject.KeyCode == Enum.KeyCode.W) then
       holdingWKey = false
   end
   if( inputObject.KeyCode == Enum.KeyCode.S) then
       holdingSKey = false
   end
   if (inputObject.KeyCode == Enum.KeyCode.A) then
       holdingAKey = false
   end
   if (inputObject.KeyCode == Enum.KeyCode.D) then
       holdingDKey = false
   end
   if (inputObject.KeyCode == Enum.KeyCode.LeftControl) then
       holdingShiftKey = false
   end
   if (inputObject.KeyCode == Enum.KeyCode.Space) then
       holdingSpaceKey = false
   end
end)
        end
    })

    local Slider = Tabs.Main:AddSlider("Slider", {
		Title = "Gravity",
		Description = "How high u jump (196 - normal / 95 - best option (so AC doesnt fuck u up)",
		Default = 196,
		Min = 70,
		Max = 196,
		Rounding = 1,
		Callback = function(Value)
			game.workspace.Gravity = Value
		end
	})

    --local Slider = Tabs.Main:AddSlider("Slider", {
		--Title = "Stomp Speed",
		--Description = "Speed",
		--Default = 1,
		--Min = 0.5,
		--Max = 2.2,
		--Rounding = 1,
		--Callback = function(Value)
			--game:GetService("ReplicatedStorage").Values.FinishSpeedMulti.Value = Value
		--end
	--})

    Tabs.Main:AddButton({
        Title = "Lockpick Helper",
        Description = "Makes lockpicking easy!",
        Callback = function()
			loadstring(game:HttpGet("https://raw.githubusercontent.com/Iceyze/crim-autolockpick/main/main.lua"))()
        end
    })

    Tabs.Main:AddButton({
        Title = "Brightness",
        Description = "Makes ur game brighter then normal",
        Callback = function()
			local Light = game:GetService("Lighting")
            function dofullbright()
            Light.Ambient = Color3.new(1, 1, 1)
            Light.ColorShift_Bottom = Color3.new(1, 1, 1)
            Light.ColorShift_Top = Color3.new(1, 1, 1)
            end
            
            dofullbright()

            Light.LightingChanged:Connect(dofullbright)
        end
    })



-- Addons:
-- SaveManager (Allows you to have a configuration system)
-- InterfaceManager (Allows you to have a interface managment system)

-- Hand the library over to our managers
SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)

-- Ignore keys that are used by ThemeManager.
-- (we dont want configs to save themes, do we?)
SaveManager:IgnoreThemeSettings()

-- You can add indexes of elements the save manager should ignore
SaveManager:SetIgnoreIndexes({})

-- use case for doing it this way:
-- a script hub could have themes in a global folder
-- and game configs in a separate folder per game
InterfaceManager:SetFolder("FluentScriptHub")
SaveManager:SetFolder("FluentScriptHub/specific-game")

InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)


Window:SelectTab(1)

Fluent:Notify({
    Title = "Moon Hub",
    Content = "The script has been loaded.",
    Duration = 8
})

-- You can use the SaveManager:LoadAutoloadConfig() to load a config
-- which has been marked to be one that auto loads!
SaveManager:LoadAutoloadConfig()
end
