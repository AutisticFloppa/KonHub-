--Kon Hub

--Created by KON's 

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Close = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local ImageButton = Instance.new("ImageButton")
local HUB = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextLabel_2 = Instance.new("TextLabel")
local ScrollingFrame = Instance.new("ScrollingFrame")
local NoClip = Instance.new("TextButton")
local Fly = Instance.new("TextButton")
local God = Instance.new("TextButton")
local Aimbot = Instance.new("TextButton")
local InfJump = Instance.new("TextButton")
local InfYeld = Instance.new("TextButton")
local ESP = Instance.new("TextButton")
local Suicide = Instance.new("TextButton")
local solar = Instance.new("TextButton")
local ctrltp = Instance.new("TextButton")
local jerkr15 = Instance.new("TextButton")
local jerkr6 = Instance.new("TextButton")
local Open = Instance.new("TextButton")

--Properties:
game:GetService("StarterGui"):SetCore("SendNotification",{
	Title = "KON Hub", -- Required
	Text = "KON Hub has loaded sucsessfuly!", -- Required
	Icon = "rbxassetid://117043165552834" -- Optional
})

wait(3)

local button = jerkr15
local RunService = game:GetService("RunService")

local hue = 0

RunService.RenderStepped:Connect(function(dt)
	hue = (hue + dt * 0.6) % 1 -- Adjust speed by changing 0.2
	button.BackgroundColor3 = Color3.fromHSV(hue, 1, 1)
end)

local button = jerkr6
local RunService = game:GetService("RunService")

local hue = 0

RunService.RenderStepped:Connect(function(dt)
	hue = (hue + dt * 0.6) % 1 -- Adjust speed by changing 0.2
	button.BackgroundColor3 = Color3.fromHSV(hue, 1, 1)
end)



ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ResetOnSpawn = false
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(1, 187, 255)
Frame.BackgroundTransparency = 0.550
Frame.BorderColor3 = Color3.fromRGB(27, 42, 53)
Frame.Position = UDim2.new(0.396259546, 0, 0.355973423, 0)
Frame.Size = UDim2.new(0, 282, 0, 221)
Frame.Visible = false
Frame.Active = true

local UserInputService = game:GetService('UserInputService')

local frame = Frame

local leadFrame = Instance.new('Frame') do
	leadFrame.AnchorPoint = frame.AnchorPoint
	leadFrame.Position = frame.Position
	leadFrame.Size = frame.Size
	leadFrame.Name = `Lead {frame.Name}`
	leadFrame.Visible = false
	leadFrame.Parent = frame.Parent
end

local screenGui = frame:FindFirstAncestorOfClass('ScreenGui')

local inputChanged = nil
local inputEnded = nil

local function getBoundsRelations(guiObject : GuiObject)
	local bounds = screenGui.AbsoluteSize
	local topLeft = screenGui.IgnoreGuiInset and guiObject.AbsolutePosition + Vector2.new(0, 36) or guiObject.AbsolutePosition
	local bottomRight = topLeft + guiObject.AbsoluteSize

	local boundRelations = {
		Top = topLeft.Y < 0 and math.abs(topLeft.Y) or nil,
		Left = topLeft.X < 0 and math.abs(topLeft.X) or nil,
		Right = bottomRight.X > bounds.X and math.abs(bottomRight.X - bounds.X) or nil,
		Bottom = bottomRight.Y > bounds.Y and math.abs(bottomRight.Y - bounds.Y) or nil,
	}

	return (not boundRelations.Top
		and not boundRelations.Bottom
		and not boundRelations.Left
		and not boundRelations.Right), boundRelations
end

frame.InputBegan:Connect(function(inputObject : InputObject)
	if inputObject.UserInputType == Enum.UserInputType.MouseButton1 then

		local lastMousePosition = UserInputService:GetMouseLocation()
		local goalPosition = frame.Position

		inputChanged = UserInputService.InputChanged:Connect(function(input : InputObject, event : boolean)
			if input.UserInputType == Enum.UserInputType.MouseMovement then
				local currentMousePosition = UserInputService:GetMouseLocation()
				local mouseDelta = currentMousePosition - lastMousePosition

				goalPosition += UDim2.fromOffset(mouseDelta.X, mouseDelta.Y)

				leadFrame.Position = goalPosition

				local isInBounds, relations = getBoundsRelations(leadFrame)

				if not isInBounds then
					local x = (relations.Left or 0) - (relations.Right or 0)
					local y = (relations.Top or 0) - (relations.Bottom or 0)

					goalPosition += UDim2.fromOffset(x, y)
				end

				frame.Position = goalPosition
				lastMousePosition = currentMousePosition
			end
		end)

		inputEnded = frame.InputEnded:Connect(function(input : InputObject)
			if input.UserInputType == Enum.UserInputType.MouseButton1 then
				inputChanged:Disconnect()
				inputChanged = nil

				inputEnded:Disconnect()
				inputEnded = nil
			end
		end)
	end
end)

frame.Destroying:Once(function()

	leadFrame = leadFrame:Destroy()

	if inputChanged  then
		inputChanged:Disconnect()
		inputChanged = nil
	end

	if inputEnded then
		inputEnded:Disconnect()
		inputEnded = nil
	end
end)

Close.Name = "Close"
Close.Parent = Frame
Close.BackgroundColor3 = Color3.fromRGB(176, 0, 6)
Close.BorderColor3 = Color3.fromRGB(27, 42, 53)
Close.Position = UDim2.new(0.918439746, 0, 0, 0)
Close.Size = UDim2.new(0, 23, 0, 23)
Close.Font = Enum.Font.SourceSans
Close.Text = "X"
Close.TextColor3 = Color3.fromRGB(255, 255, 255)
Close.TextScaled = true
Close.TextSize = 14.000
Close.TextWrapped = true

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(205, 56, 255)
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.Size = UDim2.new(0, 259, 0, 23)
TextLabel.Font = Enum.Font.Cartoon
TextLabel.Text = "KON    "
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 23.000
TextLabel.TextWrapped = true

ImageButton.Parent = Frame
ImageButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageButton.BackgroundTransparency = 1.000
ImageButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
ImageButton.BorderSizePixel = 0
ImageButton.Position = UDim2.new(-0.0460992903, 0, -0.085972853, 0)
ImageButton.Size = UDim2.new(0, 42, 0, 42)
ImageButton.Image = "rbxassetid://117043165552834"

HUB.Name = "HUB"
HUB.Parent = Frame
HUB.BackgroundColor3 = Color3.fromRGB(255, 143, 7)
HUB.BorderColor3 = Color3.fromRGB(0, 0, 0)
HUB.BorderSizePixel = 0
HUB.Position = UDim2.new(0.5, 0, 0.00452488707, 0)
HUB.Size = UDim2.new(0, 37, 0, 22)

UICorner.Parent = HUB

TextLabel_2.Parent = HUB
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(-0.297297299, 0, -0.0499961153, 0)
TextLabel_2.Size = UDim2.new(0, 59, 0, 23)
TextLabel_2.Font = Enum.Font.Cartoon
TextLabel_2.Text = "Hub"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 19.000
TextLabel_2.TextWrapped = true

ScrollingFrame.Parent = Frame
ScrollingFrame.Active = true
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ScrollingFrame.BackgroundTransparency = 1.000
ScrollingFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
ScrollingFrame.Position = UDim2.new(0, 0, 0.104072399, 0)
ScrollingFrame.Size = UDim2.new(0, 282, 0, 197)
ScrollingFrame.ScrollBarThickness = 9

NoClip.Name = "NoClip"
NoClip.Parent = ScrollingFrame
NoClip.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
NoClip.BorderColor3 = Color3.fromRGB(0, 0, 0)
NoClip.Position = UDim2.new(0.060283687, 0, 0.0785925239, 0)
NoClip.Size = UDim2.new(0, 113, 0, 51)
NoClip.Font = Enum.Font.Cartoon
NoClip.Text = "Noclip"
NoClip.TextColor3 = Color3.fromRGB(135, 243, 255)
NoClip.TextSize = 29.000
NoClip.TextWrapped = true
NoClip.MouseButton1Down:connect(function()
	--[[
A distribution of https://wearedevs.net/scripts

Made by WeAreDevs
Created June 26, 2025

Description: Walk through walls, by disabling collision with anything your torso touches
]]

	local Players = game:GetService("Players")
	local LocalPlayer = Players.LocalPlayer

	local function onTouched(part)
		if not part:IsA("BasePart") then return end
		if not part.Anchored then return end
		if not part.CanCollide then return end

		local character = LocalPlayer.Character
		if not character then return end

		local hrp = character:FindFirstChild("HumanoidRootPart")
		if not hrp then return end

		-- Prevent disabling floors
		if part.Position.Y < (hrp.Position.Y - hrp.Size.Y) then return end

		-- Passed all checks
		part.CanCollide = false
	end

	-- Wait for character and hook HRP
	local function setup()
		local char = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
		local hrp = char:WaitForChild("HumanoidRootPart")

		hrp.Touched:Connect(onTouched)
	end

	if LocalPlayer.Character then
		setup()
	end

	LocalPlayer.CharacterAdded:Connect(setup)
end)


Fly.Name = "Fly"
Fly.Parent = ScrollingFrame
Fly.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
Fly.BorderColor3 = Color3.fromRGB(0, 0, 0)
Fly.Position = UDim2.new(0.5, 0, 0.077348426, 0)
Fly.Size = UDim2.new(0, 109, 0, 51)
Fly.Font = Enum.Font.Cartoon
Fly.Text = "Fly"
Fly.TextColor3 = Color3.fromRGB(255, 64, 245)
Fly.TextSize = 29.000
Fly.MouseButton1Down:connect(function()
	----------------------------------------------------
	---  A redistribution of https://wearedevs.net/  ---
	----------------------------------------------------

	--Waits until the player is in game
	repeat wait()
	until game.Players.LocalPlayer and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:findFirstChild("Torso") and game.Players.LocalPlayer.Character:findFirstChild("Humanoid")
	local mouse = game.Players.LocalPlayer:GetMouse()

	--Waits until the player's mouse is found
	repeat wait() until mouse

	--Variables
	local plr = game.Players.LocalPlayer
	local torso = plr.Character.Torso
	local flying = true
	local deb = true
	local ctrl = {f = 0, b = 0, l = 0, r = 0}
	local lastctrl = {f = 0, b = 0, l = 0, r = 0}
	local maxspeed = 50
	local speed = 0
	local bg = nil
	local bv = nil

	--Actual flying
	function Fly()
		game.StarterGui:SetCore("SendNotification", {Title="Fly Activated"; Text="WeAreDevs.net"; Duration=1;})
		bg = Instance.new("BodyGyro", torso)
		bg.P = 9e4
		bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		bg.cframe = torso.CFrame
		bv = Instance.new("BodyVelocity", torso)
		bv.velocity = Vector3.new(0,0.1,0)
		bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
		repeat wait()
			plr.Character.Humanoid.PlatformStand = true
			if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then
				speed = speed+.5+(speed/maxspeed)
				if speed > maxspeed then
					speed = maxspeed
				end
			elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then
				speed = speed-1
				if speed < 0 then
					speed = 0
				end
			end
			if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then
				bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed
				lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
			elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then
				bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed
			else
				bv.velocity = Vector3.new(0,0.1,0)
			end
			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0)
		until not flying
		ctrl = {f = 0, b = 0, l = 0, r = 0}
		lastctrl = {f = 0, b = 0, l = 0, r = 0}
		speed = 0
		bg:Destroy()
		bg = nil
		bv:Destroy()
		bv = nil
		plr.Character.Humanoid.PlatformStand = false
		game.StarterGui:SetCore("SendNotification", {Title="Fly Deactivated"; Text="WeAreDevs.net"; Duration=1;})
	end

	--Controls
	mouse.KeyDown:connect(function(key)
		if key:lower() == "e" then
			if flying then 
				flying = false
			else
				flying = true
				Fly()
			end
		elseif key:lower() == "w" then
			ctrl.f = 1
		elseif key:lower() == "s" then
			ctrl.b = -1
		elseif key:lower() == "a" then
			ctrl.l = -1
		elseif key:lower() == "d" then
			ctrl.r = 1
		end
	end)

	mouse.KeyUp:connect(function(key)
		if key:lower() == "w" then
			ctrl.f = 0
		elseif key:lower() == "s" then
			ctrl.b = 0
		elseif key:lower() == "a" then
			ctrl.l = 0
		elseif key:lower() == "d" then
			ctrl.r = 0
		end
	end)

	Fly()
