local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Lunar", "DarkTheme")
local Tab = Window:NewTab("Misc")
local Section = Tab:NewSection("Speed")

Section:NewKeybind("Speed Up", "KeybindInfo", Enum.KeyCode.F, function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 50
end)
Section:NewKeybind("Speed Low", "KeybindInfo", Enum.KeyCode.G, function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 10
end)
local Section = Tab:NewSection("Jump")
Section:NewButton("Inf Jump", "ButtonInfo", function()
    local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
end)
