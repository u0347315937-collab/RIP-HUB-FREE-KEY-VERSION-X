local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "R.I.P. GUI free version",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Rayfield Interface Suite",
   LoadingSubtitle = "Slovak123456gg's team",
   ShowText = "Rayfield", -- for mobile users to unhide Rayfield, change if you'd like
   Theme = "Serenity", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   ToggleUIKeybind = "K", -- The keybind to toggle the UI visibility (string like "K" or Enum.KeyCode)

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from emitting warnings when the script has a version mismatch with the interface.

   -- ScriptID = "sid_xxxxxxxxxxxx", -- Your Script ID from developer.sirius.menu — enables analytics, managed keys, and script hosting

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include Discord.gg/. E.g. Discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the Discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "WDYM V.2 KEY SYSTEM",
      Subtitle = "very easy key system",
      Note = "its very easy its my site no junkie work ink or loottabs", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique, as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"12341-sdawa-hkshdjuau-.3479"} -- List of keys that the system will accept, can be RAW file links (pastebin, github, etc.) or simple strings ("hello", "key22")
   }
})
local main = Window:CreateTab("Main", 4483362458) -- Title, Image
local plcr = Window:CreateTab("Player", 4483362458) -- Title, Image
local comb = Window:CreateTab("Combat", 4483362458) -- Title, Image
local misc = Window:CreateTab("Misc", 4483362458) -- Title, Image
local Button = main:CreateButton({
   Name = "Destroy hub",
   Callback = function()
   Rayfield:Destroy()
   end,
})
local Button = main:CreateButton({
   Name = "Walk fling",
   Callback = function()
   --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
loadstring(game:HttpGet("https://pastebin.com/raw/r0G5gYqC"))("t.me/ByteScripts") 
   end,
})
local Button = main:CreateButton({
   Name = "fly",
   Callback = function()
   --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
loadstring(game:HttpGet("https://raw.githubusercontent.com/Dxnnyyyh148888/Fly-gui/refs/heads/main/Hhhhh"))()
   end,
})
local Slider = plcr:CreateSlider({
	Name = "walkspeed",
	Range = {1, 1000 },
	Increment = 1,
	Suffix = "ws",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local plrs = game.Players
 local plr = plrs.LocalPlayer
 walkspeed = Value;
 if plr then
  local char = plr.Character or plr.CharacterAdded:Wait()
   if char then
    local hum = char:FindFirstChildOfClass("Humanoid")
     if hum then
      hum.WalkSpeed = walkspeed
     end
   end
 end
	end,
})
local Slider = plcr:CreateSlider({
	Name = "jumppower",
	Range = {16, 516},
	Increment = 1,
	Suffix = "jp",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end,
})
local Toggle = plcr:CreateToggle({
	Name = "Inf-Jump",
	CurrentValue = false,
	Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local InfiniteJumpEnabled = Value
 game:GetService("UserInputService").JumpRequest:Connect(function()
  if InfiniteJumpEnabled then
   game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
  end
 end)
	end,
})
local Label = comb:CreateLabel("--ADVANCED KEY VERSION NEEDED", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme
local Label = misc:CreateLabel("--ADVANCED KEY VERSION NEEDED", 4483362458, Color3.fromRGB(255, 255, 255), false) -- Title, Icon, Color, IgnoreTheme
local Button = comb:CreateButton({
   Name = "LAUNCH ADVANCED VERSION",
   Callback = function() 
   setclipboard("https://sites.google.com/view/slovak123456ggskeysystem/domov")
   game:GetService("StarterGui"):SetCore("SendNotification",{
Title = "KEY kink has been copied to clipboard!",
Text = "ITS EASY!", 

Button1 = "Ok",
Duration = 30 
})
   local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
	Name = "R.I.P. ADVANCED GUI",
	LoadingTitle = "Slovaks Team Project Hub",
	LoadingSubtitle = "By Slovak123456gg's team",
	ConfigurationSaving = {
		Enabled = true,
		FolderName = "wtf hub",
		FileName = "virus.stealer777"
	},
	KeySystem = true,  
	KeySettings = {
		Title = "R.I.P. HUB KEY SYSTEM",
		Subtitle = "Slovak123456gg's Key System",
		Note = "its easy",
		SaveKey = true,
		Key = {"12341-sdawa-hkshdjuau-.3479"}
	}
})

Rayfield:Notify("Loaded!", "hi", 4483362458) -- Notfication -- Title, Content, Image
--Setting tabs
local cred = Window:CreateTab("Credits", 4483362458)
local comb = Window:CreateTab("Combat", 4483362458)
local plrc = Window:CreateTab("Player", 4483362458)
local misc = Window:CreateTab("Misc", 4483362458)
local FE = Window:CreateTab("FE", 4483362458)
 -- Title, Image
--Credits
local Section = cred:CreateSection("Credits")
local Paragraph = cred:CreateParagraph({Title = "Credits", Content = "Maded by Slovak123456gg's team"})
--Combat
local Button = comb:CreateButton({
	Name = "ESP",
	Callback = function()
 loadstring(game:HttpGet('https://pastebin.com/raw/yxpZ41xf'))()
 end,
})
local Button = comb:CreateButton({
 Name = "Aimlock",
 Callback = function()
 loadstring(game:HttpGet('https://pastebin.com/raw/NU9gz4yq'))()
 end,
})
--Player
local Slider = plrc:CreateSlider({
	Name = "walkspeed",
	Range = {1, 1000 },
	Increment = 1,
	Suffix = "ws",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local plrs = game.Players
 local plr = plrs.LocalPlayer
 walkspeed = Value;
 if plr then
  local char = plr.Character or plr.CharacterAdded:Wait()
   if char then
    local hum = char:FindFirstChildOfClass("Humanoid")
     if hum then
      hum.WalkSpeed = walkspeed
     end
   end
 end
	end,
})
local Slider = plrc:CreateSlider({
	Name = "jumppower",
	Range = {16, 516},
	Increment = 1,
	Suffix = "jp",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end,
})
local Toggle = plrc:CreateToggle({
	Name = "Inf-Jump",
	CurrentValue = false,
	Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local InfiniteJumpEnabled = Value
 game:GetService("UserInputService").JumpRequest:Connect(function()
  if InfiniteJumpEnabled then
   game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
  end
 end)
	end,
})
local Button = plrc:CreateButton({
 	Name = "Fly",
 	Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
  end
})
local Noclip = nil
local Clip = nil

function noclip()
	Clip = false
	local function Nocl()
		if Clip == false and game.Players.LocalPlayer.Character ~= nil then
			for _,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
				if v:IsA('BasePart') and v.CanCollide and v.Name ~= floatName then
					v.CanCollide = false
				end
			end
		end
		wait(0.21) -- basic optimization
	end
	Noclip = game:GetService('RunService').Stepped:Connect(Nocl)
end

function clip()
	if Noclip then Noclip:Disconnect() end
	Clip = true
end

local Button = plrc:CreateButton({
 	Name = "Noclip",
 	Callback = function()
  noclip()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Infinity Yield",
 	Callback = function()
  loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "F3X (btools)",
 	Callback = function()
  loadstring(game:GetObjects("rbxassetid://6695644299")[1].Source)()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Fake Lag",
 	Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/Biem6ondo/FAKELAG/refs/heads/main/Fakelag"))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "R6 Anim Hub",
 	Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/ExploitFin/AquaMatrix/refs/heads/AquaMatrix/AquaMatrix"))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Destroy hub",
 	Callback = function()
  Rayfield:Destroy()
  Rayfield:Notify({
   Title = "Notification Title",
   Content = "Notification Content",
   Duration = 6.5,
   Image = 4483362458,
})
  end,
})
local Button = FE:CreateButton({
 	Name = "Invisibility",
 	Callback = function()
   loadstring(game:HttpGet("https://pastebin.com/raw/3Rnd9rHf"))()
  end
})
local Button = FE:CreateButton({
 	Name = "Universal Dropkick",
 	Callback = function()
   loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-THE-REAL-dropkick-177199"))()
  end
})
local Button = FE:CreateButton({
 	Name = "Vexro Emotes",
 	Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/zyrovell/Vexro/main/vexroemotes.lua"))()
  end
})
local Button = comb:CreateButton({
 	Name = "Npc kill aura (TOOL REQUIRED)",
 	Callback = function()
   --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
-- KillSwitch v2 — GUI mejorada + spam en rango optimizado
-- Arranca OFF por defecto, pero lo podés cambiar.
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local task = task

-- ===== CONFIG =====
local START_ENABLED = false        -- true = arranca activado; false = arranca apagado
local DEFAULT_KEY = Enum.KeyCode.K -- tecla por defecto para toggle
local DEFAULT_RANGE = 8            -- rango por defecto
local AUTOCLOSE_GUI_SEC = 0        -- >0 oculta GUI automáticamente tras esos segundos (0 = nunca)
local LOOP_INTERVAL = 0.06         -- tiempo entre escaneos (segundos). Ajustalo si querés menos lag / más responsivo
local SPAM_WAIT = 0.03             -- espera entre intentos de Activate() en el spam loop
-- ==================

local enabled = START_ENABLED
local range = DEFAULT_RANGE
local hotkey = DEFAULT_KEY

local loopRunning = false
local loopThread = nil

local original_firetouch = firetouchinterest
local patchedTools = {} -- map tool -> {origActivate = fn}
local function noop_firetouch(...) end

-- spam control (visibles para doRangeHit)
local spamTask = nil
local spamActive = false

-- doRangeHit: detecta targets, hace firetouchinterest y controla spam de tool:Activate()
local function doRangeHit()
    local p = Players:GetPlayers()
    local tool = player.Character and player.Character:FindFirstChildOfClass("Tool")
    local anyTarget = false

    if tool and tool:FindFirstChild("Handle") then
        -- buscar si hay al menos un objetivo en rango y aplicar firetouchinterest sobre partes
        for i = 1, #p do
            local other = p[i]
            if other ~= player then
                local v = other.Character
                if v and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v:FindFirstChild("HumanoidRootPart") then
                    local ok, dist = pcall(function()
                        return player:DistanceFromCharacter(v.HumanoidRootPart.Position)
                    end)
                    if ok and dist and dist <= range then
                        anyTarget = true
                        for _, part in next, v:GetChildren() do
                            if part:IsA("BasePart") then
                                pcall(function()
                                    firetouchinterest(tool.Handle, part, 0)
                                    firetouchinterest(tool.Handle, part, 1)
                                end)
                            end
                        end
                    end
                end
            end
        end
    end

    -- manejar el spam: arrancar cuando aparece objetivo; parar cuando no hay
    if anyTarget and tool and tool.Parent == player.Character and enabled then
        if not spamActive then
            spamActive = true
            spamTask = task.spawn(function()
                -- este loop spamea Activate() tan rápido como el engine lo permita con una pequeña espera entre intentos
                while enabled and spamActive and tool and tool.Parent == player.Character do
                    pcall(function() tool:Activate() end)
                    task.wait(SPAM_WAIT)
                end
            end)
        end
    else
        spamActive = false
        spamTask = nil
    end
end

-- loop de ejecución controlado (optimizado para menos lag)
local function connectLoop()
    if loopRunning then return end
    loopRunning = true
    loopThread = task.spawn(function()
        while loopRunning do
            if enabled then
                pcall(doRangeHit)
            end
            task.wait(LOOP_INTERVAL)
        end
    end)
end

local function disconnectLoop()
    loopRunning = false
    loopThread = nil
end

-- Parcheo de Tool:Activate para evitar activaciones locales
local function patchToolActivate(tool)
    if not tool or patchedTools[tool] then return end
    local ok, orig = pcall(function() return tool.Activate end)
    if ok then
        patchedTools[tool] = {origActivate = orig}
        pcall(function()
            tool.Activate = function() end
        end)
    end
end

local function restoreToolActivate(tool)
    if not tool or not patchedTools[tool] then return end
    local data = patchedTools[tool]
    pcall(function()
        tool.Activate = data.origActivate
    end)
    patchedTools[tool] = nil
end

local function patchAllToolsInPlayer()
    -- patch tools in Backpack and Character
    local backpack = player:FindFirstChildOfClass("Backpack")
    if backpack then
        for _, t in pairs(backpack:GetChildren()) do
            if t:IsA("Tool") then patchToolActivate(t) end
        end
    end
    if player.Character then
        for _, t in pairs(player.Character:GetChildren()) do
            if t:IsA("Tool") then patchToolActivate(t) end
        end
    end
end

local function restoreAllTools()
    for tool, _ in pairs(patchedTools) do
        restoreToolActivate(tool)
    end
end

-- Activar / Desactivar con manejo de parches
local function enableNow()
    enabled = true
    if original_firetouch then firetouchinterest = original_firetouch end
    restoreAllTools()
    connectLoop()
    pcall(function() player:SetAttribute("KillSwitchEnabled", true) end)
    print("[KillSwitch] ACTIVADO")
end

local function disableNow()
    enabled = false
    firetouchinterest = noop_firetouch
    patchAllToolsInPlayer()
    -- parar spam inmediatamente
    spamActive = false
    spamTask = nil
    disconnectLoop()
    pcall(function() player:SetAttribute("KillSwitchEnabled", false) end)
    print("[KillSwitch] DESACTIVADO (firetouch bloqueado, Tool.Activate parcheado)")
end

-- Exponer funciones globales para control por consola/otros scripts (útil en Studio)
_G.killSwitchEnable = enableNow
_G.killSwitchDisable = disableNow
_G.killSwitchToggle = function() if enabled then disableNow() else enableNow() end end

-- ========== GUI ==========
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "KillSwitchGui"
screenGui.ResetOnSpawn = false
screenGui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,260,0,150)
frame.Position = UDim2.new(0,12,0,12)
frame.BackgroundTransparency = 0.2
frame.Parent = screenGui
frame.Active = true
frame.Draggable = true

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1,0,0,28)
title.Position = UDim2.new(0,0,0,0)
title.BackgroundTransparency = 1
title.Text = "KillSwitch (Studio)"
title.Font = Enum.Font.GothamBold
title.TextScaled = true
title.Parent = frame

local status = Instance.new("TextLabel")
status.Size = UDim2.new(1,0,0,24)
status.Position = UDim2.new(0,0,0,34)
status.BackgroundTransparency = 1
status.Text = ""
status.TextScaled = false
status.Font = Enum.Font.Gotham
status.TextSize = 14
status.TextXAlignment = Enum.TextXAlignment.Left
status.Parent = frame

local toggleBtn = Instance.new("TextButton")
toggleBtn.Size = UDim2.new(0,120,0,32)
toggleBtn.Position = UDim2.new(0,0,0,64)
toggleBtn.Text = "Toggle (K)"
toggleBtn.Font = Enum.Font.GothamBold
toggleBtn.TextScaled = true
toggleBtn.Parent = frame

local rangeLabel = Instance.new("TextLabel")
rangeLabel.Size = UDim2.new(0,140,0,20)
rangeLabel.Position = UDim2.new(0,0,0,100)
rangeLabel.BackgroundTransparency = 1
rangeLabel.Font = Enum.Font.Gotham
rangeLabel.TextSize = 14
rangeLabel.TextXAlignment = Enum.TextXAlignment.Left
rangeLabel.Parent = frame

local rangeBox = Instance.new("TextBox")
rangeBox.Size = UDim2.new(0,80,0,22)
rangeBox.Position = UDim2.new(0,150,0,98)
rangeBox.Text = tostring(range)
rangeBox.Font = Enum.Font.Gotham
rangeBox.TextSize = 14
rangeBox.ClearTextOnFocus = false
rangeBox.Parent = frame

local keyLabel = Instance.new("TextLabel")
keyLabel.Size = UDim2.new(0,120,0,20)
keyLabel.Position = UDim2.new(0,0,0,124)
keyLabel.BackgroundTransparency = 1
keyLabel.Font = Enum.Font.Gotham
keyLabel.TextSize = 14
keyLabel.TextXAlignment = Enum.TextXAlignment.Left
keyLabel.Parent = frame

local keyBox = Instance.new("TextBox")
keyBox.Size = UDim2.new(0,120,0,22)
keyBox.Position = UDim2.new(0,130,0,122)
keyBox.Text = tostring(hotkey.Name)
keyBox.Font = Enum.Font.Gotham
keyBox.TextSize = 14
keyBox.ClearTextOnFocus = false
keyBox.Parent = frame

local function updateStatus()
    status.Text = ("Status: %s    Range: %s    Key: %s"):format(enabled and "ON" or "OFF", tostring(range), tostring(hotkey.Name))
    if enabled then
        frame.BackgroundColor3 = Color3.fromRGB(40,160,40)
    else
        frame.BackgroundColor3 = Color3.fromRGB(160,40,40)
    end
end

toggleBtn.Activated:Connect(function()
    if enabled then disableNow() else enableNow() end
    updateStatus()
end)

rangeBox.FocusLost:Connect(function(enter)
    if not enter then return end
    local v = tonumber(rangeBox.Text)
    if v and v > 0 then
        range = v
    else
        rangeBox.Text = tostring(range)
    end
    updateStatus()
end)

keyBox.FocusLost:Connect(function(enter)
    if not enter then return end
    local text = keyBox.Text:upper():gsub("%s+","")
    local ok, enum = pcall(function() return Enum.KeyCode[text] end)
    if ok and enum then
        hotkey = enum
    else
        keyBox.Text = tostring(hotkey.Name)
    end
    updateStatus()
end)

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if gameProcessed then return end
    if input.KeyCode == hotkey then
        if enabled then disableNow() else enableNow() end
        updateStatus()
    end
end)