end)


God.Name = "God"
God.Parent = ScrollingFrame
God.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
God.BorderColor3 = Color3.fromRGB(0, 0, 0)
God.Position = UDim2.new(0.5, 0, 0.219228372, 0)
God.Size = UDim2.new(0, 109, 0, 51)
God.Font = Enum.Font.Cartoon
God.Text = "God"
God.TextColor3 = Color3.fromRGB(135, 243, 255)
God.TextSize = 29.000
God.MouseButton1Down:connect(function()
	local LocalPlayer = game:GetService("Players").LocalPlayer

	local function Invincibility()
		if LocalPlayer.Character then
			for i, v in pairs(LocalPlayer.Character:GetChildren()) do
				if v.Name == "hitbox" then
					v:Destroy()
				end
			end
		end
	end

	while wait(0.5) do
		Invincibility(LocalPlayer)
	end
end)


Aimbot.Name = "Aimbot"
Aimbot.Parent = ScrollingFrame
Aimbot.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
Aimbot.BorderColor3 = Color3.fromRGB(0, 0, 0)
Aimbot.Position = UDim2.new(0.060283687, 0, 0.222019717, 0)
Aimbot.Size = UDim2.new(0, 113, 0, 51)
Aimbot.Font = Enum.Font.Cartoon
Aimbot.Text = "Aimbot"
Aimbot.TextColor3 = Color3.fromRGB(255, 64, 245)
Aimbot.TextSize = 29.000
Aimbot.TextWrapped = true
Aimbot.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/Universal%20ESP%20and%20Aimbot.lua"))()
end)

InfJump.Name = "InfJump"
InfJump.Parent = ScrollingFrame
InfJump.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
InfJump.BorderColor3 = Color3.fromRGB(0, 0, 0)
InfJump.Position = UDim2.new(0.5, 0, 0.366436481, 0)
InfJump.Size = UDim2.new(0, 109, 0, 51)
InfJump.Font = Enum.Font.Cartoon
InfJump.Text = "InfJump"
InfJump.TextColor3 = Color3.fromRGB(255, 64, 245)
InfJump.TextSize = 29.000
InfJump.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/Infinite%20Jump.lua"))()
end)

InfYeld.Name = "InfYeld"
InfYeld.Parent = ScrollingFrame
InfYeld.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
InfYeld.BorderColor3 = Color3.fromRGB(0, 0, 0)
InfYeld.Position = UDim2.new(0.060283687, 0, 0.369227827, 0)
InfYeld.Size = UDim2.new(0, 113, 0, 51)
InfYeld.Font = Enum.Font.Cartoon
InfYeld.Text = "InfYeld"
InfYeld.TextColor3 = Color3.fromRGB(135, 243, 255)
InfYeld.TextSize = 29.000
InfYeld.TextWrapped = true
InfYeld.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/Infinite%20Yield.lua"))()
end)

ESP.Name = "ESP"
ESP.Parent = ScrollingFrame
ESP.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
ESP.BorderColor3 = Color3.fromRGB(0, 0, 0)
ESP.Position = UDim2.new(0.5, 0, 0.500330567, 0)
ESP.Size = UDim2.new(0, 109, 0, 51)
ESP.Font = Enum.Font.Cartoon
ESP.Text = "ESP"
ESP.TextColor3 = Color3.fromRGB(135, 243, 255)
ESP.TextSize = 29.000
ESP.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/WRD%20ESP.lua"))()
end)

