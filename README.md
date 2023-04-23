
local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
    Name = "Yone Hub",
    LoadingTitle = "YONE HUB",
    LoadingSubtitle = "by D4C",
    ConfigurationSaving = {
       Enabled = false,
       FolderName = nil, -- Create a custom folder for your hub/game
       FileName = "Big Hub"
    },
    Discord = {
       Enabled = false,
       Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
       RememberJoins = true -- Set this to false to make them join the discord every time they load it up
    },
    KeySystem = true, -- Set this to true to use our key system
    KeySettings = {
       Title = "Key System",
       Subtitle = "Key System",
       Note = "https://pastebin.com/raw/tccQkceg ",
       FileName = "Yone hub Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
       SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
       GrabKeyFromSite = true, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
       Key = {"RELEASE"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
    }
 })

 local Tab = Window:CreateTab("Main", 4483362458) -- Title, Image

local Section = Tab:CreateSection("Main")

local Button = Tab:CreateButton({
   Name = "Inf cash/exp on",
   Callback = function()
      getgenv().farm = true -- "false" to stop

while farm do task.wait()
game:GetService("ReplicatedStorage").Events.Dialogue:FireServer({
["Type"] = "End",
["Npc"] = workspace.Npcs.Mita,
["Path"] = "Accept"
})
game:GetService("ReplicatedStorage").Events.Dialogue:FireServer({
["Type"] = "End",
["Npc"] = workspace.Npcs:FindFirstChild("Saru Kenshi"),
["Path"] = "SetSpawn"
})
end
   end,
})

local Button = Tab:CreateButton({
   Name = "Inf cash/exp off",
   Callback = function()
      getgenv().farm = false -- "false" to stop

      while farm do task.wait()
      game:GetService("ReplicatedStorage").Events.Dialogue:FireServer({
      ["Type"] = "End",
      ["Npc"] = workspace.Npcs.Mita,
      ["Path"] = "Accept"
      })
      game:GetService("ReplicatedStorage").Events.Dialogue:FireServer({
      ["Type"] = "End",
      ["Npc"] = workspace.Npcs:FindFirstChild("Saru Kenshi"),
      ["Path"] = "SetSpawn"
      })
      end
   end,
})
 
 local Section = Tab:CreateSection("Local player")

 Section:Set("Local player")

 local Button = Tab:CreateButton({
   Name = "LSHIFT speed",
   Callback = function()
local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';
UIS.InputBegan:connect(function(UserInput)
        if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.LeftShift then
            _G.Running = true
                while wait(0.005) and _G.Running == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 1
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 1
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 1
end
        end
end)
UIS.InputEnded:connect(function(UserInput)
        if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.LeftShift then
                _G.Running = false
        end
end)
   end,
})

 local Tab = Window:CreateTab("Teleport", 4483362458) -- Title, Image

 local Button = Tab:CreateButton({
   Name = "Osiris",
   Callback = function()
      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1212.48804, 306.777374, -2054.39673, 1, 0, 0, 0, 1, 0, 0, 0, 1)
   end,
})

 local Button = Tab:CreateButton({
   Name = "???",
   Callback = function()
      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2783.73267, 33.5775261, -191.978027, -6.91413879e-06, -1, -6.31809235e-06, -0.0870228708, 6.91413879e-06, -0.996206343, 0.996206343, -6.31809235e-06, -0.0870229006)
   end,
})

local Button = Tab:CreateButton({
   Name = "Aika Roshu",
   Callback = function()
      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1550.8407, 331.67688, 1481.85083, -0.499959469, 0.0341792144, -0.865374088, 0, 0.999220967, 0.0394656956, 0.866048813, 0.0197312497, -0.499569982)
   end,
})

local Button = Tab:CreateButton({
   Name = "Airi",
   Callback = function()
      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(685.696655, 6.2887373, 619.365356, -0.662489831, -5.79167079e-08, 0.749071896, -1.52908683e-07, 1, -5.79166581e-08, -0.749071896, -1.52908797e-07, -0.662489831)
   end,
})

local Button = Tab:CreateButton({
   Name = "Akihito",
   Callback = function()
      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-758.072571, 307.00647, 721.179077, 1, 0, 0, 0, 1, 0, 0, 0, 1)
   end,
})

 Rayfield:Notify({
    Title = "Welcome",
    Content = "Welcome to the script",
    Duration = 10,
    Image = 4483362458,
    Actions = { -- Notification Buttons
       Ignore = {
          Name = "Okay!",
          Callback = function()
          print("The user tapped Okay!")
       end
    },
 },
 })

 local Tab = Window:CreateTab("Misc", 4483362458) -- Title, Image


 
