# Farm
local player = game:GetService("Players").LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
local location = game:GetService("Workspace"):WaitForChild("Finish"):WaitForChild("Chest")
 
-- You can delete this if you want
if not character and humanoidRootPart and location then
    game:GetService("StarterGui"):SetCore("SendNotification",{
    Title = "Note",
    Text = "The script doesnt work, parts are missing",
    Icon = "rbxassetid://111491696505833"
})
end
-- [{LOOP CONDITION}]
_G.works = true --set to false if you want to stop
 
-- [{AutoFarm}]
while _G.works do
    humanoidRootPart.CFrame = location.CFrame
    wait(5) --if lower than 5 it can be a little glitchy
end