Suicide.Name = "Suicide"
Suicide.Parent = ScrollingFrame
Suicide.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
Suicide.BorderColor3 = Color3.fromRGB(0, 0, 0)
Suicide.Position = UDim2.new(0.060283687, 0, 0.503211796, 0)
Suicide.Size = UDim2.new(0, 113, 0, 51)
Suicide.Font = Enum.Font.Cartoon
Suicide.Text = "Suicide gun"
Suicide.TextColor3 = Color3.fromRGB(255, 64, 245)
Suicide.TextScaled = true
Suicide.TextSize = 29.000
Suicide.TextWrapped = true
Suicide.MouseButton1Down:connect(function()
	--SUICIDE GUN REBORN BY DMS
	o1 = Instance.new("Tool")
	o2 = Instance.new("Part")
	o3 = Instance.new("SpecialMesh")
	o4 = Instance.new("Part")
	o5 = Instance.new("BlockMesh")
	o6 = Instance.new("Part")
	o7 = Instance.new("BlockMesh")
	o8 = Instance.new("Part")
	o9 = Instance.new("BlockMesh")
	o10 = Instance.new("Part")
	o11 = Instance.new("BlockMesh")
	o12 = Instance.new("Part")
	o13 = Instance.new("BlockMesh")
	o14 = Instance.new("Part")
	o15 = Instance.new("BlockMesh")
	o16 = Instance.new("Part")
	o17 = Instance.new("BlockMesh")
	o18 = Instance.new("Part")
	o19 = Instance.new("BlockMesh")
	o20 = Instance.new("Part")
	o21 = Instance.new("CylinderMesh")
	o22 = Instance.new("Part")
	o23 = Instance.new("CylinderMesh")
	o24 = Instance.new("Part")
	o25 = Instance.new("CylinderMesh")
	o26 = Instance.new("Part")
	o27 = Instance.new("BlockMesh")
	o28 = Instance.new("Part")
	o29 = Instance.new("CylinderMesh")
	o30 = Instance.new("Part")
	o31 = Instance.new("PointLight")
	o32 = Instance.new("BillboardGui")
	o33 = Instance.new("ImageLabel")
	o34 = Instance.new("BlockMesh")
	o35 = Instance.new("Part")
	o36 = Instance.new("BlockMesh")
	o37 = Instance.new("Part")
	o38 = Instance.new("BlockMesh")
	o39 = Instance.new("Part")
	o40 = Instance.new("BlockMesh")
	o41 = Instance.new("Part")
	o42 = Instance.new("Decal")
	o43 = Instance.new("CylinderMesh")
	o44 = Instance.new("Part")
	o45 = Instance.new("CylinderMesh")
	o46 = Instance.new("Part")
	o47 = Instance.new("BlockMesh")
	o48 = Instance.new("Part")
	o49 = Instance.new("SpecialMesh")
	o50 = Instance.new("Part")
	o51 = Instance.new("SpecialMesh")
	o52 = Instance.new("Part")
	o53 = Instance.new("BlockMesh")
	o54 = Instance.new("Part")
	o55 = Instance.new("BlockMesh")
	o56 = Instance.new("Part")
	o57 = Instance.new("BlockMesh")
	o58 = Instance.new("Part")
	o59 = Instance.new("CylinderMesh")
	o60 = Instance.new("Part")
	o61 = Instance.new("SpecialMesh")
	o62 = Instance.new("Part")
	o63 = Instance.new("BlockMesh")
	o64 = Instance.new("Part")
	o65 = Instance.new("SpecialMesh")
	o66 = Instance.new("Part")
	o67 = Instance.new("BlockMesh")
	o68 = Instance.new("Part")
	o69 = Instance.new("BlockMesh")
	o70 = Instance.new("Part")
	o71 = Instance.new("SpecialMesh")
	o72 = Instance.new("Part")
	o73 = Instance.new("BlockMesh")
	o74 = Instance.new("Part")
	o75 = Instance.new("BlockMesh")
	o76 = Instance.new("Part")
	o77 = Instance.new("BlockMesh")
	o78 = Instance.new("Part")
	o79 = Instance.new("SpecialMesh")
	o80 = Instance.new("Part")
	o81 = Instance.new("CylinderMesh")
	o82 = Instance.new("Part")
	o83 = Instance.new("SpecialMesh")
	o84 = Instance.new("Part")
	o85 = Instance.new("BlockMesh")
	o86 = Instance.new("Part")
	o87 = Instance.new("SpecialMesh")
	o88 = Instance.new("Part")
	o89 = Instance.new("SpecialMesh")
	o90 = Instance.new("Part")
	o91 = Instance.new("BlockMesh")
	o92 = Instance.new("Part")
	o93 = Instance.new("BlockMesh")
	o94 = Instance.new("Part")
	o95 = Instance.new("SpecialMesh")
	o96 = Instance.new("Part")
	o97 = Instance.new("BlockMesh")
	o98 = Instance.new("Part")
	o99 = Instance.new("SpecialMesh")
	o100 = Instance.new("Part")
	o101 = Instance.new("BlockMesh")
	o102 = Instance.new("Part")
	o103 = Instance.new("BlockMesh")
	o104 = Instance.new("Part")
	o105 = Instance.new("SpecialMesh")
	o106 = Instance.new("Part")
	o107 = Instance.new("BlockMesh")
	o108 = Instance.new("Part")
	o109 = Instance.new("CylinderMesh")
	o110 = Instance.new("Part")
	o111 = Instance.new("BlockMesh")
	o112 = Instance.new("Part")
	o113 = Instance.new("SpecialMesh")
	o114 = Instance.new("Part")
	o115 = Instance.new("CylinderMesh")
	o116 = Instance.new("Part")
	o117 = Instance.new("BlockMesh")
	o118 = Instance.new("Part")
	o119 = Instance.new("SpecialMesh")
	o120 = Instance.new("Part")
	o121 = Instance.new("BlockMesh")
	o122 = Instance.new("Part")
	o123 = Instance.new("SpecialMesh")
	o124 = Instance.new("Part")
	o125 = Instance.new("SpecialMesh")
	o126 = Instance.new("Part")
	o127 = Instance.new("BlockMesh")
	o128 = Instance.new("Part")
	o129 = Instance.new("BlockMesh")
	o130 = Instance.new("Part")
	o131 = Instance.new("SpecialMesh")
	o132 = Instance.new("Part")
	o133 = Instance.new("BlockMesh")
	o134 = Instance.new("Part")
	o135 = Instance.new("BlockMesh")
	o136 = Instance.new("Part")
	o137 = Instance.new("SpecialMesh")
	o138 = Instance.new("Part")
	o139 = Instance.new("BlockMesh")
	o140 = Instance.new("Part")
	o141 = Instance.new("CylinderMesh")
	o142 = Instance.new("Part")
	o143 = Instance.new("BlockMesh")
	o144 = Instance.new("Part")
	o145 = Instance.new("SpecialMesh")
	o146 = Instance.new("Part")
	o147 = Instance.new("SpecialMesh")
	o148 = Instance.new("Part")
	o149 = Instance.new("Sound")
	o150 = Instance.new("BlockMesh")
	o1.Name = "Suicide"
	o1.Parent = game.Players.LocalPlayer.Backpack
	o2.Parent = o1
	o2.Material = Enum.Material.SmoothPlastic
	o2.BrickColor = BrickColor.new("Really black")
	o2.Position = Vector3.new(18.950964, 0.850407004, 14.2854338)
	o2.Rotation = Vector3.new(-2.19040904e-013, 2.50129006e-006, -180)
	o2.Anchored = true
	o2.FormFactor = Enum.FormFactor.Custom
	o2.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o2.CFrame = CFrame.new(18.950964, 0.850407004, 14.2854338, -1, 8.74227766e-008, 4.36557457e-008, -8.74227766e-008, -1, 3.82298495e-015, 4.36557457e-008, 3.92853881e-018, 1)
	o2.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o2.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o3.Parent = o2
	o3.Scale = Vector3.new(0.666666687, 0.388888866, 0.416666687)
	o3.MeshType = Enum.MeshType.Wedge
	o4.Parent = o1
	o4.Material = Enum.Material.SmoothPlastic
	o4.BrickColor = BrickColor.new("Really black")
	o4.Position = Vector3.new(18.950964, 0.953182995, 14.5104237)
	o4.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o4.Anchored = true
	o4.FormFactor = Enum.FormFactor.Custom
	o4.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o4.CFrame = CFrame.new(18.950964, 0.953182995, 14.5104237, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o4.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o4.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o5.Parent = o4
	o5.Scale = Vector3.new(0.333333343, 0.194444433, 0.694444478)
	o6.Parent = o1
	o6.Material = Enum.Material.SmoothPlastic
	o6.BrickColor = BrickColor.new("Black")
	o6.Position = Vector3.new(18.950964, 1.13095105, 14.5993176)
	o6.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o6.Anchored = true
	o6.FormFactor = Enum.FormFactor.Custom
	o6.Size = Vector3.new(0.566666663, 0.200000003, 0.200000003)
	o6.CFrame = CFrame.new(18.950964, 1.13095105, 14.5993176, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o6.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o6.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o7.Parent = o6
	o7.Scale = Vector3.new(1, 0.583333313, 0.722222269)
	o8.Name = "SightBack"
	o8.Parent = o1
	o8.Material = Enum.Material.SmoothPlastic
	o8.Position = Vector3.new(18.950964, 1.23151195, 14.4882116)
	o8.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o8.Anchored = true
	o8.FormFactor = Enum.FormFactor.Custom
	o8.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o8.CFrame = CFrame.new(18.950964, 1.23151195, 14.4882116, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o8.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o8.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o8.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o8.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o8.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o8.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o9.Parent = o8
	o9.Scale = Vector3.new(0.166666672, 0.111111112, 0.411111116)
	o10.Parent = o1
	o10.Material = Enum.Material.SmoothPlastic
	o10.BrickColor = BrickColor.new("Really black")
	o10.Position = Vector3.new(18.950964, 0.961513996, 14.5937595)
	o10.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o10.Anchored = true
	o10.FormFactor = Enum.FormFactor.Custom
	o10.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o10.CFrame = CFrame.new(18.950964, 0.961513996, 14.5937595, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o10.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o10.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o11.Parent = o10
	o11.Scale = Vector3.new(0.49999997, 0.277777761, 0.694444478)
	o12.Parent = o1
	o12.Material = Enum.Material.SmoothPlastic
	o12.BrickColor = BrickColor.new("Really black")
	o12.Position = Vector3.new(18.950964, 1.19539297, 14.5993176)
	o12.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o12.Anchored = true
	o12.FormFactor = Enum.FormFactor.Custom
	o12.Size = Vector3.new(0.566666663, 0.200000003, 0.200000003)
	o12.CFrame = CFrame.new(18.950964, 1.19539297, 14.5993176, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o12.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o12.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o13.Parent = o12
	o13.Scale = Vector3.new(1, 0.249999985, 0.411111116)
	o14.Parent = o1
	o14.Material = Enum.Material.SmoothPlastic
	o14.BrickColor = BrickColor.new("Really black")
	o14.Position = Vector3.new(18.908186, 1.19095695, 14.5993176)
	o14.Rotation = Vector3.new(-90, 44.9999962, 90)
	o14.Anchored = true
	o14.FormFactor = Enum.FormFactor.Custom
	o14.Size = Vector3.new(0.566666663, 0.200000003, 0.200000003)
	o14.CFrame = CFrame.new(18.908186, 1.19095695, 14.5993176, 0, -0.707106709, 0.707106709, 5.38120031e-018, 0.707106769, 0.707106769, -1, 2.04281037e-011, 9.59801127e-011)
	o14.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o14.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o15.Parent = o14
	o15.Scale = Vector3.new(1, 0.194444433, 0.222222224)
	o16.Name = "SightBack"
	o16.Parent = o1
	o16.Material = Enum.Material.SmoothPlastic
	o16.Position = Vector3.new(18.9787407, 1.25372696, 14.4882116)
	o16.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o16.Anchored = true
	o16.FormFactor = Enum.FormFactor.Custom
	o16.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o16.CFrame = CFrame.new(18.9787407, 1.25372696, 14.4882116, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o16.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o16.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o16.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o16.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o16.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o16.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o17.Parent = o16
	o17.Scale = Vector3.new(0.166666672, 0.111111112, 0.13333334)
	o18.Name = "SightBack"
	o18.Parent = o1
	o18.Material = Enum.Material.SmoothPlastic
	o18.Position = Vector3.new(18.9231701, 1.25372696, 14.4882002)
	o18.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o18.Anchored = true
	o18.FormFactor = Enum.FormFactor.Custom
	o18.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o18.CFrame = CFrame.new(18.9231701, 1.25372696, 14.4882002, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o18.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o18.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o18.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o18.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o18.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o18.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o19.Parent = o18
	o19.Scale = Vector3.new(0.166666672, 0.111111112, 0.13333334)
	o20.Parent = o1
	o20.Material = Enum.Material.SmoothPlastic
	o20.BrickColor = BrickColor.new("Black")
	o20.Position = Vector3.new(18.950964, 0.886528015, 14.5798664)
	o20.Rotation = Vector3.new(-90, -2.50447761e-006, -90)
	o20.Anchored = true
	o20.FormFactor = Enum.FormFactor.Custom
	o20.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o20.CFrame = CFrame.new(18.950964, 0.886528015, 14.5798664, -8.74279067e-008, 1, -4.37113812e-008, -3.83195418e-015, 4.37113812e-008, 1, 1, 8.74279067e-008, -4.65359901e-018)
	o20.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o20.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o21.Parent = o20
	o21.Scale = Vector3.new(0.416666687, 0.722222269, 0.416666687)
	o22.Name = "SightLine"
	o22.Parent = o1
	o22.Material = Enum.Material.SmoothPlastic
	o22.BrickColor = BrickColor.new("Smoky grey")
	o22.Position = Vector3.new(18.950964, 1.21539295, 15.7804356)
	o22.Rotation = Vector3.new(90, -2.50447761e-006, -90)
	o22.Anchored = true
	o22.FormFactor = Enum.FormFactor.Custom
	o22.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o22.CFrame = CFrame.new(18.950964, 1.21539295, 15.7804356, 0, 1, -4.37113812e-008, 5.38120031e-018, -4.37113812e-008, -1, -1, 0, 6.1083781e-018)
	o22.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o22.Color = Color3.new(0.356863, 0.364706, 0.411765)
	o23.Parent = o22
	o23.Scale = Vector3.new(0.505999982, 0.150000006, 0.505999982)
	o24.Parent = o1
	o24.Material = Enum.Material.SmoothPlastic
	o24.BrickColor = BrickColor.new("Black")
	o24.Position = Vector3.new(18.950964, 0.96707201, 15.7326679)
	o24.Rotation = Vector3.new(-90, -2.50447761e-006, -180)
	o24.Anchored = true
	o24.FormFactor = Enum.FormFactor.Custom
	o24.Size = Vector3.new(0.200000003, 0.344444454, 0.200000003)
	o24.CFrame = CFrame.new(18.950964, 0.96707201, 15.7326679, -1, 4.36557457e-008, -4.37113812e-008, -4.37113812e-008, 1.9122997e-015, 1, 4.36557457e-008, 1, -4.65359901e-018)
	o24.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o24.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o25.Parent = o24
	o25.Scale = Vector3.new(0.405599982, 1, 0.405599982)
	o26.Parent = o1
	o26.Material = Enum.Material.SmoothPlastic
	o26.BrickColor = BrickColor.new("Black")
	o26.Position = Vector3.new(18.950964, 1.01984501, 15.7298756)
	o26.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o26.Anchored = true
	o26.FormFactor = Enum.FormFactor.Custom
	o26.Size = Vector3.new(0.338888884, 0.200000003, 0.200000003)
	o26.CFrame = CFrame.new(18.950964, 1.01984501, 15.7298756, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o26.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o26.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o27.Parent = o26
	o27.Scale = Vector3.new(1, 0.527777731, 0.611111104)
	o28.Parent = o1
	o28.Material = Enum.Material.SmoothPlastic
	o28.BrickColor = BrickColor.new("Black")
	o28.Position = Vector3.new(18.950964, 0.96707201, 15.7298756)
	o28.Rotation = Vector3.new(-90, -2.50447761e-006, -180)
	o28.Anchored = true
	o28.FormFactor = Enum.FormFactor.Custom
	o28.Size = Vector3.new(0.200000003, 0.338888884, 0.200000003)
	o28.CFrame = CFrame.new(18.950964, 0.96707201, 15.7298756, -1, 4.36557457e-008, -4.37113812e-008, -4.37113812e-008, 1.9122997e-015, 1, 4.36557457e-008, 1, -4.65359901e-018)
	o28.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o28.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o29.Parent = o28
	o29.Scale = Vector3.new(0.611111104, 1, 0.611111104)
	o30.Name = "Main"
	o30.Parent = o1
	o30.Material = Enum.Material.SmoothPlastic
	o30.BrickColor = BrickColor.new("Really black")
	o30.Transparency = 1
	o30.Position = Vector3.new(18.950964, 1.12816894, 15.9493256)
	o30.Rotation = Vector3.new(90, -2.50447761e-006, 2.50796006e-006)
	o30.Anchored = true
	o30.FormFactor = Enum.FormFactor.Custom
	o30.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o30.CFrame = CFrame.new(18.950964, 1.12816894, 15.9493256, 1, -4.3772161e-008, -4.37113812e-008, -4.37113812e-008, -1.49011594e-008, -1, 4.3772161e-008, 1, -1.49011603e-008)
	o30.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o30.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o31.Name = "FlashFX"
	o31.Parent = o30
	o31.Color = Color3.new(1, 1, 0)
	o31.Enabled = false
	o31.Brightness = 10
	o31.Range = 6
	o31.Shadows = true
	o32.Name = "FlashGui"
	o32.Parent = o30
	o32.Size = UDim2.new(1.1000000238419,0,1.1000000238419,0)
	o32.Enabled = false
	o33.Name = "Label"
	o33.Parent = o32
	o33.Size = UDim2.new(1,0,1,0)
	o33.BackgroundTransparency = 1
	o33.Image = "http://www.roblox.com/asset/?id=117472237"
	o34.Parent = o30
	o34.Scale = Vector3.new(0.99999994, 0.99999994, 0.99999994)
	o35.Parent = o1
	o35.Material = Enum.Material.SmoothPlastic
	o35.BrickColor = BrickColor.new("Black")
	o35.Position = Vector3.new(18.908186, 1.19095695, 15.5132236)
	o35.Rotation = Vector3.new(-90, 44.9999962, 90)
	o35.Anchored = true
	o35.FormFactor = Enum.FormFactor.Custom
	o35.Size = Vector3.new(0.772222221, 0.200000003, 0.200000003)
	o35.CFrame = CFrame.new(18.908186, 1.19095695, 15.5132236, 0, -0.707106709, 0.707106709, 5.38120031e-018, 0.707106769, 0.707106769, -1, 2.04281037e-011, 9.59801127e-011)
	o35.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o35.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o36.Parent = o35
	o36.Scale = Vector3.new(1, 0.194444433, 0.222222224)
	o37.Parent = o1
	o37.Material = Enum.Material.SmoothPlastic
	o37.BrickColor = BrickColor.new("Black")
	o37.Position = Vector3.new(18.950964, 1.19539297, 15.5132236)
	o37.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o37.Anchored = true
	o37.FormFactor = Enum.FormFactor.Custom
	o37.Size = Vector3.new(0.772222221, 0.200000003, 0.200000003)
	o37.CFrame = CFrame.new(18.950964, 1.19539297, 15.5132236, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o37.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o37.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o38.Parent = o37
	o38.Scale = Vector3.new(1, 0.249999985, 0.411111116)
	o39.Parent = o1
	o39.Material = Enum.Material.SmoothPlastic
	o39.BrickColor = BrickColor.new("Black")
	o39.Position = Vector3.new(18.950964, 1.13095105, 15.5132236)
	o39.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o39.Anchored = true
	o39.FormFactor = Enum.FormFactor.Custom
	o39.Size = Vector3.new(0.772222221, 0.200000003, 0.200000003)
	o39.CFrame = CFrame.new(18.950964, 1.13095105, 15.5132236, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o39.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o39.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o40.Parent = o39
	o40.Scale = Vector3.new(1, 0.583333313, 0.722222269)
	o41.Parent = o1
	o41.Material = Enum.Material.SmoothPlastic
	o41.BrickColor = BrickColor.new("Black")
	o41.Position = Vector3.new(18.950964, 1.12816894, 15.3854284)
	o41.Rotation = Vector3.new(-90, -2.50447761e-006, -180)
	o41.Anchored = true
	o41.FormFactor = Enum.FormFactor.Custom
	o41.Size = Vector3.new(0.200000003, 1.06111109, 0.200000003)
	o41.CFrame = CFrame.new(18.950964, 1.12816894, 15.3854284, -1, 4.36557457e-008, -4.37113812e-008, -4.37113812e-008, 1.9122997e-015, 1, 4.36557457e-008, 1, -4.65359901e-018)
	o41.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o41.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o42.Parent = o41
	o42.Texture = "http://www.roblox.com/asset/?id=47760372"
	o42.Face = Enum.NormalId.Top
	o43.Parent = o41
	o43.Scale = Vector3.new(0.49999997, 1, 0.49999997)
	o44.Parent = o1
	o44.Material = Enum.Material.SmoothPlastic
	o44.BrickColor = BrickColor.new("Black")
	o44.Position = Vector3.new(18.950964, 0.961513996, 15.352108)
	o44.Rotation = Vector3.new(-90, -2.50447761e-006, -180)
	o44.Anchored = true
	o44.FormFactor = Enum.FormFactor.Custom
	o44.Size = Vector3.new(0.200000003, 0.416666627, 0.200000003)
	o44.CFrame = CFrame.new(18.950964, 0.961513996, 15.352108, -1, 4.36557457e-008, -4.37113812e-008, -4.37113812e-008, 1.9122997e-015, 1, 4.36557457e-008, 1, -4.65359901e-018)
	o44.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o44.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o45.Parent = o44
	o45.Scale = Vector3.new(0.666666687, 1, 0.666666687)
	o46.Name = "Mag"
	o46.Parent = o1
	o46.Material = Enum.Material.SmoothPlastic
	o46.BrickColor = BrickColor.new("Black")
	o46.Position = Vector3.new(18.950964, 0.129971996, 14.3866644)
	o46.Rotation = Vector3.new(101, 90, 0)
	o46.Anchored = true
	o46.FormFactor = Enum.FormFactor.Custom
	o46.Size = Vector3.new(0.200000003, 0.333333343, 0.200000003)
	o46.CFrame = CFrame.new(18.950964, 0.129971996, 14.3866644, -2.79885857e-008, -5.49657244e-008, 1, 0.981627166, -0.190809026, 1.69563066e-008, 0.190809026, 0.981627107, 5.93718141e-008)
	o46.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o46.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o47.Parent = o46
	o47.Scale = Vector3.new(0.027777778, 1, 0.666666687)
	o48.Parent = o1
	o48.Material = Enum.Material.SmoothPlastic
	o48.BrickColor = BrickColor.new("Black")
	o48.Position = Vector3.new(18.950964, 0.161533996, 14.3493176)
	o48.Rotation = Vector3.new(0.019784553, -6.66929267e-009, 180)
	o48.Anchored = true
	o48.FormFactor = Enum.FormFactor.Custom
	o48.Size = Vector3.new(0.200000003, 0.200000003, 0.266666681)
	o48.CFrame = CFrame.new(18.950964, 0.161533996, 14.3493176, -1, -8.74227979e-008, -1.16401111e-010, 8.74227766e-008, -0.99999994, -0.000345305598, 0, -0.000345305569, 0.99999994)
	o48.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o48.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o49.Parent = o48
	o49.Scale = Vector3.new(0.694444478, 0.222222224, 1)
	o49.MeshType = Enum.MeshType.Wedge
	o50.Parent = o1
	o50.Material = Enum.Material.SmoothPlastic
	o50.BrickColor = BrickColor.new("Really black")
	o50.Position = Vector3.new(18.950964, 0.155975997, 14.3354216)
	o50.Rotation = Vector3.new(3.08320072e-016, 0, -180)
	o50.Anchored = true
	o50.FormFactor = Enum.FormFactor.Custom
	o50.Size = Vector3.new(0.200000003, 0.200000003, 0.438888878)
	o50.CFrame = CFrame.new(18.950964, 0.155975997, 14.3354216, -1, 1.0960446e-021, 0, 1.0960446e-021, -1, -5.38120031e-018, 0, 5.38120031e-018, 1)
	o50.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o50.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o51.Parent = o50
	o51.Scale = Vector3.new(0.666666687, 0.333333343, 1)
	o51.MeshType = Enum.MeshType.Wedge
	o52.Parent = o1
	o52.Material = Enum.Material.SmoothPlastic
	o52.BrickColor = BrickColor.new("Black")
	o52.Position = Vector3.new(18.950964, 0.239300996, 14.1882057)
	o52.Rotation = Vector3.new(105, 90, 0)
	o52.Anchored = true
	o52.FormFactor = Enum.FormFactor.Custom
	o52.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o52.CFrame = CFrame.new(18.950964, 0.239300996, 14.1882057, -1.07331601e-008, -6.40018527e-008, 1, 0.965925813, -0.258819044, -6.21114538e-009, 0.258819073, 0.965925813, 6.46105036e-008)
	o52.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o52.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o53.Parent = o52
	o53.Scale = Vector3.new(0.944444478, 0.111111112, 0.611111104)
	o54.Parent = o1
	o54.Material = Enum.Material.SmoothPlastic
	o54.BrickColor = BrickColor.new("Really black")
	o54.Position = Vector3.new(18.950964, 0.225419, 14.3520937)
	o54.Rotation = Vector3.new(-3.25256337e-007, 90, 0)
	o54.Anchored = true
	o54.FormFactor = Enum.FormFactor.Custom
	o54.Size = Vector3.new(0.26111111, 0.200000003, 0.200000003)
	o54.CFrame = CFrame.new(18.950964, 0.225419, 14.3520937, 8.94069672e-008, -6.24762481e-015, 1, -5.6767937e-009, 1, 1.42108539e-014, -1, -5.6767937e-009, 8.94069672e-008)
	o54.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o54.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o55.Parent = o54
	o55.Scale = Vector3.new(1, 0.416666687, 0.694444478)
	o56.Parent = o1
	o56.Material = Enum.Material.SmoothPlastic
	o56.BrickColor = BrickColor.new("Really black")
	o56.Position = Vector3.new(18.950964, 0.197641, 14.2215319)
	o56.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o56.Anchored = true
	o56.FormFactor = Enum.FormFactor.Custom
	o56.Size = Vector3.new(0.211111099, 0.200000003, 0.200000003)
	o56.CFrame = CFrame.new(18.950964, 0.197641, 14.2215319, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o56.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o56.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o57.Parent = o56
	o57.Scale = Vector3.new(1, 0.0833333358, 0.666666687)
	o58.Parent = o1
	o58.Material = Enum.Material.SmoothPlastic
	o58.BrickColor = BrickColor.new("Really black")
	o58.Position = Vector3.new(18.950964, 0.258204013, 14.3493176)
	o58.Rotation = Vector3.new(-90, -2.50447761e-006, -90)
	o58.Anchored = true
	o58.FormFactor = Enum.FormFactor.Custom
	o58.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o58.CFrame = CFrame.new(18.950964, 0.258204013, 14.3493176, -8.74279067e-008, 1, -4.37113812e-008, -3.83195418e-015, 4.37113812e-008, 1, 1, 8.74279067e-008, -4.65359901e-018)
	o58.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o58.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o59.Parent = o58
	o59.Scale = Vector3.new(0.49999997, 0.722222269, 0.472222239)
	o60.Parent = o1
	o60.Material = Enum.Material.SmoothPlastic
	o60.BrickColor = BrickColor.new("Really black")
	o60.Position = Vector3.new(18.950964, 0.244874001, 14.1993141)
	o60.Rotation = Vector3.new(0.019784553, -6.66929267e-009, 180)
	o60.Anchored = true
	o60.FormFactor = Enum.FormFactor.Custom
	o60.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o60.CFrame = CFrame.new(18.950964, 0.244874001, 14.1993141, -1, -8.74227979e-008, -1.16401111e-010, 8.74227766e-008, -0.99999994, -0.000345305598, 0, -0.000345305569, 0.99999994)
	o60.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o60.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o61.Parent = o60
	o61.Scale = Vector3.new(0.694444478, 0.222222224, 0.222222224)
	o61.MeshType = Enum.MeshType.Wedge
	o62.Parent = o1
	o62.Material = Enum.Material.SmoothPlastic
	o62.BrickColor = BrickColor.new("Black")
	o62.Position = Vector3.new(18.993742, 1.19095695, 15.1076584)
	o62.Rotation = Vector3.new(90, 44.9999962, -90)
	o62.Anchored = true
	o62.FormFactor = Enum.FormFactor.Custom
	o62.Size = Vector3.new(1.58333337, 0.200000003, 0.200000003)
	o62.CFrame = CFrame.new(18.993742, 1.19095695, 15.1076584, 0, 0.707106709, 0.707106709, 5.38120031e-018, 0.707106769, -0.707106769, -1, 9.59801127e-011, -2.04281037e-011)
	o62.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o62.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o63.Parent = o62
	o63.Scale = Vector3.new(1, 0.194444433, 0.222222224)
	o64.Parent = o1
	o64.Material = Enum.Material.SmoothPlastic
	o64.Position = Vector3.new(18.950964, 0.867092013, 15.1298876)
	o64.Rotation = Vector3.new(180, 2.50796006e-006, 8.65142192e-006)
	o64.Anchored = true
	o64.FormFactor = Enum.FormFactor.Custom
	o64.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o64.CFrame = CFrame.new(18.950964, 0.867092013, 15.1298876, 1, -1.50995803e-007, 4.3772161e-008, -1.50995803e-007, -1, -6.59664855e-015, 4.3772161e-008, 3.92853881e-018, -1)
	o64.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o64.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o64.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o64.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o64.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o64.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o65.Parent = o64
	o65.Scale = Vector3.new(0.611111104, 0.333333343, 0.138888881)
	o65.MeshType = Enum.MeshType.Wedge
	o66.Parent = o1
	o66.Material = Enum.Material.SmoothPlastic
	o66.Position = Vector3.new(18.950964, 0.83930999, 15.1048679)
	o66.Rotation = Vector3.new(89.9999771, 90, 0)
	o66.Anchored = true
	o66.FormFactor = Enum.FormFactor.Custom
	o66.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o66.CFrame = CFrame.new(18.950964, 0.83930999, 15.1048679, -8.74231674e-008, 2.50292942e-008, 1, 1, 4.33125763e-007, 8.74231461e-008, -4.33125791e-007, 1, -2.50292942e-008)
	o66.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o66.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o66.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o66.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o66.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o66.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o67.Parent = o66
	o67.Scale = Vector3.new(0.944444478, 0.111111112, 0.611111104)
	o68.Parent = o1
	o68.Material = Enum.Material.SmoothPlastic
	o68.BrickColor = BrickColor.new("Fossil")
	o68.Position = Vector3.new(18.950964, 0.716949999, 15.0719404)
	o68.Rotation = Vector3.new(-45, 90, 0)
	o68.Anchored = true
	o68.FormFactor = Enum.FormFactor.Custom
	o68.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o68.CFrame = CFrame.new(18.950964, 0.716949999, 15.0719404, -1.36843425e-010, -2.04281037e-011, 1, -0.707106769, 0.707106769, -1.0960446e-021, -0.707106709, -0.707106709, 0)
	o68.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o68.Color = Color3.new(0.623529, 0.631373, 0.67451)
	o69.Parent = o68
	o69.Scale = Vector3.new(0.527777731, 0.111111112, 0.611111104)
	o70.Parent = o1
	o70.Material = Enum.Material.SmoothPlastic
	o70.BrickColor = BrickColor.new("Black")
	o70.Position = Vector3.new(18.950964, 0.875427008, 15.0743237)
	o70.Rotation = Vector3.new(3.08320072e-016, 0, -180)
	o70.Anchored = true
	o70.FormFactor = Enum.FormFactor.Custom
	o70.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o70.CFrame = CFrame.new(18.950964, 0.875427008, 15.0743237, -1, 1.0960446e-021, 0, 1.0960446e-021, -1, -5.38120031e-018, 0, 5.38120031e-018, 1)
	o70.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o70.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o71.Parent = o70
	o71.Scale = Vector3.new(0.611111104, 0.249999985, 0.194444433)
	o71.MeshType = Enum.MeshType.Wedge
	o72.Parent = o1
	o72.Material = Enum.Material.SmoothPlastic
	o72.BrickColor = BrickColor.new("Black")
	o72.Position = Vector3.new(18.9315281, 1.09817195, 15.0048761)
	o72.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o72.Anchored = true
	o72.FormFactor = Enum.FormFactor.Custom
	o72.Size = Vector3.new(0.244444445, 0.200000003, 0.200000003)
	o72.CFrame = CFrame.new(18.9315281, 1.09817195, 15.0048761, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o72.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o72.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o73.Parent = o72
	o73.Scale = Vector3.new(1, 0.277777761, 0.527777731)
	o74.Parent = o1
	o74.Material = Enum.Material.SmoothPlastic
	o74.BrickColor = BrickColor.new("Black")
	o74.Position = Vector3.new(18.9870701, 1.13095105, 15.0048761)
	o74.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o74.Anchored = true
	o74.FormFactor = Enum.FormFactor.Custom
	o74.Size = Vector3.new(0.244444445, 0.200000003, 0.200000003)
	o74.CFrame = CFrame.new(18.9870701, 1.13095105, 15.0048761, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o74.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o74.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o75.Parent = o74
	o75.Scale = Vector3.new(1, 0.583333313, 0.361111134)
	o76.Parent = o1
	o76.Material = Enum.Material.SmoothPlastic
	o76.BrickColor = BrickColor.new("Black")
	o76.Position = Vector3.new(18.970396, 1.17595196, 15.0048761)
	o76.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o76.Anchored = true
	o76.FormFactor = Enum.FormFactor.Custom
	o76.Size = Vector3.new(0.244444445, 0.200000003, 0.200000003)
	o76.CFrame = CFrame.new(18.970396, 1.17595196, 15.0048761, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o76.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o76.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o77.Parent = o76
	o77.Scale = Vector3.new(1, 0.444444448, 0.216666669)
	o78.Parent = o1
	o78.Material = Enum.Material.SmoothPlastic
	o78.BrickColor = BrickColor.new("Black")
	o78.Position = Vector3.new(18.950964, 0.39764601, 14.6493216)
	o78.Rotation = Vector3.new(180, 2.50796006e-006, 5.00895612e-006)
	o78.Anchored = true
	o78.FormFactor = Enum.FormFactor.Custom
	o78.Size = Vector3.new(0.200000003, 0.550000012, 0.200000003)
	o78.CFrame = CFrame.new(18.950964, 0.39764601, 14.6493216, 1, -8.74227766e-008, 4.3772161e-008, -8.74227766e-008, -1, -3.8177829e-015, 4.3772161e-008, 6.83386182e-018, -1)
	o78.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o78.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o79.Parent = o78
	o79.Scale = Vector3.new(0.666666687, 1, 0.944444478)
	o79.MeshType = Enum.MeshType.Wedge
	o80.Parent = o1
	o80.Material = Enum.Material.SmoothPlastic
	o80.BrickColor = BrickColor.new("Black")
	o80.Position = Vector3.new(18.8859501, 0.96707201, 15.0021019)
	o80.Rotation = Vector3.new(-90, -2.50447761e-006, -90.0000076)
	o80.Anchored = true
	o80.FormFactor = Enum.FormFactor.Custom
	o80.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o80.CFrame = CFrame.new(18.8859501, 0.96707201, 15.0021019, -1.51107088e-007, 1, -4.37113812e-008, -6.60488848e-015, 4.37113812e-008, 1, 1, 1.51107088e-007, -4.65359901e-018)
	o80.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o80.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o81.Parent = o80
	o81.Scale = Vector3.new(0.249999985, 0.027777778, 0.249999985)
	o82.Parent = o1
	o82.Material = Enum.Material.SmoothPlastic
	o82.BrickColor = BrickColor.new("Dark stone grey")
	o82.Position = Vector3.new(18.950964, 0.858749986, 14.8770924)
	o82.Rotation = Vector3.new(-180, -2.50796256e-006, 5.00895703e-006)
	o82.Anchored = true
	o82.FormFactor = Enum.FormFactor.Custom
	o82.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o82.CFrame = CFrame.new(18.950964, 0.858749986, 14.8770924, 0.99999994, -8.74227837e-008, -4.37722036e-008, -8.74227837e-008, -0.99999994, 7.17606313e-018, -4.36557599e-008, 1.89421216e-015, -0.999999762)
	o82.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o82.Color = Color3.new(0.388235, 0.372549, 0.384314)
	o83.Parent = o82
	o83.Scale = Vector3.new(0.472222239, 0.416666687, 0.222222224)
	o83.MeshType = Enum.MeshType.Wedge
	o84.Parent = o1
	o84.Material = Enum.Material.SmoothPlastic
	o84.BrickColor = BrickColor.new("Black")
	o84.Position = Vector3.new(18.950964, 1.05040395, 14.9382162)
	o84.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o84.Anchored = true
	o84.FormFactor = Enum.FormFactor.Custom
	o84.Size = Vector3.new(1.24444449, 0.200000003, 0.200000003)
	o84.CFrame = CFrame.new(18.950964, 1.05040395, 14.9382162, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o84.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o84.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o85.Parent = o84
	o85.Scale = Vector3.new(1, 0.222222224, 0.722222269)
	o86.Parent = o1
	o86.Material = Enum.Material.SmoothPlastic
	o86.BrickColor = BrickColor.new("Black")
	o86.Position = Vector3.new(18.950964, 0.469879985, 14.2215319)
	o86.Rotation = Vector3.new(2.05579065e-016, -2.50796006e-006, 6.27987314e-020)
	o86.Anchored = true
	o86.FormFactor = Enum.FormFactor.Custom
	o86.Size = Vector3.new(0.200000003, 0.527777791, 0.211111099)
	o86.CFrame = CFrame.new(18.950964, 0.469879985, 14.2215319, 1, -1.0960446e-021, -4.3772161e-008, -7.78546341e-022, 1, -3.58803156e-018, 4.3772161e-008, -5.38120031e-018, 1)
	o86.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o86.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o87.Parent = o86
	o87.Scale = Vector3.new(0.666666687, 1, 1)
	o87.MeshType = Enum.MeshType.Wedge
	o88.Parent = o1
	o88.Material = Enum.Material.SmoothPlastic
	o88.BrickColor = BrickColor.new("Dark stone grey")
	o88.Position = Vector3.new(18.950964, 0.736557007, 14.8798761)
	o88.Rotation = Vector3.new(180, -2.50129006e-006, 180)
	o88.Anchored = true
	o88.FormFactor = Enum.FormFactor.Custom
	o88.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o88.CFrame = CFrame.new(18.950964, 0.736557007, 14.8798761, -1, -1.0960446e-021, -4.36557457e-008, 1.41269847e-021, 1, -1.6144448e-018, 4.36557457e-008, -5.38120031e-018, -1)
	o88.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o88.Color = Color3.new(0.388235, 0.372549, 0.384314)
	o89.Parent = o88
	o89.Scale = Vector3.new(0.472222239, 0.416666687, 0.249999985)
	o89.MeshType = Enum.MeshType.Wedge
	o90.Parent = o1
	o90.Material = Enum.Material.SmoothPlastic
	o90.BrickColor = BrickColor.new("Smoky grey")
	o90.Position = Vector3.new(18.950964, 0.683766007, 14.9020796)
	o90.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o90.Anchored = true
	o90.FormFactor = Enum.FormFactor.Custom
	o90.Size = Vector3.new(0.283333331, 0.200000003, 0.200000003)
	o90.CFrame = CFrame.new(18.950964, 0.683766007, 14.9020796, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o90.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o90.Color = Color3.new(0.356863, 0.364706, 0.411765)
	o91.Parent = o90
	o91.Scale = Vector3.new(1, 0.111111112, 0.611111104)
	o92.Parent = o1
	o92.Material = Enum.Material.SmoothPlastic
	o92.BrickColor = BrickColor.new("Black")
	o92.Position = Vector3.new(18.950964, 0.992074013, 14.9382162)
	o92.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o92.Anchored = true
	o92.FormFactor = Enum.FormFactor.Custom
	o92.Size = Vector3.new(1.24444449, 0.200000003, 0.200000003)
	o92.CFrame = CFrame.new(18.950964, 0.992074013, 14.9382162, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o92.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o92.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o93.Parent = o92
	o93.Scale = Vector3.new(1, 0.361111134, 0.666666687)
	o94.Parent = o1
	o94.Material = Enum.Material.SmoothPlastic
	o94.BrickColor = BrickColor.new("Black")
	o94.Position = Vector3.new(18.950964, 0.708733976, 14.827096)
	o94.Rotation = Vector3.new(-180, 0.0927856117, 180)
	o94.Anchored = true
	o94.FormFactor = Enum.FormFactor.Custom
	o94.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o94.CFrame = CFrame.new(18.950964, 0.708733976, 14.827096, -0.999998689, -1.0960446e-021, 0.00161941373, -1.1745207e-017, 1, 4.66291637e-018, -0.00161941373, -5.38120031e-018, -0.999998689)
	o94.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o94.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o95.Parent = o94
	o95.Scale = Vector3.new(0.611111104, 0.138888881, 0.249999985)
	o95.MeshType = Enum.MeshType.Wedge
	o96.Parent = o1
	o96.Material = Enum.Material.SmoothPlastic
	o96.BrickColor = BrickColor.new("Black")
	o96.Position = Vector3.new(18.950964, 0.797657013, 14.8104324)
	o96.Rotation = Vector3.new(180, -2.50129006e-006, 180)
	o96.Anchored = true
	o96.FormFactor = Enum.FormFactor.Custom
	o96.Size = Vector3.new(0.200000003, 0.205555543, 0.200000003)
	o96.CFrame = CFrame.new(18.950964, 0.797657013, 14.8104324, -1, -1.0960446e-021, -4.36557457e-008, 1.41269847e-021, 1, -1.6144448e-018, 4.36557457e-008, -5.38120031e-018, -1)
	o96.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o96.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o97.Parent = o96
	o97.Scale = Vector3.new(0.472222239, 1, 0.444444448)
	o98.Parent = o1
	o98.Material = Enum.Material.SmoothPlastic
	o98.BrickColor = BrickColor.new("Black")
	o98.Position = Vector3.new(18.950964, 0.875427008, 14.8298864)
	o98.Rotation = Vector3.new(-180, 0, -6.27987314e-020)
	o98.Anchored = true
	o98.FormFactor = Enum.FormFactor.Custom
	o98.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o98.CFrame = CFrame.new(18.950964, 0.875427008, 14.8298864, 1, 1.0960446e-021, 0, -1.0960446e-021, -1, 5.38120031e-018, 0, 5.38120031e-018, -1)
	o98.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o98.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o99.Parent = o98
	o99.Scale = Vector3.new(0.666666687, 0.249999985, 0.194444433)
	o99.MeshType = Enum.MeshType.Wedge
	o100.Parent = o1
	o100.Material = Enum.Material.SmoothPlastic
	o100.BrickColor = BrickColor.new("Black")
	o100.Position = Vector3.new(18.988184, 0.986526012, 14.8076496)
	o100.Rotation = Vector3.new(3.00000024, 90, 0)
	o100.Anchored = true
	o100.FormFactor = Enum.FormFactor.Custom
	o100.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o100.CFrame = CFrame.new(18.988184, 0.986526012, 14.8076496, 2.57358579e-011, -6.64535094e-012, 1, 0.0523359589, 0.99862951, -1.0960446e-021, -0.99862951, 0.0523359627, 0)
	o100.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o100.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o101.Parent = o100
	o101.Scale = Vector3.new(0.694444478, 0.249999985, 0.361111134)
	o102.Parent = o1
	o102.Material = Enum.Material.SmoothPlastic
	o102.BrickColor = BrickColor.new("Black")
	o102.Position = Vector3.new(18.950964, 0.875427008, 14.8020916)
	o102.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o102.Anchored = true
	o102.FormFactor = Enum.FormFactor.Custom
	o102.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o102.CFrame = CFrame.new(18.950964, 0.875427008, 14.8020916, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o102.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o102.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o103.Parent = o102
	o103.Scale = Vector3.new(0.0833333358, 0.249999985, 0.666666687)
	o104.Parent = o1
	o104.Material = Enum.Material.SmoothPlastic
	o104.BrickColor = BrickColor.new("Really black")
	o104.Position = Vector3.new(18.950964, 0.536549985, 14.6048756)
	o104.Rotation = Vector3.new(180, 2.50796006e-006, 5.00895612e-006)
	o104.Anchored = true
	o104.FormFactor = Enum.FormFactor.Custom
	o104.Size = Vector3.new(0.200000003, 0.794444382, 0.244444445)
	o104.CFrame = CFrame.new(18.950964, 0.536549985, 14.6048756, 1, -8.74227766e-008, 4.3772161e-008, -8.74227766e-008, -1, -3.8177829e-015, 4.3772161e-008, 6.83386182e-018, -1)
	o104.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o104.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o105.Parent = o104
	o105.Scale = Vector3.new(0.694444478, 1, 1)
	o105.MeshType = Enum.MeshType.Wedge
	o106.Name = "Mag"
	o106.Parent = o1
	o106.Material = Enum.Material.SmoothPlastic
	o106.BrickColor = BrickColor.new("Really black")
	o106.Position = Vector3.new(18.950964, 0.56080699, 14.4704056)
	o106.Rotation = Vector3.new(101, 90, 0)
	o106.Anchored = true
	o106.FormFactor = Enum.FormFactor.Custom
	o106.Size = Vector3.new(0.872222185, 0.322222203, 0.200000003)
	o106.CFrame = CFrame.new(18.950964, 0.56080699, 14.4704056, -2.79885857e-008, -5.65955389e-008, 1, 0.981627166, -0.190809026, 1.66447549e-008, 0.190809026, 0.981627107, 6.10016286e-008)
	o106.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o106.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o107.Parent = o106
	o107.Scale = Vector3.new(1, 1, 0.611111104)
	o108.Parent = o1
	o108.Material = Enum.Material.SmoothPlastic
	o108.BrickColor = BrickColor.new("Smoky grey")
	o108.Position = Vector3.new(18.950964, 0.731004, 14.7326536)
	o108.Rotation = Vector3.new(-90, 4.32571142e-006, -90.0000076)
	o108.Anchored = true
	o108.FormFactor = Enum.FormFactor.Custom
	o108.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o108.CFrame = CFrame.new(18.950964, 0.731004, 14.7326536, -1.51107088e-007, 1, 7.54979084e-008, 7.25342942e-015, -7.54979084e-008, 1, 1, 1.51107088e-007, 4.14945855e-015)
	o108.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o108.Color = Color3.new(0.356863, 0.364706, 0.411765)
	o109.Parent = o108
	o109.Scale = Vector3.new(0.416666687, 0.694444478, 0.416666687)
	o110.Parent = o1
	o110.Material = Enum.Material.SmoothPlastic
	o110.BrickColor = BrickColor.new("Black")
	o110.Position = Vector3.new(18.950964, 0.544876993, 14.4409838)
	o110.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o110.Anchored = true
	o110.FormFactor = Enum.FormFactor.Custom
	o110.Size = Vector3.new(0.227777779, 0.711111128, 0.200000003)
	o110.CFrame = CFrame.new(18.950964, 0.544876993, 14.4409838, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o110.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o110.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o111.Parent = o110
	o111.Scale = Vector3.new(1, 1, 0.666666687)
	o112.Parent = o1
	o112.Material = Enum.Material.SmoothPlastic
	o112.BrickColor = BrickColor.new("Black")
	o112.Position = Vector3.new(18.950964, 0.775434017, 14.7993164)
	o112.Rotation = Vector3.new(180, -2.50129006e-006, 180)
	o112.Anchored = true
	o112.FormFactor = Enum.FormFactor.Custom
	o112.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o112.CFrame = CFrame.new(18.950964, 0.775434017, 14.7993164, -1, -1.0960446e-021, -4.36557457e-008, 1.41269847e-021, 1, -1.6144448e-018, 4.36557457e-008, -5.38120031e-018, -1)
	o112.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o112.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o113.Parent = o112
	o113.Scale = Vector3.new(0.666666687, 0.249999985, 0.111111112)
	o113.MeshType = Enum.MeshType.Wedge
	o114.Parent = o1
	o114.Material = Enum.Material.SmoothPlastic
	o114.BrickColor = BrickColor.new("Black")
	o114.Position = Vector3.new(18.950964, 0.730996013, 14.7298584)
	o114.Rotation = Vector3.new(180, 0, -90.0000076)
	o114.Anchored = true
	o114.FormFactor = Enum.FormFactor.Custom
	o114.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o114.CFrame = CFrame.new(18.950964, 0.730996013, 14.7298584, -1.94707198e-007, 1, 0, 1, 1.94707169e-007, -4.37113883e-008, -4.37113883e-008, 0, -1)
	o114.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o114.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o115.Parent = o114
	o115.Scale = Vector3.new(0.833333373, 0.666666687, 0.805555522)
	o116.Parent = o1
	o116.Material = Enum.Material.SmoothPlastic
	o116.BrickColor = BrickColor.new("Black")
	o116.Position = Vector3.new(18.950964, 0.928192973, 14.7298584)
	o116.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o116.Anchored = true
	o116.FormFactor = Enum.FormFactor.Custom
	o116.Size = Vector3.new(0.827777743, 0.200000003, 0.200000003)
	o116.CFrame = CFrame.new(18.950964, 0.928192973, 14.7298584, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o116.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o116.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o117.Parent = o116
	o117.Scale = Vector3.new(1, 0.277777761, 0.666666687)
	o118.Parent = o1
	o118.Material = Enum.Material.SmoothPlastic
	o118.BrickColor = BrickColor.new("Black")
	o118.Position = Vector3.new(18.950964, 0.825424016, 14.7993164)
	o118.Rotation = Vector3.new(-180, 0, -6.27987314e-020)
	o118.Anchored = true
	o118.FormFactor = Enum.FormFactor.Custom
	o118.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o118.CFrame = CFrame.new(18.950964, 0.825424016, 14.7993164, 1, 1.0960446e-021, 0, -1.0960446e-021, -1, 5.38120031e-018, 0, 5.38120031e-018, -1)
	o118.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o118.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o119.Parent = o118
	o119.Scale = Vector3.new(0.666666687, 0.249999985, 0.111111112)
	o119.MeshType = Enum.MeshType.Wedge
	o120.Parent = o1
	o120.Material = Enum.Material.SmoothPlastic
	o120.BrickColor = BrickColor.new("Black")
	o120.Position = Vector3.new(18.950964, 0.600430012, 14.4798584)
	o120.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o120.Anchored = true
	o120.FormFactor = Enum.FormFactor.Custom
	o120.Size = Vector3.new(0.200000003, 0.666666687, 0.200000003)
	o120.CFrame = CFrame.new(18.950964, 0.600430012, 14.4798584, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o120.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o120.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o121.Parent = o120
	o121.Scale = Vector3.new(0.027777778, 1, 0.694444478)
	o122.Parent = o1
	o122.Material = Enum.Material.SmoothPlastic
	o122.BrickColor = BrickColor.new("Black")
	o122.Position = Vector3.new(18.950964, 0.980957985, 14.5104237)
	o122.Rotation = Vector3.new(2.05579065e-016, -2.50796006e-006, 6.27987314e-020)
	o122.Anchored = true
	o122.FormFactor = Enum.FormFactor.Custom
	o122.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o122.CFrame = CFrame.new(18.950964, 0.980957985, 14.5104237, 1, -1.0960446e-021, -4.3772161e-008, -7.78546341e-022, 1, -3.58803156e-018, 4.3772161e-008, -5.38120031e-018, 1)
	o122.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o122.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o123.Parent = o122
	o123.Scale = Vector3.new(0.694444478, 0.0833333358, 0.333333343)
	o123.MeshType = Enum.MeshType.Wedge
	o124.Parent = o1
	o124.Material = Enum.Material.SmoothPlastic
	o124.BrickColor = BrickColor.new("Black")
	o124.Position = Vector3.new(18.950964, 0.961513996, 14.6854324)
	o124.Rotation = Vector3.new(180, -2.50129006e-006, 180)
	o124.Anchored = true
	o124.FormFactor = Enum.FormFactor.Custom
	o124.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o124.CFrame = CFrame.new(18.950964, 0.961513996, 14.6854324, -1, -1.0960446e-021, -4.36557457e-008, 1.41269847e-021, 1, -1.6144448e-018, 4.36557457e-008, -5.38120031e-018, -1)
	o124.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o124.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o125.Parent = o124
	o125.Scale = Vector3.new(0.694444478, 0.277777761, 0.416666687)
	o125.MeshType = Enum.MeshType.Wedge
	o126.Parent = o1
	o126.Material = Enum.Material.SmoothPlastic
	o126.BrickColor = BrickColor.new("Really black")
	o126.Position = Vector3.new(18.950964, 0.803216994, 14.6715384)
	o126.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o126.Anchored = true
	o126.FormFactor = Enum.FormFactor.Custom
	o126.Size = Vector3.new(0.244444445, 0.200000003, 0.200000003)
	o126.CFrame = CFrame.new(18.950964, 0.803216994, 14.6715384, 0, -1.0960446e-021, 1, 5.38120031e-018, 1, -1.0960446e-021, -1, -5.38120031e-018, 0)
	o126.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o126.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o127.Parent = o126
	o127.Scale = Vector3.new(1, 0.972222209, 0.666666687)
	o128.Parent = o1
	o128.Material = Enum.Material.SmoothPlastic
	o128.BrickColor = BrickColor.new("Really black")
	o128.Position = Vector3.new(18.950964, 0.672379017, 14.6450357)
	o128.Rotation = Vector3.new(-30.0000038, 90, 0)
	o128.Anchored = true
	o128.FormFactor = Enum.FormFactor.Custom
	o128.Size = Vector3.new(0.205555543, 0.200000003, 0.200000003)
	o128.CFrame = CFrame.new(18.950964, 0.672379017, 14.6450357, 4.20376836e-008, -2.60188173e-008, 1, -0.50000006, 0.866025388, 4.35066809e-008, -0.866025388, -0.50000006, 2.33994797e-008)
	o128.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o128.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o129.Parent = o128
	o129.Scale = Vector3.new(1, 0.722222269, 0.666666687)
	o130.Parent = o1
	o130.Material = Enum.Material.SmoothPlastic
	o130.BrickColor = BrickColor.new("Really black")
	o130.Position = Vector3.new(18.950964, 0.619874001, 14.3270836)
	o130.Rotation = Vector3.new(2.05579065e-016, -2.50796006e-006, 6.27987314e-020)
	o130.Anchored = true
	o130.FormFactor = Enum.FormFactor.Custom
	o130.Size = Vector3.new(0.200000003, 0.705555558, 0.300000012)
	o130.CFrame = CFrame.new(18.950964, 0.619874001, 14.3270836, 1, -1.0960446e-021, -4.3772161e-008, -7.78546341e-022, 1, -3.58803156e-018, 4.3772161e-008, -5.38120031e-018, 1)
	o130.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o130.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o131.Parent = o130
	o131.Scale = Vector3.new(0.694444478, 1, 1)
	o131.MeshType = Enum.MeshType.Wedge
	o132.Parent = o1
	o132.Material = Enum.Material.SmoothPlastic
	o132.BrickColor = BrickColor.new("Black")
	o132.Position = Vector3.new(18.950964, 1.15317094, 14.2876415)
	o132.Rotation = Vector3.new(30.0000019, 90, 0)
	o132.Anchored = true
	o132.FormFactor = Enum.FormFactor.Custom
	o132.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o132.CFrame = CFrame.new(18.950964, 1.15317094, 14.2876415, 1.28167699e-010, -5.82076609e-011, 1, 0.5, 0.866025388, -1.0960446e-021, -0.866025388, 0.5, 0)
	o132.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o132.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o133.Parent = o132
	o133.Scale = Vector3.new(0.388888866, 0.194444433, 0.416666687)
	o134.Parent = o1
	o134.Material = Enum.Material.SmoothPlastic
	o134.BrickColor = BrickColor.new("Black")
	o134.Position = Vector3.new(18.950964, 1.10315704, 14.3126564)
	o134.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o134.Anchored = true
	o134.FormFactor = Enum.FormFactor.Custom
	o134.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o134.CFrame = CFrame.new(18.950964, 1.10315704, 14.3126564, 0, -5.9604659e-008, 1, 5.38120031e-018, 1, 5.9604659e-008, -1, -5.38374141e-018, 0)
	o134.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o134.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o135.Parent = o134
	o135.Scale = Vector3.new(0.027777778, 0.861111045, 0.416666687)
	o136.Parent = o1
	o136.Material = Enum.Material.SmoothPlastic
	o136.BrickColor = BrickColor.new("Black")
	o136.Position = Vector3.new(18.950964, 0.969842017, 14.2187424)
	o136.Rotation = Vector3.new(2.05579065e-016, -2.50796006e-006, 6.27987314e-020)
	o136.Anchored = true
	o136.FormFactor = Enum.FormFactor.Custom
	o136.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o136.CFrame = CFrame.new(18.950964, 0.969842017, 14.2187424, 1, -1.0960446e-021, -4.3772161e-008, -7.78546341e-022, 1, -3.58803156e-018, 4.3772161e-008, -5.38120031e-018, 1)
	o136.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o136.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o137.Parent = o136
	o137.Scale = Vector3.new(0.666666687, 0.249999985, 0.74999994)
	o137.MeshType = Enum.MeshType.Wedge
	o138.Parent = o1
	o138.Material = Enum.Material.SmoothPlastic
	o138.BrickColor = BrickColor.new("Black")
	o138.Position = Vector3.new(18.950964, 0.919857979, 14.2271004)
	o138.Rotation = Vector3.new(-0.600734293, 89.980217, -5.99351438e-007)
	o138.Anchored = true
	o138.FormFactor = Enum.FormFactor.Custom
	o138.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o138.CFrame = CFrame.new(18.950964, 0.919857979, 14.2271004, 4.06289615e-008, 4.25005558e-016, 0.99999994, -6.70552254e-008, 0.999999881, 4.68723726e-010, -1.00000012, -9.68575407e-008, 4.47034694e-008)
	o138.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o138.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o139.Parent = o138
	o139.Scale = Vector3.new(0.888888896, 0.249999985, 0.666666687)
	o140.Parent = o1
	o140.Material = Enum.Material.SmoothPlastic
	o140.BrickColor = BrickColor.new("Black")
	o140.Position = Vector3.new(18.950964, 1.17262495, 14.2539701)
	o140.Rotation = Vector3.new(30.0000038, 1.24663654e-006, -90)
	o140.Anchored = true
	o140.FormFactor = Enum.FormFactor.Custom
	o140.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o140.CFrame = CFrame.new(18.950964, 1.17262495, 14.2539701, -4.959292e-008, 1, 2.17579128e-008, -0.866025388, -3.19989653e-008, -0.50000006, -0.50000006, -4.36557457e-008, 0.866025388)
	o140.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o140.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o141.Parent = o140
	o141.Scale = Vector3.new(0.194444433, 0.416666687, 0.194444433)
	o142.Parent = o1
	o142.Material = Enum.Material.SmoothPlastic
	o142.BrickColor = BrickColor.new("Really black")
	o142.Position = Vector3.new(18.950964, 1.10038495, 14.3182096)
	o142.Rotation = Vector3.new(3.08320072e-016, 90, 0)
	o142.Anchored = true
	o142.FormFactor = Enum.FormFactor.Custom
	o142.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o142.CFrame = CFrame.new(18.950964, 1.10038495, 14.3182096, 0, -2.98023295e-008, 1, 5.38120031e-018, 1, 2.98023295e-008, -1, -1.91260039e-018, 0)
	o142.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o142.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o143.Parent = o142
	o143.Scale = Vector3.new(0.027777778, 0.722222269, 0.388888866)
	o144.Parent = o1
	o144.Material = Enum.Material.SmoothPlastic
	o144.BrickColor = BrickColor.new("Black")
	o144.Position = Vector3.new(18.950964, 0.986526012, 14.2826424)
	o144.Rotation = Vector3.new(3.08320072e-016, 0, 6.27987314e-020)
	o144.Anchored = true
	o144.FormFactor = Enum.FormFactor.Custom
	o144.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
	o144.CFrame = CFrame.new(18.950964, 0.986526012, 14.2826424, 1, -1.0960446e-021, 0, -1.0960446e-021, 1, -5.38120031e-018, 0, -5.38120031e-018, 1)
	o144.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o144.Color = Color3.new(0.105882, 0.164706, 0.207843)
	o145.Parent = o144
	o145.Scale = Vector3.new(0.666666687, 0.416666687, 0.333333343)
	o145.MeshType = Enum.MeshType.Wedge
	o146.Parent = o1
	o146.Material = Enum.Material.SmoothPlastic
	o146.BrickColor = BrickColor.new("Really black")
	o146.Position = Vector3.new(18.950964, 0.872651994, 14.2770796)
	o146.Rotation = Vector3.new(2.18855899e-013, 2.50129006e-006, 180)
	o146.Anchored = true
	o146.FormFactor = Enum.FormFactor.Custom
	o146.Size = Vector3.new(0.200000003, 0.200000003, 0.211111099)
	o146.CFrame = CFrame.new(18.950964, 0.872651994, 14.2770796, -1, -8.74227766e-008, 4.36557457e-008, 8.74227766e-008, -1, -3.81975606e-015, 4.36557457e-008, 6.83386182e-018, 1)
	o146.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o146.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o147.Parent = o146
	o147.Scale = Vector3.new(0.666666687, 0.277777761, 1)
	o147.MeshType = Enum.MeshType.Wedge
	o148.Name = "Handle"
	o148.Parent = o1
	o148.Material = Enum.Material.SmoothPlastic
	o148.BrickColor = BrickColor.new("Really black")
	o148.Transparency = 1
	o148.Position = Vector3.new(18.9506321, 0.598004997, 14.4106464)
	o148.Rotation = Vector3.new(180, -2.50129006e-006, 180)
	o148.Anchored = true
	o148.FormFactor = Enum.FormFactor.Custom
	o148.Size = Vector3.new(0.200000003, 0.205555543, 0.200000003)
	o148.CFrame = CFrame.new(18.9506321, 0.598004997, 14.4106464, -1, -1.0960446e-021, -4.36557457e-008, 1.41269847e-021, 1, -1.6144448e-018, 4.36557457e-008, -5.38120031e-018, -1)
	o148.BackSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.RightSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	o148.Color = Color3.new(0.0666667, 0.0666667, 0.0666667)
	o149.Name = "FireSound"
	o149.Parent = o148
	o149.SoundId = "rbxassetid://330704232"
	o149.Volume = 10
	o150.Parent = o148
	o150.Scale = Vector3.new(0.99999994, 1, 0.99999994)
	Victim = game.Players.LocalPlayer.Character
	function Suicide ()
		Victim.Torso.Neck.C0 = CFrame.new(0,1.5,0) * CFrame.Angles(math.rad(25), -math.rad(0),-math.rad(0))
		Victim.Torso.Neck.C1 = CFrame.new(0,0,0)
		wait(.02)
		Victim.Torso["Right Shoulder"].C0 = CFrame.new(2.3,.5,0) * CFrame.Angles(math.rad(-90), -math.rad(160),-math.rad(-70))
		Victim.Torso["Right Shoulder"].C1 = CFrame.new(0,0,0)
		ANGLE = -70
		ANGLE2 = -20
		for i=1,7 do
			ANGLE = ANGLE + 10
			ANGLE2 = ANGLE2 + 10
			Victim.Torso["Right Shoulder"].C0 = CFrame.new(2.3,.5,0) * CFrame.Angles(math.rad(-90), -math.rad(160),-math.rad(ANGLE))
			Victim.Torso["Right Shoulder"].C1 = CFrame.new(0,0,0)
			wait(1/30)
		end
		wait(.3)
		o1.Handle.FireSound.Parent = workspace
		workspace.FireSound:Play()
		game.Players.LocalPlayer.Character.Humanoid.Health = 0
		game.Players.LocalPlayer.Character.Head.BrickColor = BrickColor.new("Maroon")
		player = game.Players[Victim.Name]
		char = player.Character
		char.Archivable = true
		local rg = char:Clone()
		rg.HumanoidRootPart:Destroy()
		rg.Name = ""
		rg.Humanoid.MaxHealth = 0

		for i, v in pairs(rg.Torso:GetChildren()) do
			if v:IsA("Glue") or v:IsA("Motor6D") then
				v:Destroy()
			end
		end

		local n = Instance.new("Glue", rg.Torso)
		n.Name = "Neck"
		n.Part0 = rg.Torso
		n.Part1 = rg.Head
		n.C0 = CFrame.new(0, 1, 0)
		n.C1 = CFrame.new(0, -0.5, 0)


		local rs = Instance.new("Glue", rg.Torso)
		rs.Name = "Right Shoulder"
		rs.Part0 = rg.Torso
		rs.Part1 = rg["Right Arm"]
		rs.C0 = CFrame.new(1.5, 0.5, 0)
		rs.C1 = CFrame.new(0, 0.5, 0)
		local ls = Instance.new("Glue", rg.Torso)
		ls.Name = "Left Shoulder"
		ls.Part0 = rg.Torso
		ls.Part1 = rg["Left Arm"]
		ls.C0 = CFrame.new(-1.5, 0.5, 0)
		ls.C1 = CFrame.new(0, 0.5, 0)

		local rh = Instance.new("Glue", rg.Torso)
		rh.Name = "Right Hip"
		rh.Part0 = rg.Torso
		rh.Part1 = rg["Right Leg"]
		rh.C0 = CFrame.new(0.5, -1, 0)
		rh.C1 = CFrame.new(0, 1, 0)
		local lh = Instance.new("Glue", rg.Torso)
		lh.Name = "Left Hip"
		lh.Part0 = rg.Torso
		lh.Part1 = rg["Left Leg"]
		lh.C0 = CFrame.new(-0.5, -1, 0)
		lh.C1 = CFrame.new(0, 1, 0)
		char.Torso:Destroy()
		char.Head:Destroy()
		char["Left Leg"]:Destroy()
		char["Left Arm"]:Destroy()
		char["Right Leg"]:Destroy()
		char["Right Arm"]:Destroy()
		rg.Parent = game.Workspace
		rg.Head.BrickColor = BrickColor.new("Maroon")
		rg.Torso.Neck:Destroy()
		for i, v in pairs(rg.Torso:GetChildren()) do
			if v:IsA("Motor6D") then
				v:Destroy()
			end
		end
		function DEATH ()
			OHHNELLY = Instance.new("Part")
			OHHNELLY.Parent = rg
			OHHNELLY.Anchored = false
			OHHNELLY.Material = Enum.Material.SmoothPlastic
			OHHNELLY.BrickColor = BrickColor.new("Maroon")
			OHHNELLY.Size = Vector3.new(0.200000003, 0.200000003, 0.200000003)
			OHHNELLY.Position = rg.Head.Position
			OHHNELLY.Color = Color3.new(0.458824, 0, 0)
			OHHNELLY.BackSurface = Enum.SurfaceType.SmoothNoOutlines
			OHHNELLY.BottomSurface = Enum.SurfaceType.SmoothNoOutlines
			OHHNELLY.FrontSurface = Enum.SurfaceType.SmoothNoOutlines
			OHHNELLY.LeftSurface = Enum.SurfaceType.SmoothNoOutlines
			OHHNELLY.RightSurface = Enum.SurfaceType.SmoothNoOutlines
			OHHNELLY.TopSurface = Enum.SurfaceType.SmoothNoOutlines
		end
		for i=1, 10 do
			DEATH()
			print"BLOODY"
			wait()
		end
	end
	function Weld(x,y)
		local W = Instance.new("Weld")
		W.Part0 = x
		W.Part1 = y
		local CJ = CFrame.new(x.Position)
		local C0 = x.CFrame:inverse()*CJ
		local C1 = y.CFrame:inverse()*CJ
		W.C0 = C0
		W.C1 = C1
		W.Parent = x
	end

	function Get(A)
		if A.className == "Part" then
			Weld(o1.Handle, A)
			A.Anchored = false
		else
			local C = A:GetChildren()
			for i=1, #C do
				Get(C[i])
			end
		end
	end

	function Finale()
		Get(o1)
	end

	o1.Equipped:connect(Finale)
	o1.Unequipped:connect(Finale)
	o1.Activated:connect(Suicide)
	Finale()
end)

solar.Name = "solar"
solar.Parent = ScrollingFrame
solar.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
solar.BorderColor3 = Color3.fromRGB(0, 0, 0)
solar.Position = UDim2.new(0.5, 0, 0.629263461, 0)
solar.Size = UDim2.new(0, 109, 0, 51)
solar.Font = Enum.Font.Cartoon
solar.Text = "SolarHUB"
solar.TextColor3 = Color3.fromRGB(255, 64, 245)
solar.TextSize = 29.000
solar.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/Solara%20Hub%20v3.lua"))()
end)

ctrltp.Name = "ctrltp"
ctrltp.Parent = ScrollingFrame
ctrltp.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
ctrltp.BorderColor3 = Color3.fromRGB(0, 0, 0)
ctrltp.Position = UDim2.new(0.060283687, 0, 0.635526419, 0)
ctrltp.Size = UDim2.new(0, 113, 0, 51)
ctrltp.Font = Enum.Font.Cartoon
ctrltp.Text = "ctrl TP"
ctrltp.TextColor3 = Color3.fromRGB(135, 243, 255)
ctrltp.TextSize = 29.000
ctrltp.TextWrapped = true
ctrltp.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://obj.wearedevs.net/2/scripts/Click%20Teleport.lua"))()
end)

jerkr15.Name = "jerkr15"
jerkr15.Parent = ScrollingFrame
jerkr15.BackgroundColor3 = Color3.fromRGB(171, 26, 255)
jerkr15.BorderColor3 = Color3.fromRGB(0, 0, 0)
jerkr15.Position = UDim2.new(0.5, 0, 0.767180026, 0)
jerkr15.Size = UDim2.new(0, 109, 0, 51)
jerkr15.Font = Enum.Font.Cartoon
jerkr15.Text = "Jerkoff (r15)"
jerkr15.TextColor3 = Color3.fromRGB(255, 255, 255)
jerkr15.TextScaled = true
jerkr15.TextSize = 29.000
jerkr15.TextWrapped = true
jerkr15.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://pastefy.app/YZoglOyJ/raw"))()
end)


jerkr6.Name = "jerkr6"
jerkr6.Parent = ScrollingFrame
jerkr6.BackgroundColor3 = Color3.fromRGB(10, 137, 255)
jerkr6.BorderColor3 = Color3.fromRGB(0, 0, 0)
jerkr6.Position = UDim2.new(0.060283687, 0, 0.78123188, 0)
jerkr6.Size = UDim2.new(0, 113, 0, 51)
jerkr6.Font = Enum.Font.Cartoon
jerkr6.Text = "Jerkoff (R6)"
jerkr6.TextColor3 = Color3.fromRGB(255, 255, 255)
jerkr6.TextScaled = true
jerkr6.TextSize = 29.000
jerkr6.TextWrapped = true
jerkr6.MouseButton1Down:connect(function()
	loadstring(game:HttpGet("https://pastefy.app/wa3v2Vgm/raw"))()
end)


Open.Name = "Open"
Open.Parent = ScreenGui
Open.BackgroundColor3 = Color3.fromRGB(205, 56, 255)
Open.BackgroundTransparency = 0.250
Open.BorderColor3 = Color3.fromRGB(27, 42, 53)
Open.Position = UDim2.new(0.916051567, 0, 0.959843278, 0)
Open.Size = UDim2.new(0, 82, 0, 19)
Open.Font = Enum.Font.Cartoon
Open.Text = "Open "
Open.TextColor3 = Color3.fromRGB(255, 255, 255)
Open.TextScaled = true
Open.TextSize = 14.000
Open.TextWrapped = true
local UserInputService = game:GetService('UserInputService')

local frame = Open

local leadFrame = Instance.new('Frame') do
	leadFrame.AnchorPoint = frame.AnchorPoint
	leadFrame.Position = frame.Position
	leadFrame.Size = frame.Size
	leadFrame.Name = `Lead {frame.Name}`
	leadFrame.Visible = false
	leadFrame.Parent = frame.Parent
end

local screenGui = frame:FindFirstAncestorOfClass('ScreenGui')

local inputChanged = nil
local inputEnded = nil

local function getBoundsRelations(guiObject : GuiObject)
	local bounds = screenGui.AbsoluteSize
	local topLeft = screenGui.IgnoreGuiInset and guiObject.AbsolutePosition + Vector2.new(0, 36) or guiObject.AbsolutePosition
	local bottomRight = topLeft + guiObject.AbsoluteSize

	local boundRelations = {
		Top = topLeft.Y < 0 and math.abs(topLeft.Y) or nil,
		Left = topLeft.X < 0 and math.abs(topLeft.X) or nil,
		Right = bottomRight.X > bounds.X and math.abs(bottomRight.X - bounds.X) or nil,
		Bottom = bottomRight.Y > bounds.Y and math.abs(bottomRight.Y - bounds.Y) or nil,
	}

	return (not boundRelations.Top
		and not boundRelations.Bottom
		and not boundRelations.Left
		and not boundRelations.Right), boundRelations
end

frame.InputBegan:Connect(function(inputObject : InputObject)
	if inputObject.UserInputType == Enum.UserInputType.MouseButton1 then

		local lastMousePosition = UserInputService:GetMouseLocation()
		local goalPosition = frame.Position

		inputChanged = UserInputService.InputChanged:Connect(function(input : InputObject, event : boolean)
			if input.UserInputType == Enum.UserInputType.MouseMovement then
				local currentMousePosition = UserInputService:GetMouseLocation()
				local mouseDelta = currentMousePosition - lastMousePosition

				goalPosition += UDim2.fromOffset(mouseDelta.X, mouseDelta.Y)

				leadFrame.Position = goalPosition

				local isInBounds, relations = getBoundsRelations(leadFrame)

				if not isInBounds then
					local x = (relations.Left or 0) - (relations.Right or 0)
					local y = (relations.Top or 0) - (relations.Bottom or 0)

					goalPosition += UDim2.fromOffset(x, y)
				end

				frame.Position = goalPosition
				lastMousePosition = currentMousePosition
			end
		end)

		inputEnded = frame.InputEnded:Connect(function(input : InputObject)
			if input.UserInputType == Enum.UserInputType.MouseButton1 then
				inputChanged:Disconnect()
				inputChanged = nil

				inputEnded:Disconnect()
				inputEnded = nil
			end
		end)
	end
end)

frame.Destroying:Once(function()

	leadFrame = leadFrame:Destroy()

	if inputChanged  then
		inputChanged:Disconnect()
		inputChanged = nil
	end

	if inputEnded then
		inputEnded:Disconnect()
		inputEnded = nil
	end
end)

-- Scripts:

local function TDRUA_fake_script() -- Close.Closing 
	local script = Instance.new('LocalScript', Close)

	local Frame = script.Parent.Parent
	
	script.Parent.MouseButton1Click:Connect(function()
		Frame.Visible = false
	end)
end
coroutine.wrap(TDRUA_fake_script)()
local function IQRVX_fake_script() -- Open.Opening 
	local script = Instance.new('LocalScript', Open)

	local Frame = script.Parent.Parent.Frame
	
	script.Parent.MouseButton1Click:Connect(function()
		Frame.Visible = true
	end)
end
coroutine.wrap(IQRVX_fake_script)()
