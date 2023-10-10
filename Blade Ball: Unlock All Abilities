local localPlayer = game.Players.LocalPlayer
local character = localPlayer.Character or localPlayer.CharacterAdded:Wait()
local abilitiesFolder = character:WaitForChild("Abilities")

local ChosenAbility = "Raging Deflection"

local function createGUI()
    local screenGui = Instance.new("ScreenGui")
    screenGui.Name = "AbilityChooser"
    screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

    local frame = Instance.new("Frame")
    frame.Size = UDim2.new(0.080, 100, 0.45, 100)
    frame.Position = UDim2.new(0.15, -90, 0.4, -100)
    frame.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)
    frame.BorderSizePixel = 0
    frame.Parent = screenGui

    local isDragging = false
    local dragInput
    local dragStart
    local startPos

    local function update(input)
        local delta = input.Position - dragStart
        frame.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
    end

    frame.InputBegan:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.Touch then
            isDragging = true
            dragStart = input.Position
            startPos = frame.Position

            input.Changed:Connect(function()
                if input.UserInputState == Enum.UserInputState.End then
                    isDragging = false
                end
            end)
        end
    end)

    frame.InputChanged:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.Touch then
            dragInput = input
        end
    end)

    game:GetService("UserInputService").InputChanged:Connect(function(input)
        if input == dragInput and isDragging then
            update(input)
        end
    end)

    local abilities = {"Dash", "Forcefield", "Invisibility", "Platform", "Raging Deflection", "Shadow Step", "Super Jump", "Telekinesis", "Thunder Dash", "Freeze", "Infinity", "Pull", "Rapture", "Phase Bypass", "Waypoint"}
    local buttonHeight = 14
    for i, ability in ipairs(abilities) do
        local button = Instance.new("TextButton")
        button.Size = UDim2.new(1, 0, 0, buttonHeight)
        button.Position = UDim2.new(0, 0, 0, (i - 1) * (buttonHeight + 5))
        button.Text = ability
        button.BackgroundColor3 = Color3.new(0.8, 0.8, 0.8)
        button.BorderColor3 = Color3.new(1, 1, 1)
        button.Parent = frame
        
        button.MouseButton1Click:Connect(function()
            ChosenAbility = ability
        end)
    end
end

local function onCharacterAdded(newCharacter)
    character = newCharacter
    abilitiesFolder = character:WaitForChild("Abilities")
    createGUI()
end

localPlayer.CharacterAdded:Connect(onCharacterAdded)
createGUI()

while task.wait() do
    for _, obj in pairs(abilitiesFolder:GetChildren()) do
        if obj:IsA("LocalScript") then
            if obj.Name == ChosenAbility then
                obj.Disabled = false
            else
                obj.Disabled = true
            end
        end
    end
end
