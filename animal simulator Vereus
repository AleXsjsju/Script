-----------//VEREUS\\-----------
--[[Movelist
Q = The reverse penance stare,
E = Doom Pillars
T = Unleashed evil ball
Y = The hunt is on
Z = CRAZY XESTER SWITCH!!!
X = Re_*101011Dact/^ed.exe
---------]]

--To get this shit out of the way, this is NOT a edit of void boss, it was a little project of mine to see how easy it was to animate 2 hands and a head.--
--Also stop calling this void boss v2, void boss switcher or any other name you come up with.--
--I'm not proud of this project however, having a script this powerful is uncreative and boring + that's what skids care about anyway.--
--Alright enjoy it guys please do not abuse the shit out of this.--

Player=game:GetService("Players").LocalPlayer
Character=Player.Character
Character.Humanoid.Name = "vereus"
hum = Character.vereus
LeftArm=Character["Left Arm"]
LeftLeg=Character["Left Leg"]
RightArm=Character["Right Arm"]
RightLeg=Character["Right Leg"]
Root=Character["HumanoidRootPart"]
Head=Character["Head"]
Torso=Character["Torso"]
Neck=Torso["Neck"]
attacking = false
snoring = false
laughing = false
taim = nil
secondform = false
change = 0
xester = false
rachjumper = false
ws = 92
hpheight = 5
huntdown = false
visualizer = false
jumpscared = false
appi = false
stoplev = false
tauntdebounce = false
allowlev = true
MseGuide = true
position = nil
levitate = false
mouse = Player:GetMouse()
settime = 0
sine = 0
t = 0
dgs = 75
RunSrv = game:GetService("RunService")
RenderStepped = game:GetService("RunService").RenderStepped
removeuseless = game:GetService("Debris")
smoothen = game:GetService("TweenService")
randomcolortable={"Cyan","Really red","Cyan","Royal purple","Lime green","Crimson","Daisy yellow","Eggplant"}
random = #randomcolortable
smoothen = game:GetService("TweenService")
local dmt2 = {143536946,2858940717}
local laughs = {2011349649,2011349983,2011351501,2011352223,2011355991,2011356475}
local soundtable2 = {2616767970,2614901458,2616891279,2614896603,2616768521,2616848595,2614905967,2614918002,2563244734,2563244134,2563244444,2563244999,2563245407,2563654940,2563656758,2563658474,2563659001}
laugh = #laughs

local HEADLERP = Instance.new("ManualWeld")
HEADLERP.Parent = Head
HEADLERP.Part0 = Head
HEADLERP.Part1 = Head
HEADLERP.C0 = CFrame.new(0, -1.5, -.5) * CFrame.Angles(math.rad(30), math.rad(0), math.rad(0))

