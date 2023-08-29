local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local gui = Instance.new("ScreenGui")
gui.Name = "PlayerButtonsGui"
gui.Parent = game:GetService("CoreGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 300, 0, 400)
frame.Position = UDim2.new(0, 10, 0, 10)
frame.BackgroundColor3 = Color3.fromRGB(53, 53, 53)
frame.BorderColor3 = Color3.fromRGB(34, 34, 34)
frame.Active = true
frame.Draggable = true
frame.Parent = gui

local closeButton = Instance.new("TextButton")
closeButton.Size = UDim2.new(0, 20, 0, 20)
closeButton.Position = UDim2.new(0, 5, 0, 5)
closeButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
closeButton.Text = "X"
closeButton.Parent = frame

local minimizeButton = Instance.new("TextButton")
minimizeButton.Size = UDim2.new(0, 20, 0, 20)
minimizeButton.Position = UDim2.new(1, -25, 0, 5)
minimizeButton.BackgroundColor3 = Color3.fromRGB(255, 102, 102)
minimizeButton.Text = "-"
minimizeButton.Parent = frame

local scrollingFrame = Instance.new("ScrollingFrame")
scrollingFrame.Size = UDim2.new(1, -10, 1, -30)
scrollingFrame.Position = UDim2.new(0, 5, 0, 25)
scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
scrollingFrame.Parent = frame
scrollingFrame.BackgroundTransparency = 1

local listLayout = Instance.new("UIListLayout")
listLayout.Padding = UDim.new(0, 5)
listLayout.HorizontalAlignment = Enum.HorizontalAlignment.Left
listLayout.VerticalAlignment = Enum.VerticalAlignment.Top
listLayout.Parent = scrollingFrame

local function teleportPart(targetPart)
    LocalPlayer.Character.HumanoidRootPart.CFrame = targetPart.CFrame
end

local function createButton(part)
    local button = Instance.new("TextButton")
    button.Size = UDim2.new(0.9, 0, 0, 20)
    button.BackgroundColor3 = Color3.fromRGB(34, 139, 34)
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.Font = Enum.Font.Gotham
    button.TextSize = 12
    local fullName = part:GetFullName()
    button.Text = part.Name.." ("..fullName..")"
    button.TextWrapped = true
    button.TextXAlignment = Enum.TextXAlignment.Left
    button.Parent = scrollingFrame

    button.MouseButton1Click:Connect(function()
        teleportPart(part)
    end)
end

for _, part in ipairs(game:GetService("Workspace"):GetDescendants()) do
    if part:IsA("Part") and not part.Parent.Name:find("Character") then
        createButton(part)
    end
end

scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, listLayout.AbsoluteContentSize.Y)

minimizeButton.MouseButton1Click:Connect(function()
    if frame.Size == UDim2.new(0, 300, 0, 400) then
        frame.Size = UDim2.new(0, 30, 0, 30)
        minimizeButton.Text = "+"
        minimizeButton.Position = UDim2.new(1, -25, 0, 5)
    else
        frame.Size = UDim2.new(0, 300, 0, 400)
        minimizeButton.Text = "-"
        minimizeButton.Position = UDim2.new(1, -25, 0, 5)
    end
end)

closeButton.MouseButton1Click:Connect(function()
    gui:Destroy()
end)
