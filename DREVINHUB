local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Drevin hub", HidePremium = true, SaveConfig = true, IntroText = "Drevin Hub", ConfigFolder = "DREVINHUBConfig"})
OrionLib:MakeNotification({
	Name = "Welcome to drevin hub",
	Content = "ENJOY",
	Image = "rbxassetid://4483345998",
	Time = 5
})
local Main = Window:MakeTab({
	Name = "Main",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Main:AddSection({
	Name = "Main"
})
Main:AddButton({
	Name = "Fly (click x)",
	Callback = function()
      		local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()

localplayer = plr

if workspace:FindFirstChild("Core") then
workspace.Core:Destroy()
end

local Core = Instance.new("Part")
Core.Name = "Core"
Core.Size = Vector3.new(0.05, 0.05, 0.05)

spawn(function()
Core.Parent = workspace
local Weld = Instance.new("Weld", Core)
Weld.Part0 = Core
Weld.Part1 = localplayer.Character.LowerTorso
Weld.C0 = CFrame.new(0, 0, 0)
end)

workspace:WaitForChild("Core")

local torso = workspace.Core
flying = true
local speed=10
local keys={a=false,d=false,w=false,s=false}
local e1
local e2
local function start()
local pos = Instance.new("BodyPosition",torso)
local gyro = Instance.new("BodyGyro",torso)
pos.Name="EPIXPOS"
pos.maxForce = Vector3.new(math.huge, math.huge, math.huge)
pos.position = torso.Position
gyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
gyro.cframe = torso.CFrame
repeat
wait()
localplayer.Character.Humanoid.PlatformStand=true
local new=gyro.cframe - gyro.cframe.p + pos.position
if not keys.w and not keys.s and not keys.a and not keys.d then
speed=5
end
if keys.w then
new = new + workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.s then
new = new - workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.d then
new = new * CFrame.new(speed,0,0)
speed=speed+0
end
if keys.a then
new = new * CFrame.new(-speed,0,0)
speed=speed+0
end
if speed>10 then
speed=5
end
pos.position=new.p
if keys.w then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(-math.rad(speed*0),0,0)
elseif keys.s then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(math.rad(speed*0),0,0)
else
gyro.cframe = workspace.CurrentCamera.CoordinateFrame
end
until flying == false
if gyro then gyro:Destroy() end
if pos then pos:Destroy() end
flying=false
localplayer.Character.Humanoid.PlatformStand=false
speed=10
end
e1=mouse.KeyDown:connect(function(key)
if not torso or not torso.Parent then flying=false e1:disconnect() e2:disconnect() return end
if key=="w" then
keys.w=true
elseif key=="s" then
keys.s=true
elseif key=="a" then
keys.a=true
elseif key=="d" then
keys.d=true
elseif key=="x" then
if flying==true then
flying=false
else
flying=true
start()
end
end
end)
e2=mouse.KeyUp:connect(function(key)
if key=="w" then
keys.w=false
elseif key=="s" then
keys.s=false
elseif key=="a" then
keys.a=false
elseif key=="d" then
keys.d=false
end
end)
start()

  	end    
})
Main:AddButton({
	Name = "AntiStomp",
	Callback = function()
      		pcall(function()
if game.Players.LocalPlayer.Character.BodyEffects['K.O'].Value == true then

for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
    if v:IsA('MeshPart') or  v:IsA('Accessory') then
        v:Destroy()
    end
end
end
end)
  	end    
})
Main:AddButton({
	Name = "Cframe Gui",
	Callback = function()
      		local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("DREVIN HUB CFRAME", "DarkTheme")

local speed = Window:NewTab("Speed")
local rs = speed:NewSection("CFrame Speed")
rs:NewButton("CFrame Guns FIX", "ButtonInfo", function()
    for _, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
        if v:IsA("Script") and v.Name ~= "Health" and v.Name ~= "Sound" and v:FindFirstChild("LocalScript") then
            v:Destroy()
        end
    end
    game.Players.LocalPlayer.CharacterAdded:Connect(function(char)
        repeat
            wait()
        until game.Players.LocalPlayer.Character
        char.ChildAdded:Connect(function(child)
            if child:IsA("Script") then 
                wait(0.1)
                if child:FindFirstChild("LocalScript") then
                    child.LocalScript:FireServer()
                end
            end
        end)
    end)
end)
rs:NewButton("CFrame Speed (Z)", "ButtonInfo", function()
        repeat
        wait()
    until game:IsLoaded()
    local L_134_ = game:service('Players')
    local L_135_ = L_134_.LocalPlayer
    repeat
        wait()
    until L_135_.Character
    local L_136_ = game:service('UserInputService')
    local L_137_ = game:service('RunService')
    getgenv().Multiplier = 0.5
    local L_138_ = true
    local L_139_
    L_136_.InputBegan:connect(function(L_140_arg0)
        if L_140_arg0.KeyCode == Enum.KeyCode.LeftBracket then
            Multiplier = Multiplier + 0.01
            print(Multiplier)
            wait(0.2)
            while L_136_:IsKeyDown(Enum.KeyCode.LeftBracket) do
                wait()
                Multiplier = Multiplier + 0.01
                print(Multiplier)
            end
        end
        if L_140_arg0.KeyCode == Enum.KeyCode.RightBracket then
            Multiplier = Multiplier - 0.01
            print(Multiplier)
            wait(0.2)
            while L_136_:IsKeyDown(Enum.KeyCode.RightBracket) do
                wait()
                Multiplier = Multiplier - 0.01
                print(Multiplier)
            end
        end
        if L_140_arg0.KeyCode == Enum.KeyCode.Z then
            L_138_ = not L_138_
            if L_138_ == true then
                repeat
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.Humanoid.MoveDirection * Multiplier
                    game:GetService("RunService").Stepped:wait()
                until L_138_ == false
            end
        end
    end)
end)
rs:NewSlider("CFrame Speed ", "SliderInfo", 5, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    getgenv().Multiplier = s
end)
rs:NewKeybind("Toggle UI", "KeybindInfo", Enum.KeyCode.V, function()
    Library.ToggleUI()
end)
  	end    
})
Main:AddButton({
	Name = "AnimationPack!",
	Callback = function()
      		 local Folder = Instance.new('Folder', game:GetService("Workspace"))
	local AnimationPack = game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.AnimationPack
	local ScrollingFrame = AnimationPack.ScrollingFrame
	local CloseButton = AnimationPack.CloseButton

	AnimationPack.Visible = true

	local LeanAnimation = Instance.new("Animation", Folder)
	LeanAnimation.Name = "LeanAnimation"
	LeanAnimation.AnimationId = "rbxassetid://3152375249"
	local Lean = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(LeanAnimation)

	local LayAnimation = Instance.new("Animation", Folder)
	LayAnimation.Name = "LayAnimation"
	LayAnimation.AnimationId = "rbxassetid://3152378852"
	local Lay = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(LayAnimation)

	local Dance1Animation = Instance.new("Animation", Folder)
	Dance1Animation.Name = "Dance1Animation"
	Dance1Animation.AnimationId = "rbxassetid://3189773368"
	local Dance1 = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(Dance1Animation)

	local Dance2Animation = Instance.new("Animation", Folder)
	Dance2Animation.Name = "Dance2Animation"
	Dance2Animation.AnimationId = "rbxassetid://3189776546"
	local Dance2 = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(Dance2Animation)

	local GreetAnimation = Instance.new("Animation", Folder)
	GreetAnimation.Name = "GreetAnimation"
	GreetAnimation.AnimationId = "rbxassetid://3189777795"
	local Greet = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(GreetAnimation)

	local PrayingAnimation = Instance.new("Animation", Folder)
	PrayingAnimation.Name = "PrayingAnimation"
	PrayingAnimation.AnimationId = "rbxassetid://3487719500"
	local Praying = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(PrayingAnimation)

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Lean" then
				v.Name = "LeanButton"
			end
		end
	end

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Lay" then
				v.Name = "LayButton"
			end
		end
	end

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Dance1" then
				v.Name = "Dance1Button"
			end
		end
	end

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Dance2" then
				v.Name = "Dance2Button"
			end
		end
	end

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Greet" then
				v.Name = "GreetButton"
			end
		end
	end

	for i,v in pairs(ScrollingFrame:GetChildren()) do
		if v.Name == "TextButton" then
			if v.Text == "Praying" then
				v.Name = "PrayingButton"
			end
		end
	end

	function Stop()
		Lay:Stop()
		Lean:Stop()
		Dance1:Stop()
		Dance2:Stop()
		Greet:Stop()
		Praying:Stop()
	end

	local LeanTextButton = ScrollingFrame.LeanButton
	local LayTextButton = ScrollingFrame.LayButton
	local Dance1TextButton = ScrollingFrame.Dance1Button
	local Dance2TextButton = ScrollingFrame.Dance2Button
	local GreetTextButton = ScrollingFrame.GreetButton
	local PrayingTextButton = ScrollingFrame.PrayingButton

	AnimationPack.MouseButton1Click:Connect(function()
		if ScrollingFrame.Visible == false then
			ScrollingFrame.Visible = true
			CloseButton.Visible = true
		end
	end)
	CloseButton.MouseButton1Click:Connect(function()
		if ScrollingFrame.Visible == true then
			ScrollingFrame.Visible = false
			CloseButton.Visible = false
		end
	end)
	LeanTextButton.MouseButton1Click:Connect(function()
		Stop()
		Lean:Play()
	end)
	LayTextButton.MouseButton1Click:Connect(function()
		Stop()
		Lay:Play()
	end)
	Dance1TextButton.MouseButton1Click:Connect(function()
		Stop()
		Dance1:Play()
	end)
	Dance2TextButton.MouseButton1Click:Connect(function()
		Stop()
		Dance2:Play()
	end)
	GreetTextButton.MouseButton1Click:Connect(function()
		Stop()
		Greet:Play()
	end)
	PrayingTextButton.MouseButton1Click:Connect(function()
		Stop()
		Praying:Play()
	end)

	game:GetService("Players").LocalPlayer.Character.Humanoid.Running:Connect(function()
		Stop()
	end)
	game:GetService("Players").LocalPlayer.Character.Humanoid.Died:Connect(function()
		Stop()
		repeat
			wait()
		until game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 100
		wait(1)
		local AnimationPack = game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.AnimationPack
		local ScrollingFrame = AnimationPack.ScrollingFrame
		local CloseButton = AnimationPack.CloseButton

		AnimationPack.Visible = true

		local LeanAnimation = Instance.new("Animation", Folder)
		LeanAnimation.Name = "LeanAnimation"
		LeanAnimation.AnimationId = "rbxassetid://3152375249"
		local Lean = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(LeanAnimation)

		local LayAnimation = Instance.new("Animation", Folder)
		LayAnimation.Name = "LayAnimation"
		LayAnimation.AnimationId = "rbxassetid://3152378852"
		local Lay = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(LayAnimation)

		local Dance1Animation = Instance.new("Animation", Folder)
		Dance1Animation.Name = "Dance1Animation"
		Dance1Animation.AnimationId = "rbxassetid://3189773368"
		local Dance1 = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(Dance1Animation)

		local Dance2Animation = Instance.new("Animation", Folder)
		Dance2Animation.Name = "Dance2Animation"
		Dance2Animation.AnimationId = "rbxassetid://3189776546"
		local Dance2 = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(Dance2Animation)

		local GreetAnimation = Instance.new("Animation", Folder)
		GreetAnimation.Name = "GreetAnimation"
		GreetAnimation.AnimationId = "rbxassetid://3189777795"
		local Greet = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(GreetAnimation)

		local PrayingAnimation = Instance.new("Animation", Folder)
		PrayingAnimation.Name = "PrayingAnimation"
		PrayingAnimation.AnimationId = "rbxassetid://3487719500"
		local Praying = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(PrayingAnimation)

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Lean" then
					v.Name = "LeanButton"
				end
			end
		end

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Lay" then
					v.Name = "LayButton"
				end
			end
		end

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Dance1" then
					v.Name = "Dance1Button"
				end
			end
		end

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Dance2" then
					v.Name = "Dance2Button"
				end
			end
		end

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Greet" then
					v.Name = "GreetButton"
				end
			end
		end

		for i,v in pairs(ScrollingFrame:GetChildren()) do
			if v.Name == "TextButton" then
				if v.Text == "Praying" then
					v.Name = "PrayingButton"
				end
			end
		end

		function Stop()
			Lay:Stop()
			Lean:Stop()
			Dance1:Stop()
			Dance2:Stop()
			Greet:Stop()
			Praying:Stop()
		end

		local LeanTextButton = ScrollingFrame.LeanButton
		local LayTextButton = ScrollingFrame.LayButton
		local Dance1TextButton = ScrollingFrame.Dance1Button
		local Dance2TextButton = ScrollingFrame.Dance2Button
		local GreetTextButton = ScrollingFrame.GreetButton
		local PrayingTextButton = ScrollingFrame.PrayingButton

		AnimationPack.MouseButton1Click:Connect(function()
			if ScrollingFrame.Visible == false then
				ScrollingFrame.Visible = true
				CloseButton.Visible = true
			end
		end)
		CloseButton.MouseButton1Click:Connect(function()
			if ScrollingFrame.Visible == true then
				ScrollingFrame.Visible = false
				CloseButton.Visible = false
			end
		end)
		LeanTextButton.MouseButton1Click:Connect(function()
			Stop()
			Lean:Play()
		end)
		LayTextButton.MouseButton1Click:Connect(function()
			Stop()
			Lay:Play()
		end)
		Dance1TextButton.MouseButton1Click:Connect(function()
			Stop()
			Dance1:Play()
		end)
		Dance2TextButton.MouseButton1Click:Connect(function()
			Stop()
			Dance2:Play()
		end)
		GreetTextButton.MouseButton1Click:Connect(function()
			Stop()
			Greet:Play()
		end)
		PrayingTextButton.MouseButton1Click:Connect(function()
			Stop()
			Praying:Play()
		end)
	end)
  	end    
})
Main:AddButton({
	Name = "AutoStompBot - auto stomps everyone in the server by tping to them",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/grandpascripts/error502/main/StompBot.lua"))()
  	end    
})
local Section = Main:AddSection({
	Name = "Animations"
})
Main:AddButton({
	Name = "Pro Animations",
	Callback = function()
      		  while true do
    wait(1)
    for i, player in ipairs(game.Players:GetChildren()) do
    local Animate = game.Players.LocalPlayer.Character.Animate
Animate.idle.Animation1.AnimationId = "http://www.roblox.com/asset/?id=782841498"
Animate.idle.Animation2.AnimationId = "http://www.roblox.com/asset/?id=782841498"
Animate.walk.WalkAnim.AnimationId = "http://www.roblox.com/asset/?id=616168032"
Animate.run.RunAnim.AnimationId = "http://www.roblox.com/asset/?id=616163682"
Animate.jump.JumpAnim.AnimationId = "http://www.roblox.com/asset/?id=1083218792"
Animate.climb.ClimbAnim.AnimationId = "http://www.roblox.com/asset/?id=1083439238"
Animate.fall.FallAnim.AnimationId = "http://www.roblox.com/asset/?id=707829716"
game.Players.LocalPlayer.Character.Humanoid.Jump = false
    end
end
  	end    
})
local Other = Window:MakeTab({
	Name = "Other",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Other:AddSection({
	Name = "Locks + chatspy"
})
Other:AddButton({
	Name = "Green Dot (q)",
	Callback = function()
      		    _G.KEY = "q"
		_G.PART = "HumanoidRootPart"
		_G.PRED = 0.048
		_G.Frame = Vector3.new(0, 0.53, 0)
		local L_76_ = game:GetService "Workspace".CurrentCamera
		local L_77_
		local L_78_ = false
		local L_79_ = nil
		local L_80_ = game.Players.LocalPlayer:GetMouse()
		local L_81_ = Instance.new("Part", game.Workspace)
		local L_82_ = Instance.new("Folder", game.CoreGui)
		function makemarker(L_86_arg0, L_87_arg1, L_88_arg2, L_89_arg3, L_90_arg4)
			local L_91_ = Instance.new("BillboardGui", L_86_arg0)
			L_91_.Name = "PP"
			L_91_.Adornee = L_87_arg1
			L_91_.Size = UDim2.new(L_89_arg3, L_90_arg4, L_89_arg3, L_90_arg4)
			L_91_.AlwaysOnTop = true
			local L_92_ = Instance.new("Frame", L_91_)
			L_92_.Size = UDim2.new(4, 0, 4, 0)
			L_92_.BackgroundTransparency = 0.1
			L_92_.BackgroundColor3 = L_88_arg2
			local L_93_ = Instance.new("UICorner", L_92_)
			L_93_.CornerRadius = UDim.new(50, 50)
			return L_91_
		end
		local L_83_ = game.Players:GetPlayers()
		function noob(L_94_arg0)
			local L_95_
			repeat
				wait()
			until L_94_arg0.Character
			local L_96_ = makemarker(L_82_, L_94_arg0.Character:WaitForChild(_G.PART), Color3.fromRGB(255, 255, 255), 0.0, 0)
			L_96_.Name = L_94_arg0.Name
			L_94_arg0.CharacterAdded:connect(
				function(L_98_arg0)
					L_96_.Adornee = L_98_arg0:WaitForChild(_G.PART)
				end
			)
			local L_97_ = Instance.new("TextLabel", L_96_)
			L_97_.BackgroundTransparency = 1
			L_97_.Position = UDim2.new(0, 0, 0, -50)
			L_97_.Size = UDim2.new(0, 100, 0, 100)
			L_97_.Font = Enum.Font.SourceSansSemibold
			L_97_.TextSize = 14
			L_97_.TextColor3 = Color3.new(1, 1, 1)
			L_97_.TextStrokeTransparency = 0
			L_97_.TextYAlignment = Enum.TextYAlignment.Bottom
			L_97_.Text = "Bling" .. L_94_arg0.Name
			L_97_.ZIndex = 10
			spawn(
				function()
					while wait() do
						if L_94_arg0.Character then
						end
					end
				end
			)
		end
		for L_99_forvar0 = 1, #L_83_ do
			if L_83_[L_99_forvar0] ~= game.Players.LocalPlayer then
				noob(L_83_[L_99_forvar0])
			end
		end
		game.Players.PlayerAdded:connect(
			function(L_100_arg0)
				noob(L_100_arg0)
			end
		)
		game.Players.PlayerRemoving:Connect(
			function(L_101_arg0)
				L_82_[L_101_arg0.Name]:Destroy()
			end
		)
		spawn(
			function()
				L_81_.Anchored = true
				L_81_.CanCollide = false
				L_81_.Size = Vector3.new(0.1, 0.1, 0.1)
				L_81_.Transparency = 0.1
				makemarker(L_81_, L_81_, Color3.fromRGB(0, 180, 0), 0.20, 0)
			end
		)
		L_80_.KeyDown:Connect(
			function(L_102_arg0)
				if L_102_arg0 ~= _G.KEY then
					return
				end
				if L_78_ then
					L_78_ = false
					TextLabel.TextColor3 = Color3.fromRGB(255, 20, 75)
					TextLabel.Text = "------"
				else
					L_78_ = true
					L_77_ = getClosestPlayerToCursor()
					TextLabel.TextColor3 = Color3.fromRGB(12, 255, 0)
					TextLabel.Text = L_77_.Character.Humanoid.DisplayName
				end
			end
		)
		function getClosestPlayerToCursor()
			local L_103_
			local L_104_ = math.huge
			for L_105_forvar0, L_106_forvar1 in pairs(game.Players:GetPlayers()) do
				if
					L_106_forvar1 ~= game.Players.LocalPlayer and L_106_forvar1.Character and L_106_forvar1.Character:FindFirstChild("Humanoid") and
					L_106_forvar1.Character.Humanoid.Health ~= 0 and
					L_106_forvar1.Character:FindFirstChild(_G.PART)
				then
					local L_107_ = L_76_:WorldToViewportPoint(L_106_forvar1.Character.PrimaryPart.Position)
					local L_108_ = (Vector2.new(L_107_.X, L_107_.Y) - Vector2.new(L_80_.X, L_80_.Y)).magnitude
					if L_108_ < L_104_ then
						L_103_ = L_106_forvar1
						L_104_ = L_108_
					end
				end
			end
			return L_103_
		end
		game:GetService "RunService".Stepped:connect(
			function()
				if L_78_ and L_77_.Character and L_77_.Character:FindFirstChild(_G.PART) then
					L_81_.CFrame =
						CFrame.new(L_77_.Character[_G.PART].Position + _G.Frame + L_77_.Character[_G.PART].Velocity * L_79_)
				else
					L_81_.CFrame = CFrame.new(0, 9999, 0)
				end
			end
		)
		local L_84_ = getrawmetatable(game)
		local L_85_ = L_84_.__namecall
		setreadonly(L_84_, false)
		L_84_.__namecall =
			newcclosure(
				function(...)
				local L_109_ = {
					...
				}
				if L_78_ and getnamecallmethod() == "FireServer" and L_109_[2] == "UpdateMousePos" then
					L_109_[3] = L_77_.Character[_G.PART].Position + _G.Frame + L_77_.Character[_G.PART].Velocity * L_79_
					return L_85_(unpack(L_109_))
				end
				return L_85_(...)
			end
			)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_110_arg0)
				if L_110_arg0 == "/e print" then
					print(_G.PRED)
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_111_arg0)
				if L_111_arg0 == "Code:1029" then
					_G.KEY = nil
					_G.AIR = nil
					_G.PART = nil
					_G.PRED = nil
					TextLabel.Visible = false
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_112_arg0)
				if L_112_arg0 == "/e hrp" then
					_G.KEY = "q"
					_G.AIR = 0.00005
					_G.PART = "HumanoidRootPart"
					_G.PRED = 0.032
					TextLabel.Visible = true
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_113_arg0)
				if L_113_arg0 == "/e lt" then
					_G.KEY = "q"
					_G.AIR = 0.00005
					_G.PART = "LowerTorso"
					_G.PRED = 0.032
					TextLabel.Visible = true
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_114_arg0)
				if L_114_arg0 == "Screensharing" then
					_G.KEY = "q"
					_G.AIR = 0.00005
					_G.PART = "LowerTorso"
					_G.PRED = 0.033
					TextLabel.Visible = true
					L_81_ = nil
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_115_arg0)
				if L_115_arg0 == "/e P+" then
					_G.PRED = _G.PRED + 0.001
				end
			end
		)
		game.Players.LocalPlayer.Chatted:Connect(
			function(L_116_arg0)
				if L_116_arg0 == "/e P-" then
					_G.PRED = _G.PRED - 0.001
				end
			end
		)
		while wait() do
			if
				getClosestPlayerToCursor().Character.Humanoid.Jump == true and
				getClosestPlayerToCursor().Character.Humanoid.FloorMaterial == Enum.Material.Air
			then
				_G.Frame = Vector3.new(0, -2.3, 0)
				wait(0.05)
			else
				local L_117_ = game:GetService("Stats").Network.ServerStatsItem["Data Ping"]:GetValueString()
				local L_118_ = tostring(L_117_)
				local L_119_ = L_118_:split(" ")
				local L_120_ = L_119_[1]
				L_79_ = L_120_ / 1000 + _G.PRED
				_G.Frame = Vector3.new(0, 0.53, 0)
			end
		end
  	end    
})
Other:AddButton({
	Name = "Streamable Silent",
	Callback = function()
      		 loadstring(game:HttpGet("https://raw.githubusercontent.com/tayodevelup/imsoniac/main/silentaim", true))()
  	end    
})
Other:AddButton({
	Name = "MONKE LOCK Q",
	Callback = function()
      		getgenv().Key = Enum.KeyCode.Q
getgenv().Prediction = 0.1307
    getgenv().AirshotFunccc = false
    getgenv().Tracer = true
    getgenv().Partz = "LowerTorso" -- LowerTorso, HumanoidRootPart,Head,UpperTorso

    
        local CC = game:GetService"Workspace".CurrentCamera
    local LocalMouse = game.Players.LocalPlayer:GetMouse()
        local Locking = false
        local cc = game:GetService("Workspace").CurrentCamera
        local gs = game:GetService("GuiService")
        local ggi = gs.GetGuiInset
        local lp = game:GetService("Players").LocalPlayer
        local mouse = lp:GetMouse()



local Tracer = Drawing.new("Image")


Tracer.Data = game:HttpGet("https://media.newyorker.com/photos/59095bb86552fa0be682d9d0/master/pass/Monkey-Selfie.jpg")
Tracer.ZIndex = 99999
Tracer.Size = Vector2.new(110,110)


    function x(tt,tx,cc)
    game.StarterGui:SetCore("SendNotification", {
        Title = tt;
        Text = tx;
        Duration = cc;
    })
end

x("Monke lock by 3qxt9919", "Loaded", 3)


    if getgenv().flashyes == true then
                       x("Monke lock by 3qxt9919", "Already Loaded", 5)
        return
    end
    getgenv().flashyes = true
    
        local UserInputService = game:GetService("UserInputService")

    UserInputService.InputBegan:Connect(function(keygo,ok)
           if (not ok) then
           if (keygo.KeyCode == getgenv().Key) then
               Locking = not Locking
               if Locking then
               Plr =  getClosestPlayerToCursor()
                x("Monke lock by 3qxt9919", ""..Plr.Character.Humanoid.DisplayName, 3)
elseif not Locking then
    if Plr then Plr = nil
                       x("Monke lock by 3qxt9919", "Unlocked", 3)
     
         
end
end
end
end
end)
    function getClosestPlayerToCursor()
        local closestPlayer
        local shortestDistance = 137

        for i, v in pairs(game.Players:GetPlayers()) do
            if v ~= game.Players.LocalPlayer and v.Character and v.Character:FindFirstChild("Humanoid") and v.Character.Humanoid.Health ~= 0 and v.Character:FindFirstChild("LowerTorso") then
                local pos = CC:WorldToViewportPoint(v.Character.PrimaryPart.Position)
                local magnitude = (Vector2.new(pos.X, pos.Y) - Vector2.new(LocalMouse.X, LocalMouse.Y)).magnitude
                if magnitude < shortestDistance then
                    closestPlayer = v
                    shortestDistance = magnitude
                end
            end
        end
        return closestPlayer
    end



    
    

    local rawmetatable = getrawmetatable(game)
    local old = rawmetatable.__namecall
    setreadonly(rawmetatable, false)
    rawmetatable.__namecall = newcclosure(function(...)
        local args = {...}
        if Plr ~= nil  and getnamecallmethod() == "FireServer" and args[2] == "UpdateMousePos" then
            args[3] = Plr.Character[getgenv().Partz].Position+(Plr.Character[getgenv().Partz].Velocity*Prediction)
            return old(unpack(args))
        end
        return old(...)
    end)


game:GetService("RunService").RenderStepped:connect(function()    
if getgenv().AirshotFunccc == true then

            if Plr ~= nil and Plr.Character.Humanoid.Jump == true and Plr.Character.Humanoid.FloorMaterial == Enum.Material.Air then
                getgenv().Partz = "RightFoot"
            else
                Plr.Character:WaitForChild("Humanoid").StateChanged:Connect(function(old,new)
                    if new == Enum.HumanoidStateType.Freefall then
                    getgenv().Partz = "RightFoot"
                    else
                        getgenv().Partz = "LowerTorso"
                    end
                end)
            end
        end 


        if getgenv().Tracer == true and Locking then
            local Vector, OnScreen = cc:worldToViewportPoint(Plr.Character[getgenv().Partz].Position)
            Tracer.Visible = true
   Tracer.Position = Vector2.new(Vector.X, Vector.Y)
     else
            Tracer.Visible = false
        end
    

    end)
  	end    
})
Other:AddButton({
	Name = "Hood modded And Da hood q lock",
	Callback = function()
      		 loadstring(game:HttpGet('https://raw.githubusercontent.com/vKoku/kaz/main/dh'))()
  	end    
})
Other:AddButton({
	Name = "Chatspy",
	Callback = function()
      		 --SCRIPT NOT MADE BY ME I JUST NEEDED A LOADSTRING FOR IT
--\\ lol i was so humble 

--chat "/spy" to toggle!
enabled = true
--if true will check your messages too
spyOnMyself = true
--if true will chat the logs publicly (fun, risky)
public = false
--if true will use /me to stand out
publicItalics = true
--customize private logs
privateProperties = {
	Color = Color3.fromRGB(0,255,255); 
	Font = Enum.Font.SourceSansBold;
	TextSize = 18;
}
--////////////////////////////////////////////////////////////////
local StarterGui = game:GetService("StarterGui")
local Players = game:GetService("Players")
local player = Players.LocalPlayer or Players:GetPropertyChangedSignal("LocalPlayer"):Wait() or Players.LocalPlayer
local saymsg = game:GetService("ReplicatedStorage"):WaitForChild("DefaultChatSystemChatEvents"):WaitForChild("SayMessageRequest")
local getmsg = game:GetService("ReplicatedStorage"):WaitForChild("DefaultChatSystemChatEvents"):WaitForChild("OnMessageDoneFiltering")
local instance = (_G.chatSpyInstance or 0) + 1
_G.chatSpyInstance = instance

local function onChatted(p,msg)
	if _G.chatSpyInstance == instance then
		if p==player and msg:lower():sub(1,4)=="/spy" then
			enabled = not enabled
			wait(0.3)
			privateProperties.Text = "{SPY "..(enabled and "EN" or "DIS").."ABLED}"
			StarterGui:SetCore("ChatMakeSystemMessage",privateProperties)
		elseif enabled and (spyOnMyself==true or p~=player) then
			msg = msg:gsub("[\n\r]",''):gsub("\t",' '):gsub("[ ]+",' ')
			local hidden = true
			local conn = getmsg.OnClientEvent:Connect(function(packet,channel)
				if packet.SpeakerUserId==p.UserId and packet.Message==msg:sub(#msg-#packet.Message+1) and (channel=="All" or (channel=="Team" and public==false and Players[packet.FromSpeaker].Team==player.Team)) then
					hidden = false
				end
			end)
			wait(1)
			conn:Disconnect()
			if hidden and enabled then
				if public then
					saymsg:FireServer((publicItalics and "/me " or '').."{SPY} [".. p.Name .."]: "..msg,"All")
				else
					privateProperties.Text = "{SPY} [".. p.Name .."]: "..msg
					StarterGui:SetCore("ChatMakeSystemMessage",privateProperties)
				end
			end
		end
	end
end

for _,p in ipairs(Players:GetPlayers()) do
	p.Chatted:Connect(function(msg) onChatted(p,msg) end)
end
Players.PlayerAdded:Connect(function(p)
	p.Chatted:Connect(function(msg) onChatted(p,msg) end)
end)

privateProperties.Text = "{SPY "..(enabled and "EN" or "DIS").."ABLED}"
StarterGui:SetCore("ChatMakeSystemMessage",privateProperties)
if not player.PlayerGui:FindFirstChild("Chat") then wait(3) end
local chatFrame = player.PlayerGui.Chat.Frame
chatFrame.ChatChannelParentFrame.Visible = true
chatFrame.ChatBarParentFrame.Position = chatFrame.ChatChannelParentFrame.Position+UDim2.new(UDim.new(),chatFrame.ChatChannelParentFrame.Size.Y)
--loadstring(game:HttpGet('https://pastebin.com/raw/XkcN6cYQ'))()

  	end    
})
local Teleports = Window:MakeTab({
	Name = "Teleports",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Teleports:AddSection({
	Name = "Teleports"
})
Teleports:AddButton({
	Name = "Uphillz",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(480, 48, -622)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Taco",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(564, 51, -480)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Uphillz food store",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(301, 49, -621)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Gym",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-73, 22, -622)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location

  	end    
})
Teleports:AddButton({
	Name = "Hood Kicks",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-205, 21, -415)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location

  	end    
})
Teleports:AddButton({
	Name = "bank",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-373, 21, -294)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Police Station",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-248, 21, -116)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location

  	end    
})
Teleports:AddButton({
	Name = "Downhill",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-581, 8, -737)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location

  	end    
})
Teleports:AddButton({
	Name = "Db",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-1042, 21, -268)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Rev",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-641, 21, -128)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location

  	end    
})
Teleports:AddButton({
	Name = "Casino",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-997, 21, -165)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Grave",
	Callback = function()
      		local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(168, 21, -7)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})
Teleports:AddButton({
	Name = "Admin",
	Callback = function()
	local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-801, -39, -885)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
wait(0.1)
pl.CFrame = location
  	end    
})

local Credits = Window:MakeTab({
	Name = "Credits",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Credits = Credits:AddSection({
	Name = "Credits"
})
Credits:AddButton({
	Name = "Me 3qxt#9919 Dm for issues",
	Callback = function()
      		print("3qxt#9919")
  	end    
})
Credits:AddButton({
	Name = "Draco For Some Scripts Discord account banned rn!",
	Callback = function()
      		print("Banned :/")
  	end    
})
Credits:AddButton({
	Name = "Discord server: https://discord.gg/aUFVRbPw",
	Callback = function()
      		print("https://discord.gg/aUFVRbPw")
  	end    
})




OrionLib:Init()
