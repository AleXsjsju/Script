for index, value in pairs(getconnections(game:GetService("Players").LocalPlayer.Idled)) do
value:Disable()
end
local idlepos = 144
while true do
local Character = game:GetService("Players").LocalPlayer.Character
if Character then
local VehicleSeat = Character:FindFirstChildWhichIsA("Humanoid").SeatPart
if VehicleSeat and typeof(VehicleSeat) == "Instance" and VehicleSeat:IsA("VehicleSeat") then
if idlepos >= 144 then
local Vehicle = VehicleSeat:FindFirstAncestorWhichIsA("Model")
Character.Parent = Vehicle
Vehicle:MoveTo(Vector3.new(0, 1e3 * 1.8, 0))
Character.Parent = workspace
idlepos = 0
end
VehicleSeat.CFrame = CFrame.new(VehicleSeat.CFrame.X, 1e3, VehicleSeat.CFrame.Z) * CFrame.fromEulerAnglesXYZ(math.rad(0), math.rad(180), math.rad(0))
VehicleSeat.AssemblyLinearVelocity = VehicleSeat.CFrame.LookVector.Unit * Vector3.new(320, 320, 320) + Vector3.new(100 * math.cos((tick() * 60) / 28), 100 * math.cos((tick() * 60) / -28), 100 * math.cos((tick() * 60) / -28))
VehicleSeat.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
end
end
task.synchronize()
idlepos = idlepos + 1
task.desynchronize()
task.wait(0)
end
