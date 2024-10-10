local Mercury = loadstring(game:HttpGet("https://raw.githubusercontent.com/deeeity/mercury-lib/master/src.lua"))()

local GUI = Mercury:Create{
    Name = "Lheny hub",
    Size = UDim2.fromOffset(480, 340),
    Theme = Mercury.Themes.Dark,
    Link = "https://github.com/deeeity/mercury-lib"
}
local Tab = GUI:Tab{
	Name = "New Tab",
	Icon = "rbxassetid://8569322835"
}

Tab:Button{
	Name = "Walkspeed 500",
	Description = nil,
	Callback = function()local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Set the desired walk speed
local desiredWalkSpeed = 500  -- Change this value to your preferred speed

humanoid.WalkSpeed = desiredWalkSpeed

-- Optional: Reset to default speed on respawn
player.CharacterAdded:Connect(function(newCharacter)
    humanoid = newCharacter:WaitForChild("Humanoid")
    humanoid.WalkSpeed = desiredWalkSpeed
end)
  end
}    

Tab:Button{
	Name = "Walkspeed 50",
	Description = nil,
	Callback = function()local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Set the desired walk speed
local desiredWalkSpeed = 50  -- Change this value to your preferred speed

humanoid.WalkSpeed = desiredWalkSpeed

-- Optional: Reset to default speed on respawn
player.CharacterAdded:Connect(function(newCharacter)
    humanoid = newCharacter:WaitForChild("Humanoid")
    humanoid.WalkSpeed = desiredWalkSpeed
end)
 end
}
