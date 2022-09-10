-- Instances:

-- Made By ElGamer21_YT

local ScreenGui = Instance.new("ScreenGui")
local Home = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Tittle = Instance.new("TextLabel")
local UICorner_2 = Instance.new("UICorner")
local NoClipB = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local SOONB = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local ClickTPB = Instance.new("TextButton")
local UICorner_5 = Instance.new("UICorner")
local BtoolsB = Instance.new("TextButton")
local UICorner_6 = Instance.new("UICorner")
local ExtraB = Instance.new("TextBox")
local UICorner_7 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.CoreGui

Home.Name = "Home"
Home.Parent = ScreenGui
Home.AnchorPoint = Vector2.new(0.5, 0.5)
Home.BackgroundColor3 = Color3.fromRGB(225, 0, 0)
Home.Position = UDim2.new(0.219226241, 0, 0.569259942, 0)
Home.Size = UDim2.new(0, 330, 0, 216)

UICorner.CornerRadius = UDim.new(0.0900000036, 10)
UICorner.Parent = Home

Tittle.Name = "Tittle"
Tittle.Parent = Home
Tittle.AnchorPoint = Vector2.new(0.5, 0.5)
Tittle.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
Tittle.Position = UDim2.new(0.4969697, 0, 0.121359222, 0)
Tittle.Size = UDim2.new(0, 330, 0, 50)
Tittle.Font = Enum.Font.SourceSansBold
Tittle.Text = "Made By - ElGamer21_YT - V1"
Tittle.TextColor3 = Color3.fromRGB(255, 255, 255)
Tittle.TextScaled = true
Tittle.TextSize = 14.000
Tittle.TextWrapped = true

UICorner_2.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_2.Parent = Tittle

NoClipB.Name = "NoClipB"
NoClipB.Parent = Home
NoClipB.AnchorPoint = Vector2.new(0.5, 0.5)
NoClipB.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
NoClipB.Position = UDim2.new(0.257575721, 0, 0.3782233, 0)
NoClipB.Size = UDim2.new(0, 137, 0, 34)
NoClipB.Font = Enum.Font.SourceSansBold
NoClipB.Text = "NoClip"
NoClipB.TextColor3 = Color3.fromRGB(255, 255, 255)
NoClipB.TextScaled = true
NoClipB.TextSize = 14.000
NoClipB.TextWrapped = true


NoClipB.MouseButton1Down:connect(function()
	local noclipplayer = game:GetService("Players").LocalPlayer
	local noclipmouse = noclipplayer:GetMouse()

	local donoclip = false
	local noclip = false

	function b_noclip(key)
		if (key == "b") then
			if noclip == false then
				donoclip = true

				noclip = true
			elseif noclip == true then
				donoclip = false

				noclip = false
			end
		end
	end

	noclipmouse.KeyDown:connect(b_noclip)

	game:GetService("Players").LocalPlayer.Character.Head.Touched:connect(function(obj)
		if obj ~= workspace.Terrain then
			if donoclip == true then
				obj.CanCollide = false
			else
				obj.CanCollide = true
			end
		end
	end)
end)

UICorner_3.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_3.Parent = NoClipB

SOONB.Name = "SOON!B"
SOONB.Parent = Home
SOONB.AnchorPoint = Vector2.new(0.5, 0.5)
SOONB.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
SOONB.Position = UDim2.new(0.721212089, 0, 0.616087377, 0)
SOONB.Size = UDim2.new(0, 137, 0, 34)
SOONB.Font = Enum.Font.SourceSansBold
SOONB.Text = "SOON!"
SOONB.TextColor3 = Color3.fromRGB(255, 255, 255)
SOONB.TextScaled = true
SOONB.TextSize = 14.000
SOONB.TextWrapped = true

UICorner_4.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_4.Parent = SOONB

ClickTPB.Name = "ClickTPB"
ClickTPB.Parent = Home
ClickTPB.AnchorPoint = Vector2.new(0.5, 0.5)
ClickTPB.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
ClickTPB.Position = UDim2.new(0.721212089, 0, 0.3782233, 0)
ClickTPB.Size = UDim2.new(0, 137, 0, 34)
ClickTPB.Font = Enum.Font.SourceSansBold
ClickTPB.Text = "Click TP"
ClickTPB.TextColor3 = Color3.fromRGB(255, 255, 255)
ClickTPB.TextScaled = true
ClickTPB.TextSize = 14.000
ClickTPB.TextWrapped = true


ClickTPB.MouseButton1Down:connect(function()
	mouse = game.Players.LocalPlayer:GetMouse()
	tool = Instance.new("Tool")
	tool.RequiresHandle = false
	tool.Name = "Click Teleport"
	tool.Activated:connect(function()
		local pos = mouse.Hit+Vector3.new(0,2.5,0)
		pos = CFrame.new(pos.X,pos.Y,pos.Z)
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
	end)
	tool.Parent = game.Players.LocalPlayer.Backpack
end)

UICorner_5.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_5.Parent = ClickTPB

BtoolsB.Name = "BtoolsB"
BtoolsB.Parent = Home
BtoolsB.AnchorPoint = Vector2.new(0.5, 0.5)
BtoolsB.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
BtoolsB.Position = UDim2.new(0.257575721, 0, 0.616087377, 0)
BtoolsB.Size = UDim2.new(0, 137, 0, 34)
BtoolsB.Font = Enum.Font.SourceSansBold
BtoolsB.Text = "Btools"
BtoolsB.TextColor3 = Color3.fromRGB(255, 255, 255)
BtoolsB.TextScaled = true
BtoolsB.TextSize = 14.000
BtoolsB.TextWrapped = true


BtoolsB.MouseButton1Down:connect(function()
	a = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
	a.BinType = 2
	b = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
	b.BinType = 3
	c = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
	c.BinType = 4
end)

UICorner_6.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_6.Parent = BtoolsB

ExtraB.Name = "ExtraB"
ExtraB.Parent = Home
ExtraB.BackgroundColor3 = Color3.fromRGB(97, 0, 0)
ExtraB.Position = UDim2.new(-0.00303030293, 0, 0.841963291, 0)
ExtraB.Size = UDim2.new(0, 329, 0, 34)
ExtraB.Font = Enum.Font.SourceSansBold
ExtraB.Text = "Thanks For Use!!!"
ExtraB.TextColor3 = Color3.fromRGB(255, 255, 255)
ExtraB.TextScaled = true
ExtraB.TextSize = 14.000
ExtraB.TextWrapped = true

UICorner_7.CornerRadius = UDim.new(0.0900000036, 10)
UICorner_7.Parent = ExtraB