-- manejar herramientas que se agreguen mientras estamos desactivados/activados
player.CharacterAdded:Connect(function(char)
    if not enabled then
        wait(0.2)
        patchAllToolsInPlayer()
    else
        wait(0.2)
        restoreAllTools()
    end
end)

local function watchContainer(container)
    if not container then return end
    container.ChildAdded:Connect(function(child)
        if child:IsA("Tool") then
            if not enabled then patchToolActivate(child) end
        end
    end)
end
watchContainer(player:FindFirstChildOfClass("Backpack"))
if player.Character then watchContainer(player.Character) end

if AUTOCLOSE_GUI_SEC > 0 then
    delay(AUTOCLOSE_GUI_SEC, function()
        if screenGui and screenGui.Parent then screenGui.Enabled = false end
    end)
end

-- inicialización: restaurar estado desde atributo si existe
local attr = player:GetAttribute("KillSwitchEnabled")
if attr ~= nil then
    enabled = (attr == true)
else
    enabled = START_ENABLED
end

if enabled then
    enableNow()
else
    disableNow()
end
updateStatus()
  end
})
game:GetService("StarterGui"):SetCore("SendNotification",{
Title = "KEY LINK HAS BEEN COPIED TO CLIPBOARD",
Text = "", 

Button1 = "Ok",
Duration = 30 
})
   end,
})
local Button = misc:CreateButton({
   Name = "LAUNCH ADVANCED VERSION",
   Callback = function() 
   local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
    setclipboard("https://sites.google.com/view/slovak123456ggskeysystem/domov")
   game:GetService("StarterGui"):SetCore("SendNotification",{
Title = "KEY kink has been copied to clipboard!",
Text = "ITS EASY!", 

Button1 = "Ok",
Duration = 30 
})

local Window = Rayfield:CreateWindow({
	Name = "R.I.P. ADVANCED GUI",
	LoadingTitle = "Slovaks Team Project Hub",
	LoadingSubtitle = "By Slovak123456gg's team",
	ConfigurationSaving = {
		Enabled = true,
		FolderName = "wtf hub",
		FileName = "virus.stealer777"
	},
	KeySystem = true,  
	KeySettings = {
		Title = "R.I.P. HUB key system",
		Subtitle = "Slovak123456gg's Key System",
		Note = "its easy",
		SaveKey = true,
		Key = {"12341-sdawa-hkshdjuau-.3479"}
	}
})

Rayfield:Notify("Loaded!", "hi", 4483362458) -- Notfication -- Title, Content, Image
--Setting tabs
local cred = Window:CreateTab("Credits", 4483362458)
local comb = Window:CreateTab("Combat", 4483362458)
local plrc = Window:CreateTab("Player", 4483362458)
local misc = Window:CreateTab("Misc", 4483362458)
local FE = Window:CreateTab("FE", 4483362458)
 -- Title, Image
--Credits
local Section = cred:CreateSection("Credits")
local Paragraph = cred:CreateParagraph({Title = "Credits", Content = "Maded by Slovak123456gg's team"})
--Combat
local Button = comb:CreateButton({
	Name = "ESP",
	Callback = function()
 loadstring(game:HttpGet('https://pastebin.com/raw/yxpZ41xf'))()
 end,
})
local Button = comb:CreateButton({
 Name = "Aimlock",
 Callback = function()
 loadstring(game:HttpGet('https://pastebin.com/raw/NU9gz4yq'))()
 end,
})
--Player
local Slider = plrc:CreateSlider({
	Name = "walkspeed",
	Range = {1, 1000 },
	Increment = 1,
	Suffix = "ws",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local plrs = game.Players
 local plr = plrs.LocalPlayer
 walkspeed = Value;
 if plr then
  local char = plr.Character or plr.CharacterAdded:Wait()
   if char then
    local hum = char:FindFirstChildOfClass("Humanoid")
     if hum then
      hum.WalkSpeed = walkspeed
     end
   end
 end
	end,
})
local Slider = plrc:CreateSlider({
	Name = "jumppower",
	Range = {16, 516},
	Increment = 1,
	Suffix = "jp",
	CurrentValue = 16,
	Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end,
})
local Toggle = plrc:CreateToggle({
	Name = "Inf-Jump",
	CurrentValue = false,
	Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
	Callback = function(Value)
 local InfiniteJumpEnabled = Value
 game:GetService("UserInputService").JumpRequest:Connect(function()
  if InfiniteJumpEnabled then
   game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
  end
 end)
	end,
})
local Button = plrc:CreateButton({
 	Name = "Fly",
 	Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
  end
})
local Noclip = nil
local Clip = nil

function noclip()
	Clip = false
	local function Nocl()
		if Clip == false and game.Players.LocalPlayer.Character ~= nil then
			for _,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
				if v:IsA('BasePart') and v.CanCollide and v.Name ~= floatName then
					v.CanCollide = false
				end
			end
		end
		wait(0.21) -- basic optimization
	end
	Noclip = game:GetService('RunService').Stepped:Connect(Nocl)
end

function clip()
	if Noclip then Noclip:Disconnect() end
	Clip = true
end

local Button = plrc:CreateButton({
 	Name = "Noclip",
 	Callback = function()
  noclip()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Infinity Yield",
 	Callback = function()
  loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "F3X (btools)",
 	Callback = function()
  loadstring(game:GetObjects("rbxassetid://6695644299")[1].Source)()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Fake Lag",
 	Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/Biem6ondo/FAKELAG/refs/heads/main/Fakelag"))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "R6 Anim Hub",
 	Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/ExploitFin/AquaMatrix/refs/heads/AquaMatrix/AquaMatrix"))()
 	end,
})
local Button = misc:CreateButton({
 	Name = "Destroy hub",
 	Callback = function()
  Rayfield:Destroy()
  Rayfield:Notify({
   Title = "Notification Title",
   Content = "Notification Content",
   Duration = 6.5,
   Image = 4483362458,
})
  end,
})
local Button = FE:CreateButton({
 	Name = "Invisibility",
 	Callback = function()
   loadstring(game:HttpGet("https://pastebin.com/raw/3Rnd9rHf"))()
  end
})
local Button = FE:CreateButton({
 	Name = "Universal Dropkick",
 	Callback = function()
   loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-THE-REAL-dropkick-177199"))()
  end
})
local Button = FE:CreateButton({
 	Name = "Vexro Emotes",
 	Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/zyrovell/Vexro/main/vexroemotes.lua"))()
  end
})
local Button = comb:CreateButton({
 	Name = "Npc kill aura (TOOL REQUIRED)",
 	Callback = function()
   --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
-- KillSwitch v2 — GUI mejorada + spam en rango optimizado
-- Arranca OFF por defecto, pero lo podés cambiar.
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local task = task

-- ===== CONFIG =====
local START_ENABLED = false        -- true = arranca activado; false = arranca apagado
local DEFAULT_KEY = Enum.KeyCode.K -- tecla por defecto para toggle
local DEFAULT_RANGE = 8            -- rango por defecto
local AUTOCLOSE_GUI_SEC = 0        -- >0 oculta GUI automáticamente tras esos segundos (0 = nunca)
local LOOP_INTERVAL = 0.06         -- tiempo entre escaneos (segundos). Ajustalo si querés menos lag / más responsivo
local SPAM_WAIT = 0.03             -- espera entre intentos de Activate() en el spam loop
-- ==================

local enabled = START_ENABLED
local range = DEFAULT_RANGE
local hotkey = DEFAULT_KEY

local loopRunning = false
local loopThread = nil

local original_firetouch = firetouchinterest
local patchedTools = {} -- map tool -> {origActivate = fn}
local function noop_firetouch(...) end

-- spam control (visibles para doRangeHit)
local spamTask = nil
local spamActive = false

-- doRangeHit: detecta targets, hace firetouchinterest y controla spam de tool:Activate()
local function doRangeHit()
    local p = Players:GetPlayers()
    local tool = player.Character and player.Character:FindFirstChildOfClass("Tool")
    local anyTarget = false

    if tool and tool:FindFirstChild("Handle") then
        -- buscar si hay al menos un objetivo en rango y aplicar firetouchinterest sobre partes
        for i = 1, #p do
            local other = p[i]
            if other ~= player then
                local v = other.Character
                if v and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v:FindFirstChild("HumanoidRootPart") then
                    local ok, dist = pcall(function()
                        return player:DistanceFromCharacter(v.HumanoidRootPart.Position)
                    end)
                    if ok and dist and dist <= range then
                        anyTarget = true
                        for _, part in next, v:GetChildren() do
                            if part:IsA("BasePart") then
                                pcall(function()
                                    firetouchinterest(tool.Handle, part, 0)
                                    firetouchinterest(tool.Handle, part, 1)
                                end)
                            end
                        end
                    end
                end
            end
        end
    end

    -- manejar el spam: arrancar cuando aparece objetivo; parar cuando no hay
    if anyTarget and tool and tool.Parent == player.Character and enabled then
        if not spamActive then
            spamActive = true
            spamTask = task.spawn(function()
                -- este loop spamea Activate() tan rápido como el engine lo permita con una pequeña espera entre intentos
                while enabled and spamActive and tool and tool.Parent == player.Character do
                    pcall(function() tool:Activate() end)
                    task.wait(SPAM_WAIT)
                end
            end)
        end
    else
        spamActive = false
        spamTask = nil
    end
end

-- loop de ejecución controlado (optimizado para menos lag)
local function connectLoop()
    if loopRunning then return end
    loopRunning = true
    loopThread = task.spawn(function()
        while loopRunning do
            if enabled then
                pcall(doRangeHit)
            end
            task.wait(LOOP_INTERVAL)
        end
    end)
end

local function disconnectLoop()
    loopRunning = false
    loopThread = nil
end

-- Parcheo de Tool:Activate para evitar activaciones locales
local function patchToolActivate(tool)
    if not tool or patchedTools[tool] then return end
    local ok, orig = pcall(function() return tool.Activate end)
    if ok then
        patchedTools[tool] = {origActivate = orig}
        pcall(function()
            tool.Activate = function() end
        end)
    end
end

local function restoreToolActivate(tool)
    if not tool or not patchedTools[tool] then return end
    local data = patchedTools[tool]
    pcall(function()
        tool.Activate = data.origActivate
    end)
    patchedTools[tool] = nil
end

local function patchAllToolsInPlayer()
    -- patch tools in Backpack and Character
    local backpack = player:FindFirstChildOfClass("Backpack")
    if backpack then
        for _, t in pairs(backpack:GetChildren()) do
            if t:IsA("Tool") then patchToolActivate(t) end
        end
    end
    if player.Character then
        for _, t in pairs(player.Character:GetChildren()) do
            if t:IsA("Tool") then patchToolActivate(t) end
        end
    end
end

local function restoreAllTools()
    for tool, _ in pairs(patchedTools) do
        restoreToolActivate(tool)
    end
end

-- Activar / Desactivar con manejo de parches
local function enableNow()
    enabled = true
    if original_firetouch then firetouchinterest = original_firetouch end
    restoreAllTools()
    connectLoop()
    pcall(function() player:SetAttribute("KillSwitchEnabled", true) end)
    print("[KillSwitch] ACTIVADO")
end

local function disableNow()
    enabled = false
    firetouchinterest = noop_firetouch
    patchAllToolsInPlayer()
    -- parar spam inmediatamente
    spamActive = false
    spamTask = nil
    disconnectLoop()
    pcall(function() player:SetAttribute("KillSwitchEnabled", false) end)
    print("[KillSwitch] DESACTIVADO (firetouch bloqueado, Tool.Activate parcheado)")
end

-- Exponer funciones globales para control por consola/otros scripts (útil en Studio)
_G.killSwitchEnable = enableNow
_G.killSwitchDisable = disableNow
_G.killSwitchToggle = function() if enabled then disableNow() else enableNow() end end

-- ========== GUI ==========
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "KillSwitchGui"
screenGui.ResetOnSpawn = false
screenGui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,260,0,150)
frame.Position = UDim2.new(0,12,0,12)
frame.BackgroundTransparency = 0.2
frame.Parent = screenGui
frame.Active = true
frame.Draggable = true

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1,0,0,28)
title.Position = UDim2.new(0,0,0,0)
title.BackgroundTransparency = 1
title.Text = "KillSwitch (Studio)"
title.Font = Enum.Font.GothamBold
title.TextScaled = true
title.Parent = frame

local status = Instance.new("TextLabel")
status.Size = UDim2.new(1,0,0,24)
status.Position = UDim2.new(0,0,0,34)
status.BackgroundTransparency = 1
status.Text = ""
status.TextScaled = false
status.Font = Enum.Font.Gotham
status.TextSize = 14
status.TextXAlignment = Enum.TextXAlignment.Left
status.Parent = frame

local toggleBtn = Instance.new("TextButton")
toggleBtn.Size = UDim2.new(0,120,0,32)
toggleBtn.Position = UDim2.new(0,0,0,64)
toggleBtn.Text = "Toggle (K)"
toggleBtn.Font = Enum.Font.GothamBold
toggleBtn.TextScaled = true
toggleBtn.Parent = frame

local rangeLabel = Instance.new("TextLabel")
rangeLabel.Size = UDim2.new(0,140,0,20)
rangeLabel.Position = UDim2.new(0,0,0,100)
rangeLabel.BackgroundTransparency = 1
rangeLabel.Font = Enum.Font.Gotham
rangeLabel.TextSize = 14
rangeLabel.TextXAlignment = Enum.TextXAlignment.Left
rangeLabel.Parent = frame

local rangeBox = Instance.new("TextBox")
rangeBox.Size = UDim2.new(0,80,0,22)
rangeBox.Position = UDim2.new(0,150,0,98)
rangeBox.Text = tostring(range)
rangeBox.Font = Enum.Font.Gotham
rangeBox.TextSize = 14
rangeBox.ClearTextOnFocus = false
rangeBox.Parent = frame

local keyLabel = Instance.new("TextLabel")
keyLabel.Size = UDim2.new(0,120,0,20)
keyLabel.Position = UDim2.new(0,0,0,124)
keyLabel.BackgroundTransparency = 1
keyLabel.Font = Enum.Font.Gotham
keyLabel.TextSize = 14
keyLabel.TextXAlignment = Enum.TextXAlignment.Left
keyLabel.Parent = frame

local keyBox = Instance.new("TextBox")
keyBox.Size = UDim2.new(0,120,0,22)
keyBox.Position = UDim2.new(0,130,0,122)
keyBox.Text = tostring(hotkey.Name)
keyBox.Font = Enum.Font.Gotham
keyBox.TextSize = 14
keyBox.ClearTextOnFocus = false
keyBox.Parent = frame

local function updateStatus()
    status.Text = ("Status: %s    Range: %s    Key: %s"):format(enabled and "ON" or "OFF", tostring(range), tostring(hotkey.Name))
    if enabled then
        frame.BackgroundColor3 = Color3.fromRGB(40,160,40)
    else
        frame.BackgroundColor3 = Color3.fromRGB(160,40,40)
    end
end

toggleBtn.Activated:Connect(function()
    if enabled then disableNow() else enableNow() end
    updateStatus()
end)

rangeBox.FocusLost:Connect(function(enter)
    if not enter then return end
    local v = tonumber(rangeBox.Text)
    if v and v > 0 then
        range = v
    else
        rangeBox.Text = tostring(range)
    end
    updateStatus()
end)

keyBox.FocusLost:Connect(function(enter)
    if not enter then return end
    local text = keyBox.Text:upper():gsub("%s+","")
    local ok, enum = pcall(function() return Enum.KeyCode[text] end)
    if ok and enum then
        hotkey = enum
    else
        keyBox.Text = tostring(hotkey.Name)
    end
    updateStatus()
end)

UserInputService.InputBegan:Connect(function(input, gameProcessed)
    if gameProcessed then return end
    if input.KeyCode == hotkey then
        if enabled then disableNow() else enableNow() end
        updateStatus()
    end
end)

-- manejar herramientas que se agreguen mientras estamos desactivados/activados
player.CharacterAdded:Connect(function(char)
    if not enabled then
        wait(0.2)
        patchAllToolsInPlayer()
    else
        wait(0.2)
        restoreAllTools()
    end
end)

local function watchContainer(container)
    if not container then return end
    container.ChildAdded:Connect(function(child)
        if child:IsA("Tool") then
            if not enabled then patchToolActivate(child) end
        end
    end)
end
watchContainer(player:FindFirstChildOfClass("Backpack"))
if player.Character then watchContainer(player.Character) end

if AUTOCLOSE_GUI_SEC > 0 then
    delay(AUTOCLOSE_GUI_SEC, function()
        if screenGui and screenGui.Parent then screenGui.Enabled = false end
    end)
end

-- inicialización: restaurar estado desde atributo si existe
local attr = player:GetAttribute("KillSwitchEnabled")
if attr ~= nil then
    enabled = (attr == true)
else
    enabled = START_ENABLED
end

if enabled then
    enableNow()
else
    disableNow()
end
updateStatus()
  end
})
game:GetService("StarterGui"):SetCore("SendNotification",{
Title = "LOADED!",
Text = "", 

Button1 = "Ok",
Duration = 30 
})
   end,
})