local TORSOLERP = Instance.new("ManualWeld")
TORSOLERP.Parent = Root
TORSOLERP.Part0 = Torso
TORSOLERP.C0 = CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local ROOTLERP = Instance.new("ManualWeld")
ROOTLERP.Parent = Root
ROOTLERP.Part0 = Root
ROOTLERP.Part1 = Torso
ROOTLERP.C0 = CFrame.new(0, 0, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local RIGHTARMLERP = Instance.new("ManualWeld")
RIGHTARMLERP.Parent = RightArm
RIGHTARMLERP.Part0 = RightArm
RIGHTARMLERP.Part1 = Torso
RIGHTARMLERP.C0 = CFrame.new(-1.5, 0, -0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local LEFTARMLERP = Instance.new("ManualWeld")
LEFTARMLERP.Parent = LeftArm
LEFTARMLERP.Part0 = LeftArm
LEFTARMLERP.Part1 = Torso
LEFTARMLERP.C0 = CFrame.new(1.5, 0, -0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local RIGHTLEGLERP = Instance.new("ManualWeld")
RIGHTLEGLERP.Parent = RightLeg
RIGHTLEGLERP.Part0 = RightLeg
RIGHTLEGLERP.Part1 = Torso
RIGHTLEGLERP.C0 = CFrame.new(-0.5, 2, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local LEFTLEGLERP = Instance.new("ManualWeld")
LEFTLEGLERP.Parent = LeftLeg
LEFTLEGLERP.Part0 = LeftLeg
LEFTLEGLERP.Part1 = Torso
LEFTLEGLERP.C0 = CFrame.new(0.5, 2, 0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))

local function weldBetween(a, b)
    local weld = Instance.new("ManualWeld", a)
    weld.Part0 = a
    weld.Part1 = b
    weld.C0 = a.CFrame:inverse() * b.CFrame
    return weld
end

function MAKETRAIL(PARENT,POSITION1,POSITION2,LIFETIME,COLOR)
A = Instance.new("Attachment", PARENT)
A.Position = POSITION1
A.Name = "A"
B = Instance.new("Attachment", PARENT)
B.Position = POSITION2
B.Name = "B"
tr1 = Instance.new("Trail", PARENT)
tr1.Attachment0 = A
tr1.Attachment1 = B
tr1.Enabled = true
tr1.Lifetime = LIFETIME
tr1.TextureMode = "Static"
tr1.LightInfluence = 0
tr1.Color = COLOR
tr1.Transparency = NumberSequence.new(0, 1)
end

coroutine.wrap(function()
while wait() do
hum.WalkSpeed = ws
end
end)()
godmode = coroutine.wrap(function()
for i,v in pairs(Character:GetChildren()) do
if v:IsA("BasePart") and v ~= Root then
v.Anchored = false
end
end
while true do
hum.MaxHealth = math.huge
wait(0.0000001)
hum.Health = math.huge
wait()
end
end)
godmode()
ff = Instance.new("ForceField", Character)
ff.Visible = false

coroutine.wrap(function()
for i,v in pairs(Character:GetChildren()) do
if v.Name == "Animate" then v:Remove()
end
end
end)()

for _,x in pairs(Character:GetChildren()) do
if x:IsA("Decal") then x:Remove() end
end

function damagealll(Radius,Position)		
	local Returning = {}		
	for _,v in pairs(workspace:GetChildren()) do		
		if v~=Character and v:FindFirstChildOfClass('Humanoid') and v:FindFirstChild('Torso') or v:FindFirstChild('UpperTorso') then
if v:FindFirstChild("Torso") then		
			local Mag = (v.Torso.Position - Position).magnitude		
			if Mag < Radius then		
				table.insert(Returning,v)		
			end
elseif v:FindFirstChild("UpperTorso") then	
			local Mag = (v.UpperTorso.Position - Position).magnitude		
			if Mag < Radius then		
				table.insert(Returning,v)		
			end
end	
		end		
	end		
	return Returning		
end

ArtificialHB = Instance.new("BindableEvent", script)
ArtificialHB.Name = "Heartbeat"
script:WaitForChild("Heartbeat")

frame = 1 / 60
tf = 0
allowframeloss = false
tossremainder = false


lastframe = tick()
script.Heartbeat:Fire()


game:GetService("RunService").Heartbeat:connect(function(s, p)
	tf = tf + s
	if tf >= frame then
		if allowframeloss then
			script.Heartbeat:Fire()
			lastframe = tick()
		else
			for i = 1, math.floor(tf / frame) do
				script.Heartbeat:Fire()
			end
			lastframe = tick()
		end
		if tossremainder then
			tf = 0
		else
			tf = tf - frame * math.floor(tf / frame)
		end
	end
end)

function swait(num)
	if num == 0 or num == nil then
		game:service("RunService").Stepped:wait(0)
	else
		for i = 0, num do
			game:service("RunService").Stepped:wait(0)
		end
	end
end

for i,v in pairs(Root.Parent:GetDescendants()) do if v:IsA("Part") then v.Transparency = 1 end end

id = "rbxassetid://2858940717"


dmt2random = dmt2[math.random(1,#dmt2)]
doomtheme = Instance.new("Sound", Torso)
doomtheme.Volume = 4
doomtheme.Name = "doomtheme"
doomtheme.Looped = true
doomtheme.SoundId = "rbxassetid://"..dmt2random
if doomtheme.SoundId == "rbxassetid://2858940717" then
doomtheme.Pitch = .49
else
doomtheme.Pitch = 1
end
doomtheme:Play()


Torso.ChildRemoved:connect(function(removed)
if removed.Name == "doomtheme" then
if xester then
doomtheme = Instance.new("Sound",Torso)
doomtheme.Volume = 4
doomtheme.Name = "doomtheme"
doomtheme.Looped = true
doomtheme.SoundId = "rbxassetid://1382488262"
doomtheme.TimePosition = 20.72
doomtheme:Play()
else
dmt2random = dmt2[math.random(1,#dmt2)]
doomtheme = Instance.new("Sound",Torso)
doomtheme.Volume = 4
doomtheme.Name = "doomtheme"
doomtheme.Looped = true
doomtheme.SoundId = "rbxassetid://"..dmt2random
if doomtheme.SoundId == "rbxassetid://2858940717" then
doomtheme.Pitch = .49
else
doomtheme.Pitch = 1
end
doomtheme:Play()
end
end
end)

function SOUND(PARENT,ID,VOL,LOOP,REMOVE)
local so = Instance.new("Sound")
so.Parent = PARENT
so.SoundId = "rbxassetid://"..ID
so.Volume = VOL
so.Looped = LOOP
so:Play()
removeuseless:AddItem(so,REMOVE)
end

bighead = Instance.new("Part",Torso)
bighead.Size = Vector3.new(1,1,1)
bighead.Anchored = false
bighead.CanCollide = false
bighead.Locked = true
bighead.Size = Vector3.new(4.75, 4.89, 4.77)
bighead.BrickColor = BrickColor.new("Really black")
bighead.CFrame = Head.CFrame
bigheadweld = weldBetween(bighead,Head)
headmesh = Instance.new("SpecialMesh",bighead)
headmesh.MeshType = "Head"
headmesh.Scale = Vector3.new(1.25,1.25,1.25)

mask = Instance.new("Part",Torso)
mask.Size = Vector3.new(.1, 0.39, .1)
mask.Anchored = false
mask.Locked = true
mask.CanCollide = false
mask.BrickColor = BrickColor.new("White")
mask.Material = "Corroded Metal"
maskweld = weldBetween(mask,bighead)
maskweld.C0 = CFrame.new(0,-2.4,0) * CFrame.Angles(math.rad(90),0,0)
maskmesh = Instance.new("SpecialMesh",mask)
maskmesh.MeshId = "rbxassetid://5158270"
maskmesh.TextureId = "rbxassetid://128212042"
maskmesh.Scale = Vector3.new(0.7, 0.5, 0.5)

lightpart1 = Instance.new("Part",Head)
lightpart1.Size = Vector3.new(2.42,2,.516)
lightpart1.Anchored = false
lightpart1.Transparency = 1
lightpart1.BrickColor = BrickColor.new("White")
lightpart1.Material = "Neon"
lightpart1weld = weldBetween(lightpart1,Head)
lightpart1weld.C0 = CFrame.new(0,.9,2.595)

horns = Instance.new("Part",Torso)
horns.Size = Vector3.new(.1,.1,.1)
horns.Material = "Slate"
horns.Locked = true
horns.BrickColor = BrickColor.new("Really black")
horns.CFrame = Head.CFrame * CFrame.new(0,3,0)
hornsmesh = Instance.new("SpecialMesh",horns)
hornsmesh.MeshId = "rbxassetid://434078905"
hornsmesh.Scale = Vector3.new(13,12,12)
hornsweld = weldBetween(horns,bighead)
hornsweld.C0 = CFrame.new(0,-3.3,.82) * CFrame.Angles(math.rad(0),math.rad(180),0)

hand1 = Instance.new("Part",Torso)
hand1.Size = Vector3.new(.1,.1,.1)
hand1.Anchored = false
hand1.Locked = true
hand1.CanCollide = false
hand1.BrickColor = BrickColor.new("White")
hand1.Material = "Slate"
hand1mesh = Instance.new("SpecialMesh",hand1)
hand1mesh.MeshId = "rbxassetid://37241605"
hand1mesh.Scale = Vector3.new(8, 8, 8)
HAND1LERP = weldBetween(hand1,Torso)
HAND1LERP.C0 = CFrame.new(4.5,-5,6) * CFrame.Angles(math.rad(10),math.rad(-5),math.rad(-36))

hand2 = Instance.new("Part",Torso)
hand2.Size = Vector3.new(.1,.1,.1)
hand2.Anchored = false
hand2.CanCollide = false
hand2.Locked = true
hand2.BrickColor = BrickColor.new("White")
hand2.Material = "Slate"
hand2mesh = Instance.new("SpecialMesh",hand2)
hand2mesh.MeshId = "rbxassetid://2899129749"
hand2mesh.Scale = Vector3.new(.8, .8, .8)
HAND2LERP = weldBetween(hand2,Torso)
HAND2LERP.C0 = HAND2LERP.C0:Inverse() * CFrame.new(-5,-5,6) * CFrame.Angles(math.rad(90),math.rad(90),math.rad(95))

mg1 = Instance.new("Part",Torso)
mg1.Anchored = false
mg1.CanCollide = false
mg1.Locked = true
mg1.Size = Vector3.new(4,4,4)
mg1.Shape = "Ball"
mg1.BrickColor = BrickColor.new("Really black")
mg1.Material = "Neon"
mg1.CFrame = hand1.CFrame
mg1weld = weldBetween(mg1,hand1)
mg1weld.C0 = CFrame.new(0,2.7,-4)
blackhole = Instance.new("ParticleEmitter",mg1)
blackhole.Texture = "rbxassetid://258128463"
blackhole.Size = NumberSequence.new(2,2)
blackhole.Rate = 50
blackhole.LockedToPart = true
blackhole.Color = ColorSequence.new(BrickColor.new("Really black").Color,BrickColor.new("Really black").Color)
blackhole.RotSpeed = NumberRange.new(50)
blackhole.Lifetime = NumberRange.new(1)
blackhole.Speed = NumberRange.new(0)

mg2 = Instance.new("Part",Torso)
mg2.Anchored = false
mg2.CanCollide = false
mg2.Shape = "Ball"
mg2.Locked = true
mg2.Size = Vector3.new(4,4,4)
mg2.BrickColor = BrickColor.new("Really black")
mg2.Material = "Neon"
mg2.CFrame = hand2.CFrame
mg2weld = weldBetween(mg2,hand2)
mg2weld.C0 = CFrame.new(0,2.7,-4)
blackhole2 = Instance.new("ParticleEmitter",mg2)
blackhole2.Texture = "rbxassetid://258128463"
blackhole2.Size = NumberSequence.new(2,2)
blackhole2.Rate = 50
blackhole2.Color = ColorSequence.new(BrickColor.new("Really black").Color,BrickColor.new("Really black").Color)
blackhole2.RotSpeed = NumberRange.new(50)
blackhole2.Lifetime = NumberRange.new(1)
blackhole2.LockedToPart = true
blackhole2.Speed = NumberRange.new(0)

slaten = Instance.new("Decal",hand2)
slaten.Texture = "rbxassetid://647441616"
slaten.Color3 = Color3.new(0, 0, 0)
slaten.Face = "Top"

slaten2 = Instance.new("Decal",hand2)
slaten2.Texture = "rbxassetid://647417318"
slaten2.Color3 = Color3.new(0,0,0)
slaten2.Face = "Top"

slatez = Instance.new("Decal",hand1)
slatez.Texture = "rbxassetid://647441616"
slatez.Color3 = Color3.new(0, 0, 0)
slatez.Face = "Top"

slatez2 = Instance.new("Decal",hand1)
slatez2.Texture = "rbxassetid://647417318"
slatez2.Color3 = Color3.new(0,0,0)
slatez2.Face = "Top"

slatez3 = Instance.new("Decal",hand1)
slatez3.Texture = "rbxassetid://647410994"
slatez3.Color3 = Color3.new(1,1,1)
slatez3.Face = "Top"

slatez4 = Instance.new("Decal",hand1)
slatez4.Texture = "rbxassetid://647413967"
slatez4.Color3 = Color3.new(1,1,1)
slatez4.Face = "Top"

slatex = Instance.new("Decal",horns)
slatex.Texture = "rbxassetid://647441616"
slatex.Color3 = Color3.new(0, 0, 0)
slatex.Face = "Top"

slatex2 = Instance.new("Decal",horns)
slatex2.Texture = "rbxassetid://647417318"
slatex2.Color3 = Color3.new(0,0,0)
slatex2.Face = "Top"

slatex3 = Instance.new("Decal",horns)
slatex3.Texture = "rbxassetid://647410994"
slatex3.Color3 = Color3.new(1,1,1)
slatex3.Face = "Top"

slatex4 = Instance.new("Decal",horns)
slatex4.Texture = "rbxassetid://647413967"
slatex4.Color3 = Color3.new(1,1,1)
slatex4.Face = "Top"

slatex5 = Instance.new("Decal",horns)
slatex5.Texture = "rbxassetid://64739326f6"
slatex5.Color3 = Color3.new(1, 1, 1)
slatex5.Face = "Top"

eyeball1 = Instance.new("Part",Torso)
eyeball1.Anchored = false
eyeball1.CanCollide = false
eyeball1.Locked = true
eyeball1.Shape = "Ball"
eyeball1.Material = "Glass"
eyeball1.Size = Vector3.new(3.25, 3.25, 3.25)
eyeball1.BrickColor = BrickColor.new("Really black")
eyeball1weld = weldBetween(eyeball1,Head)
eyeball1weld.C0 = CFrame.new(.6,-.2,1.25)

eyeball2 = Instance.new("Part",Torso)
eyeball2.Anchored = false
eyeball2.CanCollide = false
eyeball2.Shape = "Ball"
eyeball2.Locked = true
eyeball2.Material = "Glass"
eyeball2.Size = Vector3.new(3.25, 3.25, 3.25)
eyeball2.BrickColor = BrickColor.new("Really black")
eyeball2weld = weldBetween(eyeball2,Head)
eyeball2weld.C0 = CFrame.new(-.6,-.2,1.25)

eyeball3 = Instance.new("Part",Torso)
eyeball3.Anchored = false
eyeball3.CanCollide = false
eyeball3.Locked = true
eyeball3.Material = "Neon"
eyeball3.Size = Vector3.new(0.4, 0.4, 0.4)
eyeball3.BrickColor = BrickColor.new("Crimson")
eyeball3mesh = Instance.new("SpecialMesh",eyeball3)
eyeball3mesh.MeshType = "Sphere"
eyeball3weld = weldBetween(eyeball3,Head)
eyeball3weld.C0 = CFrame.new(-1.2,-.3,2.65)

eyeball4 = Instance.new("Part",Torso)
eyeball4.Anchored = false
eyeball4.CanCollide = false
eyeball4.Material = "Neon"
eyeball4.Locked = true
eyeball4.Size = Vector3.new(0.4, 0.4, 0.4)
eyeball4.BrickColor = BrickColor.new("Crimson")
eyeball4mesh = Instance.new("SpecialMesh",eyeball4)
eyeball4mesh.MeshType = "Sphere"
eyeball4weld = weldBetween(eyeball4,Head)
eyeball4weld.C0 = CFrame.new(1.2,-.3,2.65)

coroutine.wrap(function()
while true do
wait(5)
for i = 1, 10 do
eyeball3.Size = eyeball3.Size - Vector3.new(0,.04,0)
eyeball4.Size = eyeball4.Size - Vector3.new(0,.04,0)
swait()
end
for i = 1, 10 do
eyeball3.Size = eyeball3.Size + Vector3.new(0,.04,0)
eyeball4.Size = eyeball4.Size + Vector3.new(0,.04,0)
swait()
end
swait()
end
end)()

slateh = Instance.new("Decal",mask)
slateh.Texture = "rbxassetid://647441616"
slateh.Color3 = Color3.new(0, 0, 0)
slateh.Face = "Top"

slateh2 = Instance.new("Decal",mask)
slateh2.Texture = "rbxassetid://647417318"
slateh2.Color3 = Color3.new(0,0,0)
slateh2.Face = "Top"

slateh3 = Instance.new("Decal",mask)
slateh3.Texture = "rbxassetid://647410994"
slateh3.Color3 = Color3.new(1,1,1)
slateh3.Face = "Top"

slateh4 = Instance.new("Decal",mask)
slateh4.Texture = "rbxassetid://647413967"
slateh4.Color3 = Color3.new(1,1,1)
slateh4.Face = "Top"

slateh5 = Instance.new("Decal",mask)
slateh5.Texture = "rbxassetid://64739326f6"
slateh5.Color3 = Color3.new(1, 1, 1)
slateh5.Face = "Top"

mouse.KeyDown:connect(function(Press)
Press=Press:lower()
if Press=='m' then
immortality()
elseif Press=='t' then
if xester then
if tauntdebounce then return end
tauntdebounce = true
laughing = true
laugh = laughs[math.random(1,#laughs)]
laughy = Instance.new("Sound",Head)
laughy.SoundId = "rbxassetid://"..laugh
laughy.Volume = 10
laughy:Play()
wait(1)
wait(laughy.TimeLength)
laughing = false
laughy:Remove()
tauntdebounce = false
elseif rachjumper then
if tauntdebounce == true then return end
tauntdebounce = true
rdnm2 = soundtable2[math.random(1,#soundtable2)]
tauntsound = Instance.new("Sound", Head)
tauntsound.Volume = 8
tauntsound.SoundId = "http://www.roblox.com/asset/?id="..rdnm2
tauntsound.Looped = false
tauntsound:Play()
wait(3)
wait(tauntsound.TimeLength)
tauntsound:Remove()
wait(1)
tauntdebounce = false
else
if debounce then return end
debounce = true
attacking = true
ws = 0
local energball = Instance.new("Part",Torso)
energball.Shape = "Ball"
energball.Material = "Neon"
energball.Size = Vector3.new(.1,.1,.1)
energball.Anchored = true
energball.CanCollide = false
energball.BrickColor = BrickColor.new("Really black")
energball.CFrame = hand1.CFrame * CFrame.new(0,1,-2.5)
SOUND(energball,2880335731,10,false,10)
local g1 = Instance.new("BodyGyro", Root)
g1.D = 175
g1.P = 20000
g1.MaxTorque = Vector3.new(0,9000,0)
for i = 1, 250 do
g1.CFrame = g1.CFrame:lerp(CFrame.new(Root.Position,mouse.Hit.p),.2)
coroutine.wrap(function()
local sk = Instance.new("Part",Torso)
sk.CanCollide = false
sk.Anchored = true
sk.BrickColor = BrickColor.new("Really black")
sk.Name = "sk"
sk.CFrame = energball.CFrame * CFrame.Angles(math.rad(math.random(-180,180)),0,math.rad(math.random(-180,180)))
local skmesh = Instance.new("SpecialMesh",sk)
skmesh.MeshId = "rbxassetid://662586858"
skmesh.Name = "wave"
skmesh.Scale = Vector3.new(.02,.005,.02)
for i = 1, 20 do
skmesh.Scale = skmesh.Scale + Vector3.new(.004,0,.004)
sk.Transparency = sk.Transparency + .05
swait()
end
sk:Remove()
end)()
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .7
shockwave.BrickColor = BrickColor.new("Really black")
shockwave.CFrame = CFrame.new(energball.Position) * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(7,.1,7)
shockwavemesh.MeshId = "rbxassetid://20329976"
for i = 1, 20 do
shockwave.Transparency = shockwave.Transparency + .05
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(.5,0,.5)
swait()
end
shockwave:Remove()
end)()
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .4
shockwave.BrickColor = BrickColor.new("Really black")
shockwave.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,1,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .4
shockwave2.BrickColor = BrickColor.new("Really black")
shockwave2.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(1,1,1)
shockwavemesh2.MeshId = "rbxassetid://20329976"
for i = 1, 30 do
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+math.random(-4,12)),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-math.random(-4,12)),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(8,1,8)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(10,.5,10)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
energball.Size = energball.Size + Vector3.new(.02,.02,.02)
energball.CFrame = hand1.CFrame * CFrame.new(0,0,-3)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(6.5,0,-1) * CFrame.Angles(math.rad(70),math.rad(90),math.rad(0)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(6.5,0,-5) * CFrame.Angles(math.rad(-110),math.rad(90),math.rad(0)),.2)
swait()
end
local bwoo = Instance.new("Sound",Torso)
bwoo.SoundId = "rbxassetid://134012322"
bwoo.Volume = 10
bwoo.Pitch = .85
bwoo:Play()
removeuseless:AddItem(bwoo,10)
for i = 1, 20 do
g1.CFrame = g1.CFrame:lerp(CFrame.new(Root.Position,mouse.Hit.p),.2)
energball.CFrame = hand2.CFrame * CFrame.new(0,0,-3)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(0),math.rad(-35),0),.2)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(4.5,-5 + .5 * math.sin(sine/14),6) * CFrame.Angles(math.rad(10 + 1 * math.sin(sine/13)),math.rad(-5 + 5 * math.sin(sine/12)),math.rad(-36 - 4 * math.sin(sine/11))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-4.5,0,7) * CFrame.Angles(math.rad(-90),math.rad(18),math.rad(37)),.2)
swait()
end
energball.Anchored = false
local bov = Instance.new("BodyVelocity",energball)
bov.maxForce = Vector3.new(99999,99999,99999)
energball.CFrame = CFrame.new(energball.Position,mouse.Hit.p)
bov.velocity = energball.CFrame.lookVector*300
local hitted = false
energball.Touched:connect(function(hit)
if hit:IsA("Part") and hit.Parent ~= Character and hit.Name ~= "rachjumper" and hit.Parent.Parent ~= Character then
if hitted then return end
hitted = true
print("hit")
energball.Anchored = true
local energballplosion = energball:Clone() energballplosion.Parent = Torso
energball.Transparency = 1
local render = Instance.new("Sound",energball)
render.SoundId = "rbxassetid://2006635781"
render.Volume = 10 * 10
render:Play()
local zm = 0
for i = 1, 70 do
zm = zm + 2
Hit = damagealll(zm,energball.Position)
for _,v in pairs(Hit) do
if v:FindFirstChildOfClass("Humanoid") and v:FindFirstChildOfClass("Humanoid").Health > 0 then
slachtoffer = v:FindFirstChildOfClass("Humanoid")
coroutine.wrap(function()
local w = Instance.new("Part",Torso)
w.Anchored = true
w.CanCollide = false
w.Material = "Neon"
w.BrickColor = BrickColor.new("Really black")
if slachtoffer.RigType == Enum.HumanoidRigType.R15 then
w.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame
elseif slachtoffer.RigType == Enum.HumanoidRigType.R6 then
w.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame
end
w.Size = Vector3.new(3,3,3)
w.Shape = "Ball"
for i = 1, 50 do
w.Transparency = w.Transparency + .05
w.Size = w.Size + Vector3.new(3.5,3.5,3.5)
swait()
end
w:Remove()
end)()
for i = 1, 8 do
coroutine.wrap(function()
local ps = Instance.new("Part",Torso)
ps.Size = Vector3.new(1,1,1)
ps.Anchored = true
ps.BrickColor = BrickColor.new("Really black")
ps.Material = "Neon"
if slachtoffer.RigType == Enum.HumanoidRigType.R6 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
elseif slachtoffer.RigType == Enum.HumanoidRigType.R15 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
end
local psm = Instance.new("SpecialMesh",ps)
psm.MeshType = "Sphere"
psm.Scale = Vector3.new(3,1,3)
for i = 1, 50 do
psm.Scale = psm.Scale + Vector3.new(0,5,0)
ps.Transparency = ps.Transparency + .025
swait()
end
ps:Remove()
end)()
end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Clone() x.Parent = workspace x.Material = "Glass" x.BrickColor = BrickColor.new("Really black") x.Anchored = false
x.CanCollide = true x:BreakJoints() end end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Remove() end end
slachtoffer.Parent:BreakJoints()
end
end
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .4
shockwave.BrickColor = BrickColor.new("Really black")
shockwave.CFrame = CFrame.new(energballplosion.Position) * CFrame.new(0,-8,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,2,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .4
shockwave2.BrickColor = BrickColor.new("Really black")
shockwave2.CFrame = CFrame.new(energballplosion.Position) * CFrame.new(0,-8,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(11,2,11)
shockwavemesh2.MeshId = "rbxassetid://20329976"
local biggar = 0
for i = 1, 30 do
biggar = biggar + 4
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+math.random(-4,12)),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-math.random(-4,12)),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(8 + biggar,4,8 + biggar)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(10 + biggar,4,10 + biggar)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
energballplosion.Size = energballplosion.Size + Vector3.new(2,2,2)
swait()
end
for i = 1, 80 do
zm = zm + 3.5
Hit = damagealll(zm,energball.Position)
for _,v in pairs(Hit) do
if v:FindFirstChildOfClass("Humanoid") and v:FindFirstChildOfClass("Humanoid").Health > 0 then
slachtoffer = v:FindFirstChildOfClass("Humanoid")
coroutine.wrap(function()
local w = Instance.new("Part",Torso)
w.Anchored = true
w.CanCollide = false
w.Material = "Neon"
w.BrickColor = BrickColor.new("Really black")
if slachtoffer.RigType == Enum.HumanoidRigType.R15 then
w.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame
elseif slachtoffer.RigType == Enum.HumanoidRigType.R6 then
w.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame
end
w.Size = Vector3.new(3,3,3)
w.Shape = "Ball"
for i = 1, 50 do
w.Transparency = w.Transparency + .05
w.Size = w.Size + Vector3.new(3.5,3.5,3.5)
swait()
end
w:Remove()
end)()
for i = 1, 8 do
coroutine.wrap(function()
local ps = Instance.new("Part",Torso)
ps.Size = Vector3.new(1,1,1)
ps.Anchored = true
ps.BrickColor = BrickColor.new("Really black")
ps.Material = "Neon"
if slachtoffer.RigType == Enum.HumanoidRigType.R6 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
elseif slachtoffer.RigType == Enum.HumanoidRigType.R15 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
end
local psm = Instance.new("SpecialMesh",ps)
psm.MeshType = "Sphere"
psm.Scale = Vector3.new(3,1,3)
for i = 1, 50 do
psm.Scale = psm.Scale + Vector3.new(0,5,0)
ps.Transparency = ps.Transparency + .025
swait()
end
ps:Remove()
end)()
end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Clone() x.Parent = workspace x.Material = "Glass" x.BrickColor = BrickColor.new("Really black") x.Anchored = false
x.CanCollide = true x:BreakJoints() end end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Remove() end end
slachtoffer.Parent:BreakJoints()
end
end
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .4
shockwave.BrickColor = BrickColor.new("Really black")
shockwave.CFrame = CFrame.new(energballplosion.Position) * CFrame.new(0,-8,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,6,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .4
shockwave2.BrickColor = BrickColor.new("Really black")
shockwave2.CFrame = CFrame.new(energballplosion.Position) * CFrame.new(0,-8,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(11,6,11)
shockwavemesh2.MeshId = "rbxassetid://20329976"
local biggar = 0
local biggar2 = 0
for i = 1, 30 do
biggar = biggar + 14
biggar2 = biggar2 + 22
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+math.random(-4,12)),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-math.random(-4,12)),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(16 + biggar,12 + biggar,16 + biggar)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(18 + biggar2,12,18 + biggar2)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
energballplosion.Size = energballplosion.Size + Vector3.new(7,7,7)
swait()
end
for i = 1, 50 do
energballplosion.Size = energballplosion.Size + Vector3.new(5,5,5)
energballplosion.Transparency = energballplosion.Transparency + .025
swait()
end
energballplosion:Remove()
end
end)
for i = 1, 20 do
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(6,-5 + .5 * math.sin(sine/14),6) * CFrame.Angles(math.rad(20 + 1 * math.sin(sine/13)),math.rad(-5 + 5 * math.sin(sine/12)),math.rad(-36 - 4 * math.sin(sine/11))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.5,0,5) * CFrame.Angles(math.rad(30),math.rad(-28),math.rad(37)),.2)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(0),math.rad(35),0),.2)
swait()
end
removeuseless:AddItem(g1,.001)
debounce = false
if xester then
ws = 155
else
ws = 92
end
attacking = false
end
elseif Press=='x' then
if debounce then return end
debounce = true
attacking = true
ws = 0
for i = 1, 70 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.1)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 + 1 * math.sin(sine)),math.rad(30 + 2 * math.sin(sine))),.1)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 - 1 * math.sin(sine)),math.rad(-30 - 2 * math.sin(sine))),.1)
swait()
end
for i = 1, 40 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 + 2 * math.sin(sine)),math.rad(30 + 4 * math.sin(sine))),.05)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 - 2 * math.sin(sine)),math.rad(-30 - 4 * math.sin(sine))),.05)
swait()
end
rachjumper = true
xester = false
doomtheme.Volume = 0
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .2
shockwave.BrickColor = BrickColor.new("Really red")
shockwave.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,1,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .2
shockwave2.BrickColor = BrickColor.new("Really red")
shockwave2.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(1,1,1)
shockwavemesh2.MeshId = "rbxassetid://20329976"
for i = 1, 30 do
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+16),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-16),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(10,1,10)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(14,2,14)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
coroutine.wrap(function()
local nball = Instance.new("Part",Torso)
nball.Size = Vector3.new(4,4,4)
nball.Material = "Neon"
nball.BrickColor = BrickColor.new("Really red")
nball.Shape = "Ball"
nball.Anchored = true
nball.CanCollide = false
nball.CFrame = Torso.CFrame
for i = 1, 40 do
nball.Size = nball.Size + Vector3.new(5.5,5.5,5.5)
nball.Transparency = nball.Transparency + .05
swait()
end
nball:Remove()
end)()
particlecolor = ColorSequence.new(Color3.new(255, 255, 255))

