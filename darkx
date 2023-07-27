local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "DarkX",
   LoadingTitle = "Gui Is Loading...",
   LoadingSubtitle = "Made with love popbob_tho",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "vaticanhub"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "NN|Key",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided",
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local MainTab = Window:CreateTab("Main", 4483362458) -- Title, Image
local MainSection = MainTab:CreateSection("Script's")
Rayfield:Notify({
   Title = "You succesfully executed the script",
   Content = "Gui made with love",
   Duration = 5,
   Image = nil,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "Cool i guess",
         Callback = function()
         print("The user tapped Okay!")
      end
   },
},

})

local Button = MainTab:CreateButton({
   Name = "Click Fling Gui",
   Callback = function()
loadstring(game:HttpGet(('https://raw.githubusercontent.com/0Ben1/fe/main/obf_5wpM7bBcOPspmX7lQ3m75SrYNWqxZ858ai3tJdEAId6jSI05IOUB224FQ0VSAswH.lua.txt'),true))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "Infinite Yield (Admin)",
   Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
   end,
})
local Button = MainTab:CreateButton({
   Name = "Simple Spy",
   Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/exxtremestuffs/SimpleSpySource/master/SimpleSpy.lua"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "Dex Explorer V5",
   Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/infyiff/backup/main/dex.lua"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "Chat Bypass",
   Callback = function()
loadstring(game:HttpGet("https://scriptblox.com/raw/Universal-Script-Chat-Bypasser-Not-Made-By-Me-9451"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "FE BTools",
   Callback = function()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer

if not getgenv().Network then
	getgenv().Network = {
		BaseParts = {};
		FakeConnections = {};
		Connections = {};
		Output = {
			Enabled = true;
			Prefix = "[NETWORK] ";
			Send = function(Type,Output,BypassOutput)
				if typeof(Type) == "function" and (Type == print or Type == warn or Type == error) and typeof(Output) == "string" and (typeof(BypassOutput) == "nil" or typeof(BypassOutput) == "boolean") then
					if Network["Output"].Enabled == true or BypassOutput == true then
						Type(Network["Output"].Prefix..Output);
					end;
				elseif Network["Output"].Enabled == true then
					error(Network["Output"].Prefix.."Output Send Error : Invalid syntax.");
				end;
			end;
		};
		CharacterRelative = false;
	}

	Network["Output"].Send(print,": Loading.")
	Network["Velocity"] = Vector3.new(14.46262424,14.46262424,14.46262424); --exactly 25.1 magnitude
	Network["RetainPart"] = function(Part,ReturnFakePart) --function for retaining ownership of unanchored parts
		assert(typeof(Part) == "Instance" and Part:IsA("BasePart") and Part:IsDescendantOf(workspace),Network["Output"].Prefix.."RetainPart Error : Invalid syntax: Arg1 (Part) must be a BasePart which is a descendant of workspace.")
		assert(typeof(ReturnFakePart) == "boolean" or typeof(ReturnFakePart) == "nil",Network["Output"].Prefix.."RetainPart Error : Invalid syntax: Arg2 (ReturnFakePart) must be a boolean or nil.")
		if not table.find(Network["BaseParts"],Part) then
			if Network.CharacterRelative == true then
				local Character = LocalPlayer.Character
				if Character and Character.PrimaryPart then
					local Distance = (Character.PrimaryPart.Position-Part.Position).Magnitude
					if Distance > 1000 then
						Network["Output"].Send(warn,"RetainPart Warning : PartOwnership not applied to BasePart "..Part:GetFullName()..", as it is more than "..gethiddenproperty(LocalPlayer,"MaximumSimulationRadius").." studs away.")
						return false
					end
				else
					Network["Output"].Send(warn,"RetainPart Warning : PartOwnership not applied to BasePart "..Part:GetFullName()..", as the LocalPlayer Character's PrimaryPart does not exist.")
					return false
				end
			end
			table.insert(Network["BaseParts"],Part)
			Part.CustomPhysicalProperties = PhysicalProperties.new(0,0,0,0,0)
			Network["Output"].Send(print,"PartOwnership Output : PartOwnership applied to BasePart "..Part:GetFullName()..".")
			if ReturnFakePart == true then
				return FakePart
			end
		else
			Network["Output"].Send(warn,"RetainPart Warning : PartOwnership not applied to BasePart "..Part:GetFullName()..", as it already active.")
			return false
		end
	end

	Network["RemovePart"] = function(Part) --function for removing ownership of unanchored part
		assert(typeof(Part) == "Instance" and Part:IsA("BasePart"),Network["Output"].Prefix.."RemovePart Error : Invalid syntax: Arg1 (Part) must be a BasePart.")
		local Index = table.find(Network["BaseParts"],Part)
		if Index then
			table.remove(Network["BaseParts"],Index)
			Network["Output"].Send(print,"RemovePart Output: PartOwnership removed from BasePart "..Part:GetFullName()..".")
		else
			Network["Output"].Send(warn,"RemovePart Warning : BasePart "..Part:GetFullName().." not found in BaseParts table.")
		end
	end

	Network["SuperStepper"] = Instance.new("BindableEvent") --make super fast event to connect to
	for _,Event in pairs({RunService.Stepped,RunService.Heartbeat}) do
		Event:Connect(function()
			return Network["SuperStepper"]:Fire(Network["SuperStepper"],tick())
		end)
	end

	Network["PartOwnership"] = {};
	Network["PartOwnership"]["PreMethodSettings"] = {};
	Network["PartOwnership"]["Enabled"] = false;
	Network["PartOwnership"]["Enable"] = coroutine.create(function() --creating a thread for network stuff
		if Network["PartOwnership"]["Enabled"] == false then
			Network["PartOwnership"]["Enabled"] = true --do cool network stuff before doing more cool network stuff
			Network["PartOwnership"]["PreMethodSettings"].ReplicationFocus = LocalPlayer.ReplicationFocus
			LocalPlayer.ReplicationFocus = workspace
			Network["PartOwnership"]["PreMethodSettings"].SimulationRadius = gethiddenproperty(LocalPlayer,"SimulationRadius")
			Network["PartOwnership"]["Connection"] = Network["SuperStepper"].Event:Connect(function() --super fast asynchronous loop
				sethiddenproperty(LocalPlayer,"SimulationRadius",1/0)
				for _,Part in pairs(Network["BaseParts"]) do --loop through parts and do network stuff
					coroutine.wrap(function()
						if Part:IsDescendantOf(workspace) then
							if Network.CharacterRelative == true then
								local Character = LocalPlayer.Character;
								if Character and Character.PrimaryPart then
									local Distance = (Character.PrimaryPart.Position - Part.Position).Magnitude
									if Distance > 1000 then
										Network["Output"].Send(warn,"PartOwnership Warning : PartOwnership not applied to BasePart "..Part:GetFullName()..", as it is more than "..gethiddenproperty(LocalPlayer,"MaximumSimulationRadius").." studs away.")
										Lost = true;
										Network["RemovePart"](Part)
									end
								else
									Network["Output"].Send(warn,"PartOwnership Warning : PartOwnership not applied to BasePart "..Part:GetFullName()..", as the LocalPlayer Character's PrimaryPart does not exist.")
								end
							end
							Part.Velocity = Network["Velocity"]+Vector3.new(0,math.cos(tick()*10)/100,0) --keep network by sending physics packets of 30 magnitude + an everchanging addition in the y level so roblox doesnt get triggered and fuck your ownership
						else
							Network["RemovePart"](Part)
						end
					end)()
				end
			end)
			Network["Output"].Send(print,"PartOwnership Output : PartOwnership enabled.")
		else
			Network["Output"].Send(warn,"PartOwnership Output : PartOwnership already enabled.")
		end
	end)
	Network["PartOwnership"]["Disable"] = coroutine.create(function()
		if Network["PartOwnership"]["Connection"] then
			Network["PartOwnership"]["Connection"]:Disconnect()
			LocalPlayer.ReplicationFocus = Network["PartOwnership"]["PreMethodSettings"].ReplicationFocus
			sethiddenproperty(LocalPlayer,"SimulationRadius",Network["PartOwnership"]["PreMethodSettings"].SimulationRadius)
			Network["PartOwnership"]["PreMethodSettings"] = {}
			for _,Part in pairs(Network["BaseParts"]) do
				Network["RemovePart"](Part)
			end
			Network["PartOwnership"]["Enabled"] = false
			Network["Output"].Send(print,"PartOwnership Output : PartOwnership disabled.")
		else
			Network["Output"].Send(warn,"PartOwnership Output : PartOwnership already disabled.")
		end
	end)
	Network["Output"].Send(print,": Loaded.")
end

coroutine.resume(Network["PartOwnership"]["Enable"])

player = game:GetService("Players").LocalPlayer
Gui = player.PlayerGui
Backpack = player.Backpack
Mouse = player:GetMouse()

Parts_Folder = Instance.new("Folder",workspace)

for i, Hat in pairs(player.Character:GetChildren()) do
	if Hat:IsA("Accessory") then
		local Part = Instance.new("Part",Parts_Folder)
		Part.Name = Hat.Name
		Part.Anchored = true
		Part.Size = Hat.Handle.Size
		Part.Position = player.Character.Head.Position + Vector3.new(math.random(-5,5),math.random(-1,1),math.random(-5,5))
		Part:SetAttribute("Moveable",true)
		Part.Material = Enum.Material.SmoothPlastic
		Part.CanCollide = false
        Part.Color = Color3.new(1,0,0)
	end
end


Move_Tool = Instance.new("Tool",Backpack)
Rotate_Tool = Instance.new("Tool",Backpack)
MHandle = Instance.new("Part",Move_Tool)
RHandle = Instance.new("Part",Rotate_Tool)
Mgrabs = Instance.new("Handles",Gui)
Rgrabs = Instance.new("ArcHandles",Gui)
Outline = Instance.new("Highlight")

Move_Tool.Name = "Move"
Move_Tool.CanBeDropped = false

Rotate_Tool.Name = "Rotate"
Rotate_Tool.CanBeDropped = false

MHandle.Name = "Handle"
MHandle.Transparency = 1

RHandle.Name = "Handle"
RHandle.Transparency = 1

Mgrabs.Visible = false
Mgrabs.Color3 = Color3.fromRGB(248, 236, 0)
Mgrabs.Style = "Movement"

Rgrabs.Visible = false

Outline.FillTransparency = 1
Outline.OutlineTransparency = 0

Active_Part = nil

Move_Tool.Equipped:Connect(function()
	if Active_Part ~= nil then
		Mgrabs.Visible = true
		Mgrabs.Adornee = Active_Part
	end
end)

Move_Tool.Unequipped:Connect(function()
	Mgrabs.Visible = false
	Mgrabs.Adornee = nil
end)

Move_Tool.Activated:Connect(function()
	if Mouse.Target:GetAttribute("Moveable") then
		Active_Part = Mouse.Target
		Mgrabs.Visible = true
		Mgrabs.Adornee = Active_Part
		Outline.Parent = Active_Part
	end
end)

Rotate_Tool.Equipped:Connect(function()
	if Active_Part ~= nil then
		Rgrabs.Visible = true
		Rgrabs.Adornee = Active_Part
	end
end)

Rotate_Tool.Unequipped:Connect(function()
	Rgrabs.Visible = false
	Rgrabs.Adornee = nil
end)

Rotate_Tool.Activated:Connect(function()
	if Mouse.Target:GetAttribute("Moveable") then
		Active_Part = Mouse.Target
		Rgrabs.Visible = true
		Rgrabs.Adornee = Active_Part
		Outline.Parent = Active_Part
	end
end)

MOGCFrame = CFrame.new()

Mgrabs.MouseButton1Down:Connect(function()
	MOGCFrame = Active_Part.CFrame
end)

Mgrabs.MouseDrag:Connect(function(knob, pos)
	if knob == Enum.NormalId.Front then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.LookVector * pos
	end
	if knob == Enum.NormalId.Back then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.LookVector * -pos
	end
	if knob == Enum.NormalId.Top then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.UpVector * pos
	end
	if knob == Enum.NormalId.Bottom then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.UpVector * -pos
	end
	if knob == Enum.NormalId.Left then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.RightVector * -pos
	end
	if knob == Enum.NormalId.Right then
		Active_Part.CFrame = MOGCFrame + MOGCFrame.RightVector * pos
	end
end)

ROGCFrame = CFrame.new()

Rgrabs.MouseButton1Down:Connect(function()
	ROGCFrame = Active_Part.CFrame
end)

Rgrabs.MouseDrag:Connect(function(knob, angle)
	if knob == Enum.Axis.Y then
		Active_Part.CFrame = ROGCFrame * CFrame.Angles(0,angle,0)
	end
	if knob == Enum.Axis.X then
		Active_Part.CFrame = ROGCFrame * CFrame.Angles(angle,0,0)
	end
	if knob == Enum.Axis.Z then
		Active_Part.CFrame = ROGCFrame * CFrame.Angles(0,0,angle)
	end
end)

game:GetService("StarterGui"):SetCore("SendNotification",{
	Title = "FE BTools V3 Loaded",
	Text = "Made by rouxhaver",
	Icon = "rbxassetid://12561999923"
})
game:GetService("StarterGui"):SetCore("SendNotification",{
	Title = "Network Credit:",
	Text = "thanks to 4eyes for network stuff",
	Icon = "rbxassetid://12562053596"
})

HRP = player.Character.HumanoidRootPart

for i, Part in pairs(Parts_Folder:GetChildren()) do
	local Hat = player.Character[Part.Name].Handle
	Hat.AccessoryWeld:Destroy()
    Network.RetainPart(Hat)
	local vbreak = false
	coroutine.wrap(function()
		while task.wait() do
			if vbreak == true then break end
			Hat.CFrame = Part.CFrame
		end
	end)()
	Hat:FindFirstChildWhichIsA("SpecialMesh"):Destroy()
end

player.Character.Humanoid:GetPropertyChangedSignal("Health"):Connect(function()
	Parts_Folder:Destroy()
end)
   end,

local Button = MainTab:CreateButton({
   Name = "Player Liftig Script",
   Callback = function()

player = game:GetService("Players").LocalPlayer
mouse = player:GetMouse()
camera = workspace.CurrentCamera
ts = game:GetService("TweenService")

function createtween(part, cframe,ttime)
 local tweeninfo = TweenInfo.new(ttime)
 tween = ts:Create(part, tweeninfo, {CFrame = cframe})
 tween:Play()
 tween.Completed:Wait()
end

outline = Instance.new("Highlight")

target = nil

mouse.Button1Up:Connect(function()
 if mouse.Target then
  local model = mouse.Target:FindFirstAncestorOfClass("Model")
  if model and model:FindFirstChild("Humanoid") then do
    camera.CameraSubject = model.Humanoid
    target = model
   end else
   outline.Parent = nil
  end
 end
end)

game:GetService("RunService").RenderStepped:Connect(function()
 if player.Character:FindFirstChild("HumanoidRootPart") then
  player.Character.HumanoidRootPart.Velocity = Vector3.new(0,0,0)
  if target and target:FindFirstChild("HumanoidRootPart") then
   if target.HumanoidRootPart.CFrame.Y + 20 < player.Character.HumanoidRootPart.CFrame.Y then
    tween:Cancel()
   end
  end
 end
 if mouse.Target then
  local model = mouse.Target:FindFirstAncestorOfClass("Model")
  if model and model:FindFirstChild("Humanoid") then do
    outline.Parent = model
   end else
   outline.Parent = nil
  end
 end
end)

while task.wait() do
 if target ~= nil and target:FindFirstAncestorOfClass("Workspace") and target ~= player.Character and player.Character:FindFirstChild("HumanoidRootPart") and target:FindFirstChild("HumanoidRootPart") then
  character = player.Character
  hrp = character.HumanoidRootPart
  thrp = target.HumanoidRootPart
  hrp.CFrame = thrp.CFrame * CFrame.Angles(math.rad(90),0,0) + thrp.CFrame.UpVector * -10
 end
 if target ~= nil and target:FindFirstAncestorOfClass("Workspace") and target ~= player.Character and player.Character:FindFirstChild("HumanoidRootPart") and target:FindFirstChild("HumanoidRootPart") then
  character = player.Character
  hrp = character.HumanoidRootPart
  thrp = target.HumanoidRootPart
  rot = thrp.CFrame*CFrame.Angles(math.rad(25),math.rad(25),math.rad(25))
  createtween(hrp, thrp.CFrame * CFrame.Angles(math.rad(90),0,0) + thrp.CFrame.UpVector * 1000000, 100000)
 end
end
   end,
})

local Button = MainTab:CreateButton({
   Name = "Rizz Gui",
   Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/mikhailramlal/Rizzer/main/main"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "Auto Excuse",
   Callback = function()
getgenv().dmsgs = {
  deathmessages = {"i was lagging", "that wasnt fair", "You will pay for this", "What a noob", "I will not let you get away with that", "Are you serious dude", "You will regret this", "That is a grave mistake", "I will make you suffer you little ****", "You son of a ****", "Are you out of your mind", "What the hell is wrong with you","I will find you","That isn't nice dude","Karma will hit you back"}
}

loadstring(game:HttpGet("https://raw.githubusercontent.com/goldmoments/auto-excuse/main/Script"))("Auto-Excuse Script | flamespill#7488") 
   end,
})

local Button = MainTab:CreateButton({
   Name = "Hacker Chat",
   Callback = function()
--[[
Made by Rouxhaver
When two people execute the script they can use the text box to chat with each other privately and uncensored
Note: only works on the newer bubble chat and not the old one and long messages get tagged
]]

a = "的"
b = "一"
c = "是"
d = "不"
e = "了"
f = "人"
g = "我"
h = "在"
i = "有"
j = "他"
k = "这"
l = "为"
m = "之"
n = "大"
o = "来"
p = "以"
q = "个"
r = "中"
s = "上"
t = "们"
u = "到"
v = "说"
w = "国"
x = "和"
y = "地"
z = "也"

function convert(str)
 str = str:lower()
 return str:gsub("a",a):gsub("b",b):gsub("c",c):gsub("d",d):gsub("e",e):gsub("f",f):gsub("g",g):gsub("h",h):gsub("i",i):gsub("j",j):gsub("k",k):gsub("l",l):gsub("m",m):gsub("n",n):gsub("o",o):gsub("p",p):gsub("q",q):gsub("r",r):gsub("s",s):gsub("t",t):gsub("u",u):gsub("v",v):gsub("w",w):gsub("x",x):gsub("y",y):gsub("z",z)
end

function unconvert(str)
 str = str:lower()
 return str:gsub(a,"a"):gsub(b,"b"):gsub(c,"c"):gsub(d,"d"):gsub(e,"e"):gsub(f,"f"):gsub(g,"g"):gsub(h,"h"):gsub(i,"i"):gsub(j,"j"):gsub(k,"k"):gsub(l,"l"):gsub(m,"m"):gsub(n,"n"):gsub(o,"o"):gsub(p,"p"):gsub(q,"q"):gsub(r,"r"):gsub(s,"s"):gsub(t,"t"):gsub(u,"u"):gsub(v,"v"):gsub(w,"w"):gsub(x,"x"):gsub(y,"y"):gsub(z,"z")
end

function chat(str)
 game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(str,"All")
end

player = game:GetService("Players").LocalPlayer

SG = Instance.new("ScreenGui",player.PlayerGui)

frame = Instance.new("Frame",SG)
frame.Size = UDim2.new(0.2,0,0.2,0)
frame.AnchorPoint = Vector2.new(0.5,0.5)
frame.Position = UDim2.new(0.5,0,0.8,0)
frame.Active = true
frame.Draggable = true
frame.BackgroundColor3 = Color3.new(0.14902, 0.8, 1)

textbox = Instance.new("TextBox",frame)
textbox.AnchorPoint = Vector2.new(0.5,0.5)
textbox.Size = UDim2.new(0.95,0,0.65,0)
textbox.Position = UDim2.new(0.5,0,0.6,0)
textbox.TextScaled = true
textbox.BackgroundColor3 = Color3.new(1,1,1)
textbox.Text = "Text"
textbox.TextColor3 = Color3.new(0, 0, 0)

title = Instance.new("TextLabel",frame)
title.Size = UDim2.new(0.3,0,0.3,0)
title.TextScaled = true
title.Text = "hacker chat"
title.BackgroundTransparency = 1
title.TextColor3 = Color3.new(0, 0, 0)

closebutton = Instance.new("TextButton",frame)
closebutton.Size = UDim2.new(0.15,0,0.25,0)
closebutton.AnchorPoint = Vector2.new(1,0)
closebutton.TextScaled = true
closebutton.BackgroundColor3 = Color3.new(1, 0, 0.0156863)
closebutton.Text = "X"
closebutton.Position = UDim2.new(1,0,0,0)
closebutton.TextColor3 = Color3.new(1, 1, 1)

ui = Instance.new("UIAspectRatioConstraint",frame)
ui.AspectRatio = 4

closebutton.MouseButton1Up:Connect(function()
 SG:Destroy()
end)

textbox.FocusLost:Connect(function()
 chat("三"..convert(textbox.Text))
end)

player.PlayerGui.Chat.Frame.ChatChannelParentFrame.Frame_MessageLogDisplay.Scroller.ChildAdded:Connect(function(msg)
 wait(1)
 local message = msg.TextLabel.Text
 if message:match("三") then
  msg.TextLabel.TextColor3 = Color3.new(1, 0.85098, 0)
  message = unconvert(message:gsub("三",""))
  msg.TextLabel.Text = message
 end
end)

Coregui = game:GetService("CoreGui")
if Coregui:FindFirstChild("BubbleChat") then
 Coregui.BubbleChat.DescendantAdded:Connect(function(bubble)
  wait(1)
  if bubble:IsA("TextLabel") then
   if bubble.Text:match("三") then
    bubble.Parent.BackgroundColor3 = Color3.new(1, 0.85098, 0)
    bubble.Text = unconvert(bubble.Text:gsub("三",""))
   end
  end
 end)
end
   end,
})

local BloxFruitTab = Window:CreateTab("BloxFruit", 4483362458) -- Title, Image
local MainSection = BloxFruitTab:CreateSection("Fighting Styles")

local Slider = MainTab:CreateSlider({
   Name = "Walk Speed",
   Range = {0, 300},
   Increment = 1,
   Suffix = "Speed",
   CurrentValue = 16,
   Flag = "vaticanhub", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end,
})

local Dropdown = MainTab:CreateDropdown({
   Name = "Select Are",
   Options = {"Pirate Island","Starters Islands"},
   CurrentOption = {"Option 1"},
   MultipleOptions = true,
   Flag = "teleport", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Option)

   end,
})

local Button = BloxFruitTab:CreateButton({
   Name = "Electric",
   Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro")
   end,
})

local Button = BloxFruitTab:CreateButton({
   Name = "Water KungFu",
   Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
   end,
})

local Button = BloxFruitTab:CreateButton({
   Name = "Dark Step",
   Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
   end,
})

local Button = BloxFruitTab:CreateButton({
   Name = "Dragon Breath",
   Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
   end,
})

local MainSection = BloxFruitTab:CreateSection("Other Op Script's")


local Button = BloxFruitTab:CreateButton({
   Name = "Blox Fruits Hub",
   Callback = function()
loadstring(game:HttpGet("https://gist.githubusercontent.com/noob1ee1/5607f21c9874e3724f13a88109916896/raw/5a44dc988657f4eb23294b60aa64b874bc13253b"))()
   end,
})

local Button = BloxFruitTab:CreateButton({
   Name = "Tawan X",
   Callback = function()
loadstring(game:HttpGet("https://scriptblox.com/raw/Blox-Fruits-Tawan-X-Hub-11624"))()
   end,
})

local ArmWrestleTab = Window:CreateTab("Arm Wrestle Sim", 4483362458) -- Title, Image

local Button = ArmWrestleTab:CreateButton({
   Name = "Skull Hub",
   Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/zicus-scripts/SkullHub/main/Loader.lua"))()
   end,
})

local ArmTab = Window:CreateTab("Arm Wrestler Simulator", 4483362458)

local Button = ArmTab:CreateButton({
   Name = "Inf Cash Inf Stat's",
   Callback = function()
game:GetService("ReplicatedStorage").strength:FireServer(-math.huge,1) -- just execute them all idc also this one makes you elon musk

local args = {
    [1] = math.huge
}

workspace:WaitForChild("Main3"):WaitForChild("RemoteEvent"):FireServer(unpack(args)) -- this one makes you a muscle head with no brains just raw power

local args = {
    [1] = math.huge
}

workspace:WaitForChild("Main2"):WaitForChild("RemoteEvent"):FireServer(unpack(args)) -- this one makes you a muscle head with no brains just raw power

local args = {
    [1] = 92233720350859370 -- don't cange this it might go negative if you go higher
}

workspace:WaitForChild("Main"):WaitForChild("RemoteEvent"):FireServer(unpack(args))
   end,
})

local BrookTab = Window:CreateTab("BrookHaven RP", 4483362458) -- Title, Image

local Button = BrookTab:CreateButton({
   Name = "GamePass Unlocker",
   Callback = function()
loadstring(game:HttpGet("https://scriptblox.com/raw/Brookhaven-RP-IceHub-Brookhaven-GamePass-Unlocker-9412"))()
   end,
})

local Button = BrookTab:CreateButton({
   Name = "IceHub",
   Callback = function()
loadstring(game:HttpGet("https://scriptblox.com/raw/Brookhaven-RP-IceHub-Brookhaven-8460"))()
   end,
})

