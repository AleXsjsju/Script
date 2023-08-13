local connections = getgenv().configs and getgenv().configs.connection
if connections then
    local Disable = configs.Disable
    for i,v in connections do
        v:Disconnect() 
    end
    Disable:Fire()
    Disable:Destroy()
    table.clear(configs)
end

local Disable = Instance.new("BindableEvent")
getgenv().configs = {
    connections = {},
    Disable = Disable,
    Size = Vector3.new(10,10,10),
    DeathCheck = true
}

local Players = cloneref(game:GetService("Players"))
local RunService = cloneref(game:GetService("RunService"))
local lp = Players.LocalPlayer
local Run = true
local Ignorelist = OverlapParams.new()
Ignorelist.FilterType = Enum.RaycastFilterType.Include

local function getchar(plr)
    local plr = plr or lp
    return plr.Character
end

local function gethumanoid(plr: Player | Character)
    local char = plr:IsA("Model") and plr or getchar(plr)

    if char then
        return char:FindFirstChildWhichIsA("Humanoid")
    end
end

local function IsAlive(Humanoid)
    return Humanoid and Humanoid.Health > 0
end

local function GetTouchInterest(Tool)
    return Tool and Tool:FindFirstChildWhichIsA("TouchTransmitter",true)
end

local function GetCharacters(LocalPlayerChar)
    local Characters = {}
    for i,v in Players:GetPlayers() do
        table.insert(Characters,getchar(v))
    end
    table.remove(Characters,table.find(Characters,LocalPlayerChar))
    return Characters
end

local function Attack(Tool,TouchPart,ToTouch)
    if Tool:IsDescendantOf(workspace) then
        Tool:Activate()
        firetouchinterest(TouchPart,ToTouch,1)
        firetouchinterest(TouchPart,ToTouch,0)
    end
end

table.insert(getgenv().configs.connections,Disable.Event:Connect(function()
    Run = false
end))

while Run do
    local char = getchar()
    if IsAlive(gethumanoid(char)) then
        local Tool = char and char:FindFirstChildWhichIsA("Tool")
        local TouchInterest = Tool and GetTouchInterest(Tool)

        if TouchInterest then
            local TouchPart = TouchInterest.Parent
            local Characters = GetCharacters(char)
            Ignorelist.FilterDescendantsInstances = Characters
            local InstancesInBox = workspace:GetPartBoundsInBox(TouchPart.CFrame,TouchPart.Size + getgenv().configs.Size,Ignorelist)

            for i,v in InstancesInBox do
                local Character = v:FindFirstAncestorWhichIsA("Model")

                if table.find(Characters,Character) then
                    if getgenv().configs.DeathCheck then                    
                        if IsAlive(gethumanoid(Character)) then
                            Attack(Tool,TouchPart,v)
                        end
                    else
                        Attack(Tool,TouchPart,v)
                    end
                end
            end
        end
    end
    RunService.Heartbeat:Wait()
end