particlemiter1 = Instance.new("ParticleEmitter", bighead)
particlemiter1.Enabled = true
particlemiter1.Color = particlecolor
particlemiter1.Texture = "rbxassetid://1390780157"
particlemiter1.Lifetime = NumberRange.new(.05)
particlemiter1.Size = NumberSequence.new(7.5,7.5)
particlemiter1.Rate = 4
particlemiter1.Rotation = NumberRange.new(0,360)
particlemiter1.RotSpeed = NumberRange.new(0)
particlemiter1.Speed = NumberRange.new(0)

particlemiter2 = Instance.new("ParticleEmitter", hand1)
particlemiter2.Enabled = true
particlemiter2.Color = particlecolor
particlemiter2.Texture = "rbxassetid://1390780157"
particlemiter2.Lifetime = NumberRange.new(.05)
particlemiter2.Size = NumberSequence.new(5,5)
particlemiter2.Rate = 4
particlemiter2.Rotation = NumberRange.new(0,360)
particlemiter2.RotSpeed = NumberRange.new(0)
particlemiter2.Speed = NumberRange.new(0)

particlemiter3 = Instance.new("ParticleEmitter", hand2)
particlemiter3.Enabled = true
particlemiter3.Color = particlecolor
particlemiter3.Texture = "rbxassetid://1390780157"
particlemiter3.Lifetime = NumberRange.new(.05)
particlemiter3.Size = NumberSequence.new(5,5)
particlemiter3.Rate = 4
particlemiter3.Rotation = NumberRange.new(0,360)
particlemiter3.RotSpeed = NumberRange.new(0)
particlemiter3.Speed = NumberRange.new(0)
coroutine.wrap(function()
transformsound = Instance.new("Sound",Torso)
transformsound.Volume = 10
transformsound.SoundId = "rbxassetid://159576182"
transformsound:Play() 
coroutine.wrap(function()
wait(1)
realmofexistence = Instance.new("Sound",Torso)
realmofexistence.Volume = 8
realmofexistence.SoundId = "rbxassetid://2565721367"
realmofexistence:Play()
end)()
wait(2.2)
doomtheme.SoundId = "rbxassetid://2902017580"
doomtheme:Play()
doomtheme.Pitch = 1
doomtheme.TimePosition = 0
for i = 1, 30 do
doomtheme.Volume = doomtheme.Volume + .25
swait()
end
end)()

slaten.Transparency = 1
slaten2.Transparency = 1
slateh.Transparency = 1
slateh2.Transparency = 1
slateh3.Transparency = 1
slateh4.Transparency = 1
slateh5.Transparency = 1
slatex.Transparency = 1
slatex2.Transparency = 1
slatex3.Transparency = 1
slatex4.Transparency = 1
slatex5.Transparency = 1
slatez.Transparency = 1
slatez2.Transparency = 1
slatez3.Transparency = 1
slatez4.Transparency = 1
eyeball1.Transparency = 1
eyeball2.Transparency = 1
eyeball3.Transparency = 1
eyeball4.Transparency = 1
lightpart1.Transparency = 1
Root.Anchored = false
horns.Material = "Slate"
horns.Locked = true
horns.BrickColor = BrickColor.new("Really black")
hornsmesh.MeshId = "rbxassetid://398618628"
hornsmesh.VertexColor = Vector3.new(1,0,0)
hornsmesh.TextureId = "rbxassetid://1461382301"
hornsmesh.Scale = Vector3.new(4.9, 5.5, 5.8)
hornsweld.C0 = CFrame.new(0,3.8,-4.5) * CFrame.Angles(math.rad(0),math.rad(0),0)
mask.Anchored = false
mask.Locked = true
mask.CanCollide = false
mask.Transparency = 0
mask.BrickColor = BrickColor.new("White")
mask.Material = "Corroded Metal"
maskweld.C0 = CFrame.new(0,1.45,-.4) * CFrame.Angles(math.rad(0),0,0)
maskmesh.MeshId = "rbxassetid://64560176"
maskmesh.TextureId = "rbxassetid://1326186614"
maskmesh.Scale = Vector3.new(5.04, 5.04, 5.04)
hand2.BrickColor = BrickColor.new("Really black")
hand1.BrickColor = BrickColor.new("Really black")
face = Instance.new("Decal",bighead)
face.Texture = "rbxassetid://1127768638"
face.Color3 = Color3.new(255, 255, 255)
face.Face = "Front"
attacking = false
ws = 92
debounce = false
elseif Press=='z' then
if debounce then return end
debounce = true
attacking = true
ws = 0
for i = 1, 70 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.1)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 + 1 * math.sin(sine)),math.rad(30 + 2 * math.sin(sine))),.1)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 - 1 * math.sin(sine)),math.rad(-30 - 2 * math.sin(sine))),.1)
swait()
end
for i = 1, 40 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 + 2 * math.sin(sine)),math.rad(30 + 4 * math.sin(sine))),.05)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 - 2 * math.sin(sine)),math.rad(-30 - 4 * math.sin(sine))),.05)
swait()
end
if rachjumper then
face:Remove()
particlemiter1:Remove()
particlemiter2:Remove()
particlemiter3:Remove()
end
xester = true
rachjumper = false
hand1.BrickColor = BrickColor.new("White")
hand2.BrickColor = BrickColor.new("White")
coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .2
shockwave.BrickColor = BrickColor.new("White")
shockwave.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,1,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .2
shockwave2.BrickColor = BrickColor.new("White")
shockwave2.CFrame = CFrame.new(Root.Position) * CFrame.new(0,-8,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(1,1,1)
shockwavemesh2.MeshId = "rbxassetid://20329976"
for i = 1, 30 do
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+16),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-16),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(10,1,10)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(14,2,14)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
coroutine.wrap(function()
local nball = Instance.new("Part",Torso)
nball.Size = Vector3.new(4,4,4)
nball.Material = "Neon"
nball.BrickColor = BrickColor.new("White")
nball.Shape = "Ball"
nball.Anchored = true
nball.CanCollide = false
nball.CFrame = Torso.CFrame
for i = 1, 40 do
nball.Size = nball.Size + Vector3.new(5.5,5.5,5.5)
nball.Transparency = nball.Transparency + .05
swait()
end
nball:Remove()
end)()
doomtheme.SoundId = "rbxassetid://1382488262"
doomtheme:Play()
doomtheme.Volume = 6
doomtheme.Pitch = 1
doomtheme.TimePosition = 20.7
slaten.Transparency = 1
slaten2.Transparency = 1
slateh.Transparency = 1
slateh2.Transparency = 1
slateh3.Transparency = 1
slateh4.Transparency = 1
slateh5.Transparency = 1
slatex.Transparency = 1
slatex2.Transparency = 1
slatex3.Transparency = 1
slatex4.Transparency = 1
slatex5.Transparency = 1
slatez.Transparency = 1
slatez2.Transparency = 1
slatez3.Transparency = 1
slatez4.Transparency = 1
eyeball1.Transparency = 1
eyeball2.Transparency = 1
eyeball3.Transparency = 1
eyeball4.Transparency = 1
lightpart1.Transparency = 0
laugh = laughs[math.random(1,#laughs)]
local laughy = Instance.new("Sound",Head)
laughy.SoundId = "rbxassetid://"..laugh
laughy.Volume = 10
laughy:Play()
removeuseless:AddItem(laughy,10)
Root.Anchored = false
horns.Material = "Slate"
horns.Locked = true
horns.BrickColor = BrickColor.new("Really black")
hornsmesh.MeshId = "rbxassetid://193760002"
hornsmesh.VertexColor = Vector3.new(1,0,0)
hornsmesh.TextureId = "rbxassetid://379225327"
hornsmesh.Scale = Vector3.new(5.41,5.41,5.41)
hornsweld.C0 = CFrame.new(0,-2.75,-1.7) * CFrame.Angles(math.rad(0),math.rad(0),math.rad(0))
mask.Anchored = false
mask.Locked = true
mask.CanCollide = false
mask.BrickColor = BrickColor.new("White")
mask.Material = "Corroded Metal"
maskweld.C0 = CFrame.new(0,0,2.5) * CFrame.Angles(math.rad(0),0,0)
maskmesh.MeshId = "rbxassetid://13520257"
maskmesh.TextureId = "rbxassetid://13520260"
maskmesh.Scale = Vector3.new(5.53, 5, 5.1)
for i = 1, 30 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(30),math.rad(0 * math.sin(sine/16)),math.rad(0)),.1)
swait()
end
for i = 1, 50 do
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-140 + 2 * math.sin(sine)),math.rad(180 - 1 * math.sin(sine)),math.rad(-30 - 2 * math.sin(sine))),.03)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-140 + 2 * math.sin(sine)),math.rad(180 + 1 * math.sin(sine)),math.rad(30 + 2 * math.sin(sine))),.03)
swait()
end
for i = 1, 50 do
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-140 + 8 * math.sin(sine)),math.rad(180 - 5 * math.sin(sine)),math.rad(-30 - 8 * math.sin(sine))),.03)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-140 + 8 * math.sin(sine)),math.rad(180 + 5 * math.sin(sine)),math.rad(30 + 8 * math.sin(sine))),.03)
swait()
end
ws = 155
Root.Anchored = false
debounce = false
attacking = false
xester = true
elseif Press=='r' then
if mouse.Target ~= nil and mouse.Target.Parent:FindFirstChildOfClass("Humanoid") then
if debounce then return end
debounce = true
attacking = true
local enemy = mouse.Target.Parent:FindFirstChildOfClass("Humanoid")
local targ = mouse.Target.Parent:FindFirstChildOfClass("Humanoid").Parent
SOUND(Head,1837106999,10,false,10)
ws = 0
local z = { 
Color = BrickColor.new("Crimson").Color
}
local z2 = { 
Color = BrickColor.new("Really black").Color
}
eyeball1.Material = "Neon"
eyeball2.Material = "Neon"
for i = 1, 7 do
local lol = smoothen:Create(eyeball1,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol2:Play()
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50),math.rad(180),math.rad(10)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50),math.rad(180),math.rad(-10)),.2)
swait()
end
for i = 1, 70 do
local lol = smoothen:Create(eyeball1,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol2:Play()
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 + 1 * math.sin(sine)),math.rad(30 + 2 * math.sin(sine))),.05)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 2 * math.sin(sine)),math.rad(180 - 1 * math.sin(sine)),math.rad(-30 - 2 * math.sin(sine))),.05)
swait()
end
for i = 1, 40 do
local lol = smoothen:Create(eyeball1,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol2:Play()
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-50),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(-2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 + 2 * math.sin(sine)),math.rad(30 + 4 * math.sin(sine))),.05)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(2,-2,-4) * CFrame.Angles(math.rad(-50 + 4 * math.sin(sine)),math.rad(180 - 2 * math.sin(sine)),math.rad(-30 - 4 * math.sin(sine))),.05)
swait()
end
attacking = false
local targetfound = false
local chasemusic = Instance.new("Sound",Head)
chasemusic.Volume = 10
chasemusic.SoundId = "rbxassetid://2866313732"
chasemusic.Looped = true
chasemusic:Play()
for i = 1, 1000 do
if targetfound then break end
local Hit = damagealll(15,Torso.Position)
for _,v in pairs(Hit) do
if v:FindFirstChildOfClass("Humanoid") and v:FindFirstChildOfClass("Humanoid").Parent.Name == enemy.Parent.Name then
targetfound = true
slachtoffer = v:FindFirstChildOfClass("Humanoid")
end
end
huntdown = true
hum:MoveTo(enemy.Parent.Torso.Position)
ws = 150
swait()
end
if targetfound then
attacking = true
local lweld = weldBetween(enemy.Parent.Torso,hand1)
lweld.C0 = CFrame.new(2,-2,0) * CFrame.Angles(math.rad(0),math.rad(90),math.rad(90))
ws = 0
enemy.WalkSpeed = 0
enemy.JumpPower = 0
local IAMHERE = Instance.new("Sound",Head)
IAMHERE.SoundId = "rbxassetid://2867055627"
IAMHERE.Volume = 10
IAMHERE:Play()
removeuseless:AddItem(IAMHERE,10)
for i = 1, 220 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-10),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(2,-7.5,-2.2) * CFrame.Angles(math.rad(90 + 2 * math.sin(sine)),math.rad(2 * math.sin(sine)),math.rad(-80 + 2 * math.sin(sine))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-2,-7.5,-2.2) * CFrame.Angles(math.rad(90 - 2 * math.sin(sine)),math.rad(2 * math.sin(sine)),math.rad(80 - 2 * math.sin(sine))),.2)
swait()
end
lweld:Remove()
coroutine.wrap(function()
local w = Instance.new("Part",Torso)
w.Anchored = true
w.CanCollide = false
w.Material = "Neon"
w.BrickColor = BrickColor.new("Really black")
if targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R15 then
w.CFrame = targ:FindFirstChild("UpperTorso").CFrame
elseif targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then
w.CFrame = targ:FindFirstChild("Torso").CFrame
end
w.Size = Vector3.new(3,3,3)
w.Shape = "Ball"
for i = 1, 50 do
w.Transparency = w.Transparency + .05
w.Size = w.Size + Vector3.new(3.5,3.5,3.5)
swait()
end
w:Remove()
end)()
for i = 1, 8 do
coroutine.wrap(function()
local ps = Instance.new("Part",Torso)
ps.Size = Vector3.new(1,1,1)
ps.Anchored = true
ps.BrickColor = BrickColor.new("Really black")
ps.Material = "Neon"
if targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R15 then
ps.CFrame = targ:FindFirstChild("UpperTorso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
elseif targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then
ps.CFrame = targ:FindFirstChild("Torso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
end
local psm = Instance.new("SpecialMesh",ps)
psm.MeshType = "Sphere"
psm.Scale = Vector3.new(3,1,3)
for i = 1, 50 do
psm.Scale = psm.Scale + Vector3.new(0,5,0)
ps.Transparency = ps.Transparency + .025
swait()
end
ps:Remove()
end)()
end
for i,x in pairs(targ:GetDescendants()) do if x:IsA("Part") then x:Clone() x.Parent = workspace x.Material = "Glass" x.BrickColor = BrickColor.new("Really black") x.Anchored = false
x.CanCollide = true x:BreakJoints() end end
for i,x in pairs(targ:GetDescendants()) do if x:IsA("Part") then x:Remove() end end
targ:BreakJoints()
SOUND(hand1,264486467,8,false,10)
huntdown = false
for i = 1, 25 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-25),math.rad(0 * math.sin(sine/16)),math.rad(0)),.05)
local lol = smoothen:Create(eyeball1,TweenInfo.new(.5,Enum.EasingStyle.Linear),z2)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.5,Enum.EasingStyle.Linear),z2)
lol2:Play()
chasemusic.Volume = chasemusic.Volume - .5
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(2,-7.5,-1) * CFrame.Angles(math.rad(90),math.rad(0),math.rad(-80)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-2,-7.5,-1) * CFrame.Angles(math.rad(90),math.rad(0),math.rad(80)),.2)
swait()
end
chasemusic:Remove()
if xester then
ws = 155
else
ws = 92
end
eyeball1.Material = "Glass"
eyeball2.Material = "Glass"
attacking = false
debounce = false
else
if xester then
ws = 155
else
ws = 92
end
huntdown = false
eyeball1.Material = "Glass"
eyeball2.Material = "Glass"
debounce = false
attacking = false
coroutine.wrap(function()
for i = 1, 25 do
if debounce then break end
local lol = smoothen:Create(eyeball1,TweenInfo.new(.5,Enum.EasingStyle.Linear),z2)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.5,Enum.EasingStyle.Linear),z2)
lol2:Play()
swait()
end
end)()
chasemusic:Remove()
end
end
elseif Press=='e' then
if debounce then return end
debounce = true
attacking = true
g1 = Instance.new("BodyGyro", Root)
g1.D = 175
g1.P = 20000
g1.MaxTorque = Vector3.new(0,9000,0)
ws = 30
for i =  1,  75 do
g1.CFrame = g1.CFrame:lerp(CFrame.new(Root.Position,mouse.Hit.p),.2)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(5.2 + .6 * math.sin(sine/14),-5,6) * CFrame.Angles(math.rad(15 * math.sin(sine/12)),math.rad(16 * math.sin(sine/14)),math.rad(0)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.2 + .6 * math.sin(sine/14),-5,6) * CFrame.Angles(math.rad(-15 * math.sin(sine/12)),math.rad(-16 * math.sin(sine/14)),math.rad(0)),.2)
swait()
end
local bwoo = Instance.new("Sound",Torso)
bwoo.SoundId = "rbxassetid://134012322"
bwoo.Volume = 10
bwoo.Pitch = .85
bwoo:Play()
removeuseless:AddItem(bwoo,7)
for i =  1,  25 do
g1.CFrame = g1.CFrame:lerp(CFrame.new(Root.Position,mouse.Hit.p),.2)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(25),math.rad(0 * math.sin(sine/16)),math.rad(0)),.2)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(5.2,-5,6) * CFrame.Angles(math.rad(-94 + 8 * math.sin(sine/12)),math.rad(3 * math.sin(sine/10)),math.rad(0)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.2,-5,6) * CFrame.Angles(math.rad(-94 - 8 * math.sin(sine/12)),math.rad(3 * -math.sin(sine/10)),math.rad(0)),.2)
swait()
end
ws = 0
for i =  1,  3 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(0),math.rad(0 * math.sin(sine/16)),math.rad(0)),.2)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(5.2,-5,6) * CFrame.Angles(math.rad(-76 + 8 * math.sin(sine/12)),math.rad(3 * math.sin(sine/10)),math.rad(0)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.2,-5,6) * CFrame.Angles(math.rad(-76 - 8 * math.sin(sine/12)),math.rad(3 * -math.sin(sine/10)),math.rad(0)),.2)
swait()
end
local rocksm = Instance.new("Sound",Torso)
rocksm.SoundId = "rbxassetid://168514932"
rocksm.Volume = 10
rocksm.Pitch = .94
rocksm:Play()
removeuseless:AddItem(rocksm,7)
removeuseless:AddItem(g1,.001)
local rb = Instance.new("Part",Torso)
rb.Size = Vector3.new(.1,.1,.1)
rb.Anchored = false
rb.Transparency = 1
rb.CanCollide = false
rb.CFrame = CFrame.new(mouse.Hit.p) * CFrame.new(0,30,10)
local rbweld = weldBetween(rb,Root)
rbweld.C0 = CFrame.new(0,10,45)
local txc = 10
coroutine.wrap(function()
	for i = 1, 10 do
		coroutine.wrap(function()
	local sondb = Instance.new("Part",rb)
	sondb.Anchored = true
	sondb.Transparency = 1
	sondb.CanCollide = false
	sondb.CFrame = rb.CFrame
	local booms = Instance.new("Sound",sondb)
	booms.SoundId = "rbxassetid://2175667385"
	booms.Volume = 5
	booms.Pitch = .8
	for i = 1, 20 do
		swait()
	end
	wait(1)
	booms:Play()
	end)()
	swait(6)
	end
end)()
for i = 1, 90 do
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(-30),math.rad(0 * math.sin(sine/16)),math.rad(0)),.2)
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(5.2,-2,7.2 + .95 * math.sin(sine/12)) * CFrame.Angles(math.rad(45),math.rad(-9),math.rad(0)),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.2,-2,7.2+ .95 * math.sin(sine/12)) * CFrame.Angles(math.rad(45),math.rad(9),math.rad(0)),.2)
	coroutine.wrap(function()
	local cyl = Instance.new("Part",Torso)
	cyl.Shape = "Cylinder"
	cyl.BrickColor = BrickColor.new("Really black")
	cyl.Anchored = true
	cyl.Transparency = 1
	cyl.CanCollide = false
	cyl.Material = "Neon"
	cyl.CFrame = rb.CFrame * CFrame.new(math.random(-30,30),2,math.random(-30,30)) * CFrame.Angles(math.rad(90),math.rad(90),0)
	cyl.Size = Vector3.new(4,6 * math.random(4,8),6 * math.random(4,8))
	for i = 1, 20 do
		cyl.Transparency = cyl.Transparency - .05
		swait()
	end
	wait(1)
	local brock = Instance.new("Part",Torso)
	brock.Size = Vector3.new(9,70 + math.random(10,33),9)
	brock.Anchored = true
	brock.Transparency = .3
	brock.CanCollide = false
	brock.Material = "Neon"
	brock.BrickColor = BrickColor.new("Really black")
	brock.CFrame = cyl.CFrame * CFrame.new(0,70,0)
	coroutine.wrap(function()
local shockwave = Instance.new("Part", Torso)
shockwave.Size = Vector3.new(1,1,1)
shockwave.CanCollide = false
shockwave.Anchored = true
shockwave.Transparency = .4
shockwave.BrickColor = BrickColor.new("White")
shockwave.CFrame = CFrame.new(cyl.Position) * CFrame.new(0,-1,0)
local shockwavemesh = Instance.new("SpecialMesh", shockwave)
shockwavemesh.Scale = Vector3.new(10,1,10)
shockwavemesh.MeshId = "rbxassetid://20329976"
local shockwave2 = Instance.new("Part", Torso)
shockwave2.Size = Vector3.new(1,1,1)
shockwave2.CanCollide = false
shockwave2.Anchored = true
shockwave2.Transparency = .4
shockwave2.BrickColor = BrickColor.new("White")
shockwave2.CFrame = CFrame.new(cyl.Position) * CFrame.new(0,-1,0)
local shockwavemesh2 = Instance.new("SpecialMesh", shockwave2)
shockwavemesh2.Scale = Vector3.new(1,1,1)
shockwavemesh2.MeshId = "rbxassetid://20329976"
for i = 1, 30 do
shockwave.CFrame = shockwave.CFrame * CFrame.Angles(math.rad(0),math.rad(0+math.random(-4,12)),0)
shockwave2.CFrame = shockwave2.CFrame * CFrame.Angles(math.rad(0),math.rad(0-math.random(-4,12)),0)
shockwave.Transparency = shockwave.Transparency + 0.05
shockwave2.Transparency = shockwave2.Transparency + 0.05
shockwavemesh2.Scale = shockwavemesh2.Scale + Vector3.new(8,2.5,8)
shockwavemesh.Scale = shockwavemesh.Scale + Vector3.new(10,2,10)
swait()
end
shockwave:Remove()
shockwave2:Remove()
	end)()
Hit = damagealll(52,brock.Position)
for _,v in pairs(Hit) do
if v:FindFirstChildOfClass("Humanoid") and v:FindFirstChildOfClass("Humanoid").Health > 0 then
slachtoffer = v:FindFirstChildOfClass("Humanoid")
coroutine.wrap(function()
local w = Instance.new("Part",Torso)
w.Anchored = true
w.CanCollide = false
w.Material = "Neon"
w.BrickColor = BrickColor.new("Really black")
if slachtoffer.RigType == Enum.HumanoidRigType.R15 then
w.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame
elseif slachtoffer.RigType == Enum.HumanoidRigType.R6 then
w.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame
end
w.Size = Vector3.new(3,3,3)
w.Shape = "Ball"
for i = 1, 50 do
w.Transparency = w.Transparency + .05
w.Size = w.Size + Vector3.new(3.5,3.5,3.5)
swait()
end
w:Remove()
end)()
for i = 1, 8 do
coroutine.wrap(function()
local ps = Instance.new("Part",Torso)
ps.Size = Vector3.new(1,1,1)
ps.Anchored = true
ps.BrickColor = BrickColor.new("Really black")
ps.Material = "Neon"
if slachtoffer.RigType == Enum.HumanoidRigType.R6 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("Torso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
elseif slachtoffer.RigType == Enum.HumanoidRigType.R15 then
ps.CFrame = slachtoffer.Parent:FindFirstChild("UpperTorso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
end
local psm = Instance.new("SpecialMesh",ps)
psm.MeshType = "Sphere"
psm.Scale = Vector3.new(3,1,3)
for i = 1, 50 do
psm.Scale = psm.Scale + Vector3.new(0,5,0)
ps.Transparency = ps.Transparency + .025
swait()
end
ps:Remove()
end)()
end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Clone() x.Parent = workspace x.Material = "Glass" x.BrickColor = BrickColor.new("Really black") x.Anchored = false
x.CanCollide = true x:BreakJoints() end end
for i,x in pairs(slachtoffer.Parent:GetDescendants()) do if x:IsA("Part") then x:Remove() end end
slachtoffer.Parent:BreakJoints()
end
end
	for i = 1, 50 do
		brock.CFrame = brock.CFrame:lerp(CFrame.new(cyl.Position) * CFrame.new(0,2,0) * CFrame.Angles(math.rad(math.random(-12,12)),math.rad(math.random(-12,12)),math.rad(math.random(-12,12))),.25)
		swait()
	end
	wait(4)
	for i = 1, 40 do
		brock.CFrame = brock.CFrame:lerp(CFrame.new(cyl.Position) * CFrame.new(0,2,0) * CFrame.Angles(math.rad(math.random(-12,12)),math.rad(math.random(-12,12)),math.rad(math.random(-12,12))),.25)
		swait()
	end
	for i = 1, 40 do
		brock.Transparency = brock.Transparency + .025
		brock.CFrame = brock.CFrame:lerp(CFrame.new(cyl.Position) * CFrame.new(0,-40,0) * CFrame.Angles(math.rad(math.random(-12,12)),math.rad(math.random(-12,12)),math.rad(math.random(-12,12))),.09)
		swait()
	end
	brock:Remove()
	for i = 1, 30 do
		cyl.Size = cyl.Size + Vector3.new(0,3,3)
		cyl.Transparency = cyl.Transparency + .05
		swait()
	end
	cyl:Remove()
	rb:Remove()
	end)()
	txc = txc + 8
	rbweld.C0 = rbweld.C0:lerp(CFrame.new(0,10,txc),.3)
	swait()
end
attacking = false
debounce = false
if xester then
ws = 155
else
ws = 92
end
elseif Press=='q' then
if mouse.Target ~= nil and mouse.Target.Parent:FindFirstChildOfClass("Humanoid") then
if debounce then return end
debounce = true
ws = 0
g1 = Instance.new("BodyGyro", Root)
g1.D = 175
g1.P = 20000
g1.MaxTorque = Vector3.new(0,9000,0)
local targ = mouse.Target.Parent:FindFirstChildOfClass("Humanoid").Parent
for i = 1, 20 do
g1.CFrame = g1.CFrame:lerp(CFrame.new(Root.Position,targ.Head.Position),.2)
swait()
end
removeuseless:AddItem(g1,.001)
eyeball1.BrickColor = BrickColor.new("Crimson")
eyeball1.Material = "Neon"
eyeball2.BrickColor = BrickColor.new("Crimson")
eyeball2.Material = "Neon"
local z = { 
Color = BrickColor.new("Really black").Color
}
SOUND(Head,2175667385,10,false,10)
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
coroutine.wrap(function()
coroutine.wrap(function()
coroutine.wrap(function()
local w = Instance.new("Part",Torso)
w.Anchored = true
w.CanCollide = false
w.Material = "Neon"
w.BrickColor = BrickColor.new("Really black")
if targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R15 then
w.CFrame = targ:FindFirstChild("UpperTorso").CFrame
elseif targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then
w.CFrame = targ:FindFirstChild("Torso").CFrame
end
w.Size = Vector3.new(3,3,3)
w.Shape = "Ball"
for i = 1, 50 do
w.Transparency = w.Transparency + .05
w.Size = w.Size + Vector3.new(3.5,3.5,3.5)
swait()
end
w:Remove()
end)()
for i = 1, 8 do
coroutine.wrap(function()
local ps = Instance.new("Part",Torso)
ps.Size = Vector3.new(1,1,1)
ps.Anchored = true
ps.BrickColor = BrickColor.new("Really black")
ps.Material = "Neon"
if targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R15 then
ps.CFrame = targ:FindFirstChild("UpperTorso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
elseif targ:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then
ps.CFrame = targ:FindFirstChild("Torso").CFrame * CFrame.Angles(math.rad(math.random(-180,180)),math.rad(math.random(-180,180)),math.rad(math.random(-180,180)))
end
local psm = Instance.new("SpecialMesh",ps)
psm.MeshType = "Sphere"
psm.Scale = Vector3.new(3,1,3)
for i = 1, 50 do
psm.Scale = psm.Scale + Vector3.new(0,5,0)
ps.Transparency = ps.Transparency + .025
swait()
end
ps:Remove()
end)()
end
end)()
for i,x in pairs(targ:GetDescendants()) do if x:IsA("Part") then x:Clone() x.Parent = workspace x.Material = "Glass" x.BrickColor = BrickColor.new("Really black") x.Anchored = false
x.CanCollide = true x:BreakJoints() end end
for i,x in pairs(targ:GetDescendants()) do if x:IsA("Part") then x:Remove() end end
targ:BreakJoints()
for i = 1, 40 do
local lol = smoothen:Create(eyeball1,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol:Play()
local lol2 = smoothen:Create(eyeball2,TweenInfo.new(.3,Enum.EasingStyle.Linear),z)
lol2:Play()
swait()
end
eyeball1.BrickColor = BrickColor.new("Really black")
eyeball2.BrickColor = BrickColor.new("Really black")
eyeball1.Material = "Glass"
eyeball2.Material = "Glass"
debounce = false
if xester then
ws = 155
else
ws = 92
end
end)()
end
end
end
end)

checks1 = coroutine.wrap(function() -------Checks
while true do
if Root.Velocity.Magnitude < 10 then
position = "Idle"
elseif Root.Velocity.Magnitude > 10 then
position = "Walking"
else
end
wait()
end
end)
checks1()

function ray(POSITION, DIRECTION, RANGE, IGNOREDECENDANTS)
	return workspace:FindPartOnRay(Ray.new(POSITION, DIRECTION.unit * RANGE), IGNOREDECENDANTS)
end

function ray2(StartPos, EndPos, Distance, Ignore)
local DIRECTION = CFrame.new(StartPos,EndPos).lookVector
return ray(StartPos, DIRECTION, Distance, Ignore)
end

OrgnC0 = Neck.C0
local movelimbs = coroutine.wrap(function()
while RunSrv.RenderStepped:wait() do
TrsoLV = Torso.CFrame.lookVector
Dist = nil
Diff = nil
if not MseGuide then
print("Failed to recognize")
else
local _, Point = Workspace:FindPartOnRay(Ray.new(Head.CFrame.p, mouse.Hit.lookVector), Workspace, false, true)
Dist = (Head.CFrame.p-Point).magnitude
Diff = Head.CFrame.Y-Point.Y
local _, Point2 = Workspace:FindPartOnRay(Ray.new(LeftArm.CFrame.p, mouse.Hit.lookVector), Workspace, false, true)
Dist2 = (LeftArm.CFrame.p-Point).magnitude
Diff2 = LeftArm.CFrame.Y-Point.Y
HEADLERP.C0 = CFrame.new(0, -1.5, -0) * CFrame.Angles(math.rad(0), math.rad(0), math.rad(0))
Neck.C0 = Neck.C0:lerp(OrgnC0*CFrame.Angles((math.tan(Diff/Dist)*1), 0, (((Head.CFrame.p-Point).Unit):Cross(Torso.CFrame.lookVector)).Y*1), .1)
end
end
end)
movelimbs()
immortal = {}
for i,v in pairs(Character:GetDescendants()) do
	if v:IsA("BasePart") and v.Name ~= "lmagic" and v.Name ~= "rmagic" then
		if v ~= Root and v ~= Torso and v ~= Head and v ~= RightArm and v ~= LeftArm and v ~= RightLeg and v.Name ~= "lmagic" and v.Name ~= "rmagic" and v ~= LeftLeg then
			v.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0)
		end
		table.insert(immortal,{v,v.Parent,v.Material,v.Color,v.Transparency})
	elseif v:IsA("JointInstance") then
		table.insert(immortal,{v,v.Parent,nil,nil,nil})
	end
end
for e = 1, #immortal do
	if immortal[e] ~= nil then
		local STUFF = immortal[e]
		local PART = STUFF[1]
		local PARENT = STUFF[2]
		local MATERIAL = STUFF[3]
		local COLOR = STUFF[4]
		local TRANSPARENCY = STUFF[5]
if levitate then
		if PART.ClassName == "Part" and PART ~= Root and PART.Name ~= eyo1 and PART.Name ~= eyo2 and PART.Name ~= "lmagic" and PART.Name ~= "rmagic" then
			PART.Material = MATERIAL
			PART.Color = COLOR
			PART.Transparency = TRANSPARENCY
		end
		PART.AncestryChanged:connect(function()
			PART.Parent = PARENT
		end)
else
		if PART.ClassName == "Part" and PART ~= Root and PART.Name ~= "lmagic" and PART.Name ~= "rmagic" then
			PART.Material = MATERIAL
			PART.Color = COLOR
			PART.Transparency = TRANSPARENCY
		end
		PART.AncestryChanged:connect(function()
			PART.Parent = PARENT
		end)
end
	end
end
function immortality()
	for e = 1, #immortal do
		if immortal[e] ~= nil then
			local STUFF = immortal[e]
			local PART = STUFF[1]
			local PARENT = STUFF[2]
			local MATERIAL = STUFF[3]
			local COLOR = STUFF[4]
			local TRANSPARENCY = STUFF[5]
			if PART.ClassName == "Part" and PART == Root then
				PART.Material = MATERIAL
				PART.Color = COLOR
				PART.Transparency = TRANSPARENCY
			end
			if PART.Parent ~= PARENT then
				hum:Remove()
				PART.Parent = PARENT
				hum = Instance.new("Humanoid",Character)
if levitate then
eyo1:Remove()
eyo2:Remove()
end
                                hum.Name = "noneofurbusiness"
			end
		end
	end
end
coroutine.wrap(function()
while true do
hum:SetStateEnabled("Dead",false) hum:SetStateEnabled(Enum.HumanoidStateType.Dead, false)
if hum.Health < .1 then
immortality()
end
wait()
end
end)()

leftlocation = Instance.new("Part",LeftArm)
leftlocation.Size = Vector3.new(1,1,1)
leftlocation.Transparency = 1
leftlocationweld = weldBetween(leftlocation,LeftArm)
leftlocationweld.C0 = CFrame.new(0,1.2,0)
rightlocation = Instance.new("Part",RightArm)
rightlocation.Size = Vector3.new(1,1,1)
rightlocation.Transparency = 1
rightlocationweld = weldBetween(rightlocation,RightArm)
rightlocationweld.C0 = CFrame.new(0,1.2,0)

coroutine.wrap(function()
while true do
hpheight = 5.8 + .95 * math.sin(sine/12)
hum.HipHeight = hpheight
swait()
end
end)()

local anims = coroutine.wrap(function()
while true do
settime = 0.05
sine = sine + change
if position == "Walking" and attacking == false then
if huntdown then
change = .85
else
change = .5
end
walking = true
if xester then
ws = 155
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(5.9,-7 + 0 * math.sin(sine/6),5) * CFrame.Angles(math.rad(212 + 3 * math.sin(sine/6)),math.rad(-25),math.rad(2 * math.sin(sine/6))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5.9,-7 + 0 * math.sin(sine/6),5) * CFrame.Angles(math.rad(212 + 3 * math.sin(sine/6)),math.rad(25),math.rad(2 * math.sin(sine/6))),.2)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0 * math.sin(sine/1.75),0) * CFrame.Angles(math.rad(0 + 0 * math.sin(sine/3.5)),math.rad(0 * math.sin(sine/3.5)) + Root.RotVelocity.Y / 15,math.rad(0) + Root.RotVelocity.Y / 19),.2)
LEFTARMLERP.C0 = LEFTARMLERP.C0:lerp(CFrame.new(1.5,.78,0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(4),math.rad(35)),.25)
RIGHTARMLERP.C0 = RIGHTARMLERP.C0:lerp(CFrame.new(-1.5, .78, 0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(-4),math.rad(-35)), 0.25)
RIGHTLEGLERP.C0 = RIGHTLEGLERP.C0:lerp(CFrame.new(-.58,1.8,0) * CFrame.Angles(math.rad(6 + 1 * math.sin(sine/12)),math.rad(-2 + 2 * math.sin(sine/12)),math.rad(5 - 1 * math.sin(sine/12))),.2)
LEFTLEGLERP.C0 = LEFTLEGLERP.C0:lerp(CFrame.new(1.2,1.3, -.12) * CFrame.Angles(math.rad(-9 + .5 * math.sin(sine/12)),math.rad(2 - 1 * math.sin(sine/12)),math.rad(-35 + 1 * math.sin(sine/12))),.2)
else
ws = 92
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(4.2 + 1 * math.sin(sine/3.5),-5 + .5 * math.sin(sine/3.5),6) * CFrame.Angles(math.rad(150 + 120 * math.sin(sine/3.5)),math.rad(30 * math.sin(sine/3.5)),math.rad(-17 * math.sin(sine/3.5))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-4.2 + 1 * math.sin(sine/3.5),-5 + .5 * math.sin(sine/3.5),6) * CFrame.Angles(math.rad(150 + 120 * -math.sin(sine/3.5)),math.rad(30 * math.sin(sine/3.5)),math.rad(-17 * math.sin(sine/3.5))),.2)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,1 * math.sin(sine/1.75),0) * CFrame.Angles(math.rad(0 + 5 * math.sin(sine/3.5)),math.rad(10 * math.sin(sine/3.5)) + Root.RotVelocity.Y / 15,math.rad(0) + Root.RotVelocity.Y / 19),.2)
LEFTARMLERP.C0 = LEFTARMLERP.C0:lerp(CFrame.new(1.5,.78,0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(4),math.rad(35)),.25)
RIGHTARMLERP.C0 = RIGHTARMLERP.C0:lerp(CFrame.new(-1.5, .78, 0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(-4),math.rad(-35)), 0.25)
RIGHTLEGLERP.C0 = RIGHTLEGLERP.C0:lerp(CFrame.new(-.58,1.8,0) * CFrame.Angles(math.rad(6 + 1 * math.sin(sine/12)),math.rad(-2 + 2 * math.sin(sine/12)),math.rad(5 - 1 * math.sin(sine/12))),.2)
LEFTLEGLERP.C0 = LEFTLEGLERP.C0:lerp(CFrame.new(1.2,1.3, -.12) * CFrame.Angles(math.rad(-9 + .5 * math.sin(sine/12)),math.rad(2 - 1 * math.sin(sine/12)),math.rad(-35 + 1 * math.sin(sine/12))),.2)
end
elseif position == "Idle" and attacking == false then
change = .5
HAND1LERP.C0 = HAND1LERP.C0:lerp(CFrame.new(4.5,-5 + .5 * math.sin(sine/14),6) * CFrame.Angles(math.rad(10 + 1 * math.sin(sine/13)),math.rad(-5 + 5 * math.sin(sine/12)),math.rad(-36 - 4 * math.sin(sine/11))),.2)
HAND2LERP.C0 = HAND2LERP.C0:lerp(CFrame.new(-5,-5 + .5 * math.sin(sine/14),6) * CFrame.Angles(math.rad(13 - 3 * math.sin(sine/12)),math.rad(36 - 3 * math.sin(sine/13)),math.rad(35 + 2 * math.sin(sine/11))),.2)
ROOTLERP.C0 = ROOTLERP.C0:lerp(CFrame.new(0,0,0) * CFrame.Angles(math.rad(0 + 5 * math.sin(sine/12)),math.rad(0 * math.sin(sine/16)),math.rad(0)),.2)
LEFTARMLERP.C0 = LEFTARMLERP.C0:lerp(CFrame.new(1.5,.78,0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(4),math.rad(35)),.25)
RIGHTARMLERP.C0 = RIGHTARMLERP.C0:lerp(CFrame.new(-1.5, .78, 0) * CFrame.Angles(math.rad(180 + 4 * math.sin(sine/12)),math.rad(-4),math.rad(-35)), 0.25)
RIGHTLEGLERP.C0 = RIGHTLEGLERP.C0:lerp(CFrame.new(-.58,1.8,0) * CFrame.Angles(math.rad(6 + 1 * math.sin(sine/12)),math.rad(-2 + 2 * math.sin(sine/12)),math.rad(5 - 1 * math.sin(sine/12))),.2)
LEFTLEGLERP.C0 = LEFTLEGLERP.C0:lerp(CFrame.new(1.2,1.3, -.12) * CFrame.Angles(math.rad(-9 + .5 * math.sin(sine/12)),math.rad(2 - 1 * math.sin(sine/12)),math.rad(-35 + 1 * math.sin(sine/12))),.2)
end
swait()
end
end)
anims()
warn("The one you fear, Made by Supr14.")
