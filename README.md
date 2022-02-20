-- init
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GreenDeno/Venyx-UI-Library/main/source.lua"))()
local venyx = library.new("Venyx", 5013109572)

-- themes
local themes = {
	Background = Color3.fromRGB(24, 24, 24),
	Glow = Color3.fromRGB(0, 0, 0),
	Accent = Color3.fromRGB(10, 10, 10),
	LightContrast = Color3.fromRGB(20, 20, 20),
	DarkContrast = Color3.fromRGB(14, 14, 14),  
	TextColor = Color3.fromRGB(255, 255, 255)
}

if _G.Teams == "Pirates" then
    for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
        v.Function()
    end
elseif _G.Teams == "Marines" then
    for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
        v.Function()
    end
else
    for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
        v.Function()
    end
end

local LocalPlayer = game:GetService("Players").LocalPlayer
local VirtualUser = game:GetService('VirtualUser')
local placeId = game.PlaceId
if placeId == 2753915549 then
    Sea1 = true
elseif placeId == 4442272183 then
    Sea2 = true
elseif placeId == 7449423635 then
    Sea3 = true
end

function CheckQuest() 
    MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
    if Sea1 then
        if MyLevel == 1 or MyLevel <= 9 then
            Mon = "Bandit [Lv. 5]"
            LevelQuest = 1
            NameQuest = "BanditQuest1"
            NameMon = "Bandit"
            CFrameMon = CFrame.new(1184.6668701172, 66.851402282715, 1513.2677001953)
            CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
        elseif MyLevel == 10 or MyLevel <= 14 then
            Mon = "Monkey [Lv. 14]"
            LevelQuest = 1
            NameQuest = "JungleQuest"
            NameMon = "Monkey"
            CFrameMon = CFrame.new(-1606.4381103516, 35.292171478271, 171.13681030273)
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        elseif MyLevel == 15 or MyLevel <= 29 then
            Mon = "Gorilla [Lv. 20]"
            LevelQuest = 2
            NameQuest = "JungleQuest"
            NameMon = "Gorilla"
            CFrameMon = CFrame.new(-1155.7474365234, 13.141628265381, -546.68371582031)
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        elseif MyLevel == 30 or MyLevel <= 39 then
            Mon = "Pirate [Lv. 35]"
            LevelQuest = 1
            NameQuest = "BuggyQuest1"
            NameMon = "Pirate"
            CFrameMon = CFrame.new(-1157.0579833984, 47.273414611816, 3970.0051269531)
            CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        elseif MyLevel == 40 or MyLevel <= 59 then
            Mon = "Brute [Lv. 45]"
            LevelQuest = 2
            NameQuest = "BuggyQuest1"
            NameMon = "Brute"
            CFrameMon = CFrame.new(-1136.0251464844, 86.027862548828, 4303.5830078125)
            CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        elseif MyLevel == 60 or MyLevel <= 74 then
            Mon = "Desert Bandit [Lv. 60]"
            LevelQuest = 1
            NameQuest = "DesertQuest"
            NameMon = "Desert Bandit"
            CFrameMon = CFrame.new(864.65197753906, 20.758842468262, 4536.83203125)
            CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
        elseif MyLevel == 75 or MyLevel <= 89 then
            Mon = "Desert Officer [Lv. 70]"
            LevelQuest = 2
            NameQuest = "DesertQuest"
            NameMon = "Desert Officer"
            CFrameMon = CFrame.new(1549.7355957031, 14.452038764954, 4373.1884765625)
            CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
        elseif MyLevel == 90 or MyLevel <= 99 then
            Mon = "Snow Bandit [Lv. 90]"
            LevelQuest = 1
            NameQuest = "SnowQuest"
            NameMon = "Snow Bandit"
            CFrameMon = CFrame.new(1422.7448730469, 119.62019348145, -1414.0554199219)
            CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
            CFrameTweenPak = Vector3.new(1379.6555175781, 87.272789001465, -1354.8793945313)
        elseif MyLevel == 100 or MyLevel <= 119 then
            Mon = "Snowman [Lv. 100]"
            LevelQuest = 2
            NameQuest = "SnowQuest"
            NameMon = "Snowman"
            CFrameMon = CFrame.new(1220.6397705078, 138.0118560791, -1489.2474365234)
            CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
        elseif MyLevel == 120 or MyLevel <= 149 then
            Mon = "Chief Petty Officer [Lv. 120]"
            LevelQuest = 1
            NameQuest = "MarineQuest2"
            NameMon = "Chief Petty Officer"
            CFrameMon = CFrame.new(-4937.7001953125, 43.252059936523, 4197.0908203125)
            CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 150 or MyLevel <= 174 then
            Mon = "Sky Bandit [Lv. 150]"
            LevelQuest = 1
            NameQuest = "SkyQuest"
            NameMon = "Sky Bandit"
            CFrameMon = CFrame.new(-4953.0014648438, 365.25204467773, -2923.8449707031)
            CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
        elseif MyLevel == 175 or MyLevel <= 224 then
            Mon = "Dark Master [Lv. 175]"
            LevelQuest = 2
            NameQuest = "SkyQuest"
            NameMon = "Dark Master"
            CFrameMon = CFrame.new(-5227.7631835938, 428.12329101562, -2285.0556640625)
            CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
        elseif MyLevel == 225 or MyLevel <= 274 then
            Mon = "Toga Warrior [Lv. 225]"
            LevelQuest = 1
            NameQuest = "ColosseumQuest"
            NameMon = "Toga Warrior"
            CFrameMon = CFrame.new(-1819.9221191406, 52.790023803711, -2743.7270507812)
            CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
        elseif MyLevel == 275 or MyLevel <= 299 then
            Mon = "Gladiator [Lv. 275]"
            LevelQuest = 2
            NameQuest = "ColosseumQuest"
            NameMon = "Gladiator"
            CFrameMon = CFrame.new(-1339.7672119141, 39.460353851318, -3238.71875)
            CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
        elseif MyLevel == 300 or MyLevel <= 329 then
            Mon = "Military Soldier [Lv. 300]"
            LevelQuest = 1
            NameQuest = "MagmaQuest"
            NameMon = "Military Soldier"
            CFrameMon = CFrame.new(-5474.4526367188, 38.43244934082, 8606.517578125)
            CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
        elseif MyLevel == 330 or MyLevel <= 374 then
            Mon = "Military Spy [Lv. 330]"
            LevelQuest = 2
            NameQuest = "MagmaQuest"
            NameMon = "Military Spy"
            CFrameMon = CFrame.new(-5880.0727539062, 134.29690551758, 8869.8037109375)
            CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
        elseif MyLvel == 375 or MyLevel <= 399 then
            Mon = "Fishman Warrior [Lv. 375]"
            LevelQuest = 1
            NameQuest = "FishmanQuest"
            NameMon = "Fishman Warrior"
            CFrameMon = CFrame.new(60993.60546875, 96.347175598145, 1367.5928955078)
            CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            end
        elseif MyLevel == 400 or MyLevel <= 449 then
            Mon = "Fishman Commando [Lv. 400]"
            LevelQuest = 2
            NameQuest = "FishmanQuest"
            NameMon = "Fishman Commando"
            CFrameMon = CFrame.new(61910.90625, 108.48404693604, 1536.6251220703)
            CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            end
        elseif MyLevel == 450 or MyLevel <= 474 then
            Mon = "God's Guard [Lv. 450]"
            LevelQuest = 1
            NameQuest = "SkyExp1Quest"
            NameMon = "God's Guard"
            CFrameMon = CFrame.new(-4681.8432617188, 845.27716064453, -1955.4534912109)
            CFrameQuest = CFrame.new(-4721.88867, 843.874695, -1949.96643, 0.996191859, -0, -0.0871884301, 0, 1, -0, 0.0871884301, 0, 0.996191859)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
            end
        elseif MyLevel == 475 or MyLevel <= 524 then
            Mon = "Shanda [Lv. 475]"
            LevelQuest = 2
            NameQuest = "SkyExp1Quest"
            NameMon = "Shanda"
            CFrameMon = CFrame.new(-7691.0053710938, 5600.5346679688, -441.2951965332)
            CFrameQuest = CFrame.new(-7859.09814, 5544.19043, -381.476196, -0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, -0.422592998)
            if  _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
            end
        elseif MyLevel == 525 or MyLevel <= 549 then
            Mon = "Royal Squad [Lv. 525]"
            LevelQuest = 1
            NameQuest = "SkyExp2Quest"
            NameMon = "Royal Squad"
            CFrameMon = CFrame.new(-7639.4243164062, 5637.0805664062, -1422.8220214844)
            CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 550 or MyLevel <= 624 then
            Mon = "Royal Soldier [Lv. 550]"
            LevelQuest = 2
            NameQuest = "SkyExp2Quest"
            NameMon = "Royal Soldier"
            CFrameMon = CFrame.new(-7859.00390625, 5662.416015625, -1704.2005615234)
            CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 625 or MyLevel <= 649 then
            Mon = "Galley Pirate [Lv. 625]"
            LevelQuest = 1
            NameQuest = "FountainQuest"
            NameMon = "Galley Pirate"
            CFrameMon = CFrame.new(5521.0883789062, 107.23796844482, 4077.607421875)
            CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
        elseif MyLevel >= 650 then
            Mon = "Galley Captain [Lv. 650]"
            LevelQuest = 2
            NameQuest = "FountainQuest"
            NameMon = "Galley Captain"
            CFrameMon = CFrame.new(5556.1420898438, 113.47412109375, 4819.0576171875)
            CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
        end
    elseif Sea2 then
        if MyLevel == 700 or MyLevel <= 724 then
            Mon = "Raider [Lv. 700]"
            LevelQuest = 1
            NameQuest = "Area1Quest"
            NameMon = "Raider"
            CFrameMon = CFrame.new(-463.38961791992, 97.173683166504, 2324.0480957031)
            CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
        elseif MyLevel == 725 or MyLevel <= 774 then
            Mon = "Mercenary [Lv. 725]"
            LevelQuest = 2
            NameQuest = "Area1Quest"
            NameMon = "Mercenary"
            CFrameMon = CFrame.new(-1071.4328613281, 88.655242919922, 1629.7348632812)
            CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
        elseif MyLevel == 775 or MyLevel <= 799 then
            Mon = "Swan Pirate [Lv. 775]"
            LevelQuest = 1
            NameQuest = "Area2Quest"
            NameMon = "Swan Pirate"
            CFrameMon = CFrame.new(1024.1345214844, 73.029739379883, 1262.7456054688)
            CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
        elseif MyLevel == 800 or MyLevel <= 874 then
            Mon = "Factory Staff [Lv. 800]"
            NameQuest = "Area2Quest"
            LevelQuest = 2
            NameMon = "Factory Staff"
            CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
            CFrameMon = CFrame.new(296.786499, 72.9948196, -57.1298141, -0.876037002, -5.32364979e-08, 0.482243896, -3.87658332e-08, 1, 3.99718729e-08, -0.482243896, 1.63222538e-08, -0.876037002)
        elseif MyLevel == 875 or MyLevel <= 899 then
            Mon = "Marine Lieutenant [Lv. 875]"
            LevelQuest = 1
            NameQuest = "MarineQuest3"
            NameMon = "Marine Lieutenant"
            CFrameMon = CFrame.new(-2842.595703125, 72.96614074707, -3012.0222167969)
            CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
        elseif MyLevel == 900 or MyLevel <= 949 then
            Mon = "Marine Captain [Lv. 900]"
            LevelQuest = 2
            NameQuest = "MarineQuest3"
            NameMon = "Marine Captain"
            CFrameMon = CFrame.new(-1927.8619384766, 72.96614074707, -3385.0322265625)
            CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
        elseif MyLevel == 950 or MyLevel <= 974 then
            Mon = "Zombie [Lv. 950]"
            LevelQuest = 1
            NameQuest = "ZombieQuest"
            NameMon = "Zombie"
            CFrameMon = CFrame.new(-5685.9233398438, 48.480125427246, -853.23724365234)
            CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
        elseif MyLevel == 975 or MyLevel <= 999 then
            Mon = "Vampire [Lv. 975]"
            LevelQuest = 2
            NameQuest = "ZombieQuest"
            NameMon = "Vampire"
            CFrameMon = CFrame.new(-6018.3452148438, 6.4027013778687, -1267.6065673828)
            CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
        elseif MyLevel == 1000 or MyLevel <= 1049 then
            Mon = "Snow Trooper [Lv. 1000]"
            LevelQuest = 1
            NameQuest = "SnowMountainQuest"
            NameMon = "Snow Trooper"
            CFrameMon = CFrame.new(481.48031616211, 401.42202758789, -5361.2138671875)
            CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
        elseif MyLevel == 1050 or MyLevel <= 1099 then
            Mon = "Winter Warrior [Lv. 1050]"
            LevelQuest = 2
            NameQuest = "SnowMountainQuest"
            NameMon = "Winter Warrior"
            CFrameMon = CFrame.new(1148.3015136719, 429.38235473633, -5262.1708984375)
            CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
        elseif MyLevel == 1100 or MyLevel <= 1124 then
            Mon = "Lab Subordinate [Lv. 1100]"
            LevelQuest = 1
            NameQuest = "IceSideQuest"
            NameMon = "Lab Subordinate"
            CFrameMon = CFrame.new(-5775.5200195313, 42.301044464111, -4483.5092773438)
            CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
        elseif MyLevel == 1125 or MyLevel <= 1174 then
            Mon = "Horned Warrior [Lv. 1125]"
            LevelQuest = 2
            NameQuest = "IceSideQuest"
            NameMon = "Horned Warrior"
            CFrameMon = CFrame.new(-6283.5942382813, 18.321973800659, -5606.4282226563)
            CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
        elseif MyLevel == 1175 or MyLevel <= 1199 then
            Mon = "Magma Ninja [Lv. 1175]"
            LevelQuest = 1
            NameQuest = "FireSideQuest"
            NameMon = "Magma Ninja"
            CFrameMon = CFrame.new(-5686.64453125, 15.951762199402, -5713.7026367188)
            CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
        elseif MyLevel == 1200 or MyLevel <= 1249 then
            Mon = "Lava Pirate [Lv. 1200]"
            LevelQuest = 2
            NameQuest = "FireSideQuest"
            NameMon = "Lava Pirate"
            CFrameMon = CFrame.new(-5427.345703125, 67.961860656738, -4694.3706054688)
            CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
        elseif MyLevel == 1250 or MyLevel <= 1274 then
            Mon = "Ship Deckhand [Lv. 1250]"
            LevelQuest = 1
            NameQuest = "ShipQuest1"
            NameMon = "Ship Deckhand"
            CFrameMon = CFrame.new(1163.80872, 138.288452, 33058.4258)
            CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)         
            if  _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 18500 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            end
        elseif MyLevel == 1275 or MyLevel <= 1299 then
            Mon = "Ship Engineer [Lv. 1275]"
            LevelQuest = 2
            NameQuest = "ShipQuest1"
            NameMon = "Ship Engineer"
            CFrameMon = CFrame.new(916.666504, 44.0920448, 32917.207)
            CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)   
            if  _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 18500 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            end             
        elseif MyLevel == 1300 or MyLevel <= 1324 then
            Mon = "Ship Steward [Lv. 1300]"
            LevelQuest = 1
            NameQuest = "ShipQuest2"
            NameMon = "Ship Steward"
            CFrameMon = CFrame.new(918.743286, 129.591064, 33443.4609)
            CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)         
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 18500 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            end
        elseif MyLevel == 1325 or MyLevel <= 1349 then
            Mon = "Ship Officer [Lv. 1325]"
            LevelQuest = 2
            NameQuest = "ShipQuest2"
            NameMon = "Ship Officer"
            CFrameMon = CFrame.new(786.051941, 181.474106, 33303.2969)
            CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            end
        elseif MyLevel == 1350 or MyLevel <= 1374 then
            Mon = "Arctic Warrior [Lv. 1350]"
            LevelQuest = 1
            NameQuest = "FrostQuest"
            NameMon = "Arctic Warrior"
            CFrameMon = CFrame.new(5973.6040039062, 61.72314453125, -6168.0717773438)
            CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 16500 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            end
        elseif MyLevel == 1375 or MyLevel <= 1424 then
            Mon = "Snow Lurker [Lv. 1375]"
            LevelQuest = 2
            NameQuest = "FrostQuest"
            NameMon = "Snow Lurker"
            CFrameMon = CFrame.new(5518.5166015625, 60.520919799805, -6829.7817382812)
            CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
            if _G.Auto_Farm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 16500 then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            end
        elseif MyLevel == 1425 or MyLevel <= 1449 then
            Mon = "Sea Soldier [Lv. 1425]"
            LevelQuest = 1
            NameQuest = "ForgottenQuest"
            NameMon = "Sea Soldier"
            CFrameMon = CFrame.new(-3231.1901855469, 61.941078186035, -9733.154296875)
            CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
        elseif MyLevel >= 1450 then
            Mon = "Water Fighter [Lv. 1450]"
            LevelQuest = 2
            NameQuest = "ForgottenQuest"
            NameMon = "Water Fighter"
            CFrameMon = CFrame.new(-3261.4780273438, 291.33917236328, -10596.365234375)
            CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
        end
    elseif Sea3 then
        if MyLevel == 1500 or MyLevel <= 1524 then
            Mon = "Pirate Millionaire [Lv. 1500]"
            LevelQuest = 1
            NameQuest = "PiratePortQuest"
            NameMon = "Pirate Millionaire"
            CFrameMon = CFrame.new(-366.55215454102, 68.321365356445, 5561.5541992188)
            CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
            CFrameTweenPak = Vector3.new(-366.55215454102, 68.321365356445, 5561.5541992188)
        elseif MyLevel == 1525 or MyLevel <= 1574 then
            Mon = "Pistol Billionaire [Lv. 1525]"
            LevelQuest = 2
            NameQuest = "PiratePortQuest"
            NameMon = "Pistol Billionaire"
            CFrameMon = CFrame.new(-413.86712646484, 123.34642028809, 5857.123046875)
            CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
        elseif MyLevel == 1575 or MyLevel <= 1599 then
            Mon = "Dragon Crew Warrior [Lv. 1575]"
            LevelQuest = 1
            NameQuest = "AmazonQuest"
            NameMon = "Dragon Crew Warrior"
            CFrameMon = CFrame.new(6297.5546875, 108.10154724121, -1078.3551025391)
            CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
            elseif MyLevel == 1600 or MyLevel <= 1624 then 
            Mon = "Dragon Crew Archer [Lv. 1600]"
            NameQuest = "AmazonQuest"
            LevelQuest = 2
            NameMon = "Dragon Crew Archer"
            CFrameQuest = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
            CFrameMon = CFrame.new(6831.1171875, 441.76708984375, 446.58615112305)
            elseif MyLevel == 1625 or MyLevel <= 1649 then
            Mon = "Female Islander [Lv. 1625]"
            NameQuest = "AmazonQuest2"
            LevelQuest = 1
            NameMon = "Female Islander"
            CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
            CFrameMon = CFrame.new(5792.5166015625, 848.14392089844, 1084.1818847656)
            elseif MyLevel == 1650 or MyLevel <= 1699 then 
            Mon = "Giant Islander [Lv. 1650]"
            NameQuest = "AmazonQuest2"
            LevelQuest = 2
            NameMon = "Giant Islander"
            CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
            CFrameMon = CFrame.new(5009.5068359375, 664.11071777344, -40.960144042969)
        elseif MyLevel == 1700 or MyLevel <= 1724 then
            Mon = "Marine Commodore [Lv. 1700]"
            LevelQuest = 1
            NameQuest = "MarineTreeIsland"
            NameMon = "Marine Commodore"
            CFrameMon = CFrame.new(2475.3618164062, 190.4232635498, -7174.0126953125)
            CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
            elseif MyLevel == 1725 or MyLevel <= 1774 then
            Mon = "Marine Rear Admiral [Lv. 1725]"
            NameMon = "Marine Rear Admiral"
            NameQuest = "MarineTreeIsland"
            LevelQuest = 2
            CFrameQuest = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
            CFrameMon = CFrame.new(3294.3142089844, 385.41125488281, -7048.6342773438)
            CFrameTweenQuest = Vector3.new(2179.98828125, 28.731239318848, -6740.0551757813)
        elseif MyLevel == 1775 or MyLevel <= 1799 then
            Mon = "Fishman Raider [Lv. 1775]"
            LevelQuest = 1
            NameQuest = "DeepForestIsland3"
            NameMon = "Fishman Raider"
            CFrameMon = CFrame.new(-10310.296875, 426.3200378418, -8592.0048828125)
            CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)   
        elseif MyLevel == 1800 or MyLevel <= 1824 then
            Mon = "Fishman Captain [Lv. 1800]"
            LevelQuest = 2
            NameQuest = "DeepForestIsland3"
            NameMon = "Fishman Captain"
            CFrameMon = CFrame.new(-10728.3046875, 397.76626586914, -9079.86328125)
            CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)   
        elseif MyLevel == 1825 or MyLevel <= 1849 then
            Mon = "Forest Pirate [Lv. 1825]"
            LevelQuest = 1
            NameQuest = "DeepForestIsland"
            NameMon = "Forest Pirate"
            CFrameMon = CFrame.new(-13265.977539063, 428.16796875, -7758.57421875)
            CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
        elseif MyLevel == 1850 or MyLevel <= 1899 then
            Mon = "Mythological Pirate [Lv. 1850]"
            LevelQuest = 2
            NameQuest = "DeepForestIsland"
            NameMon = "Mythological Pirate"
            CFrameMon = CFrame.new(-13392.751953125, 622.6171875, -7082.2348632813)
            CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)   
        elseif MyLevel == 1900 or MyLevel <= 1924 then
            Mon = "Jungle Pirate [Lv. 1900]"
            LevelQuest = 1
            NameQuest = "DeepForestIsland2"
            NameMon = "Jungle Pirate"
            CFrameMon = CFrame.new(-11997.963867188, 431.92016601563, -10300.259765625)
            CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
        elseif MyLevel == 1925 or MyLevel <= 1974 then
            Mon = "Musketeer Pirate [Lv. 1925]"
            LevelQuest = 2
            NameQuest = "DeepForestIsland2"
            NameMon = "Musketeer Pirate"
            CFrameMon = CFrame.new(-13549.004882812, 446.30151367188, -9876.7529296875)
            CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
        elseif MyLevel == 1975 or MyLevel <= 1999 then
            Mon = "Reborn Skeleton [Lv. 1975]"
            LevelQuest = 1
            NameQuest = "HauntedQuest1"
            NameMon = "Reborn Skeleton"
            CFrameMon = CFrame.new(-8767.4658203125, 184.68771362305, 6228.1762695313)
            CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        elseif MyLevel == 2000 or MyLevel <= 2024 then
            Mon = "Living Zombie [Lv. 2000]"
            LevelQuest = 2
            NameQuest = "HauntedQuest1"
            NameMon = "Living Zombie"
            CFrameMon = CFrame.new(-10109.233398438, 397.53930664062, 5912.5102539062)
            CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
        elseif MyLevel == 2025 or MyLevel <= 2049 then
            Mon = "Demonic Soul [Lv. 2025]"
            LevelQuest = 1
            NameQuest = "HauntedQuest2"
            NameMon = "Demonic Soul"
            CFrameMon = CFrame.new(-9365.5595703125, 222.10494995117, 6231.1879882813)
            CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0) 
        elseif MyLevel == 2050 or MyLevel <= 2074 then
            Mon = "Posessed Mummy [Lv. 2050]"
            LevelQuest = 2
            NameQuest = "HauntedQuest2"
            NameMon = "Posessed Mummy"
            CFrameMon = CFrame.new(-9556.00488, 66.3880768, 6370.78076, 0.999951124, 3.36073747e-08, -0.00988800824, -3.39445911e-08, 1, -3.39356419e-08, 0.00988800824, 3.42696289e-08, 0.999951124)
            CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 2075 or MyLevel <= 2099 then
            Mon = "Peanut Scout [Lv. 2075]"
            LevelQuest = 1
            NameQuest = "NutsIslandQuest"
            NameMon = "Peanut Scout"
            CFrameMon = CFrame.new(-2192.3247070312, 94.319366455078, -10092.274414062, 0, 0, -1, 0, 1, 0, 1, 0, 0)
            CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 2100 or MyLevel <= 2124 then
            Mon = "Peanut President [Lv. 2100]"
            LevelQuest = 2
            NameQuest = "NutsIslandQuest"
            NameMon = "Peanut President"
            CFrameMon = CFrame.new(-2120.5974121094, 124.56230163574, -10441.361328125, 0, 0, -1, 0, 1, 0, 1, 0, 0)
            CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel == 2125 or MyLevel <= 2149 then
            Mon = "Ice Cream Chef [Lv. 2125]"
            LevelQuest = 1
            NameQuest = "IceCreamIslandQuest"
            NameMon = "Ice Cream Chef"
            CFrameMon = CFrame.new(-898.00366210938, 119.35078430176, -10943.458984375, 0, 0, -1, 0, 1, 0, 1, 0, 0)
            CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        elseif MyLevel >= 2150 then
            Mon = "Ice Cream Commander [Lv. 2150]"
            LevelQuest = 2
            NameQuest = "IceCreamIslandQuest"
            NameMon = "Ice Cream Commander"
            CFrameMon = CFrame.new(-514.06311035156, 172.69267272949, -11215.62890625, 0, 0, -1, 0, 1, 0, 1, 0, 0)
            CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
        end
    end
end

function Hop()
    local PlaceID = game.PlaceId
    local AllIDs = {}
    local foundAnything = ""
    local actualHour = os.date("!*t").hour
    local Deleted = false
    function TPReturner()
        local Site;
        if foundAnything == "" then
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
        else
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
        end
        local ID = ""
        if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
            foundAnything = Site.nextPageCursor
        end
        local num = 0;
        for i,v in pairs(Site.data) do
            local Possible = true
            ID = tostring(v.id)
            if tonumber(v.maxPlayers) > tonumber(v.playing) then
                for _,Existing in pairs(AllIDs) do
                    if num ~= 0 then
                        if ID == tostring(Existing) then
                            Possible = false
                        end
                    else
                        if tonumber(actualHour) ~= tonumber(Existing) then
                            local delFile = pcall(function()
                                -- delfile("NotSameServers.json")
                                AllIDs = {}
                                table.insert(AllIDs, actualHour)
                            end)
                        end
                    end
                    num = num + 1
                end
                if Possible == true then
                    table.insert(AllIDs, ID)
                    wait()
                    pcall(function()
                        -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                        wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                    end)
                    wait(4)
                end
            end
        end
    end
    function Teleport() 
        while wait() do
            pcall(function()
                TPReturner()
                if foundAnything ~= "" then
                    TPReturner()
                end
            end)
        end
    end
    Teleport()
end 

function Buso()
    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
    end
end

SelectToolWeapon = ""
function EquipWeapon(ToolSe)
	if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
		local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
		wait(.4)
		game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
	end
end

function TP(Pos)
	local Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
	if Distance >= 1000 then
		Speed = 220
    elseif Distance <= 600 then
		Speed = 600
	end
	tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
	tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = Pos})
	tween:Play()
	getgenv().Clip = true
    spawn(function()
        if Distance <= 6 then
            getgenv().Clip = false
        end
    end)
	if Distance <= 100 then
		tween:Cancel()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
	end
end

if syn then
    spawn(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            pcall(function()
                if game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
                    if _G.AutoKaitan or getgenv().Clip then
                        setfflag("HumanoidParallelRemoveNoPhysics", "False")
                        setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
                        game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                    else
                        game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(18)
                    end
                end
            end)
        end)
    end)
else
    spawn(function()
        pcall(function()
            while task.wait() do
                if _G.AutoKaitan or getgenv().Clip then
                    if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("XenonNoClipKubNo1") then
                        local Noclip = Instance.new("BodyVelocity")
                        Noclip.Name = "XenonNoClipKubNo1"
                        Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                        Noclip.MaxForce = Vector3.new(100000,100000,100000)
                        Noclip.Velocity = Vector3.new(0,0,0)
                    end
                end
            end
        end)
    end)
    
    spawn(function()
        pcall(function()
            game:GetService("RunService").Stepped:Connect(function()
                if _G.AutoKaitan or getgenv().Clip then
                    for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("BasePart") then
                            v.CanCollide = false    
                        end
                    end
                end
            end)
        end)
    end)
end

function StopTween(Config)
    if not Config then
        wait()
        TP(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
        wait()
        if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("XenonNoClipKubNo1") then
            game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("XenonNoClipKubNo1"):Destroy()
        end
        getgenv().Clip = false
    end
end

spawn(function()
    while wait() do
        pcall(function()
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v.ToolTip == "Melee" then
                    getgenv().SelectWeaponMalee = v.Name
                end
            end
        end)
    end
end)

spawn(function()
	while wait(.1) do
		for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
			if v:IsA("Tool") then 
				if v.ToolTip == "Wear" then    
					getgenv().SelectAccessories = v.Name
				end
			end
		end
	end
end)


-- first page
local page = venyx:addPage("Test", 5012544693)
local section1 = page:addSection("Section 1")
local section2 = page:addSection("Section 2")


 Wapon = {}
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
	if v:IsA("Tool") then
		table.insert(Wapon ,v.Name)
	end
end
for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
	if v:IsA("Tool") then
		table.insert(Wapon, v.Name)
	end
end

local SelectWeapona = section1:addDropdown("Select Weapon",Wapon,function(Value)
	_G.SelectWeapon = Value
	_G.SelectToolWeaponOld = Value
end)

section1:addButton("Refresh Weapon", function()
	SelectWeapona:Clear()
	Wapon = {}
	for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
		if v:IsA("Tool") then
			SelectWeapona:Add(v.Name)
		end
	end
	for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
		if v:IsA("Tool") then
			SelectWeapona:Add(v.Name)
		end
	end
end)

section1:addToggle("Auto Farm",_G.Auto_Farm,function(value)
    _G.Auto_Farm = value
end)

spawn(function()
    pcall(function()
        while wait() do
            if _G.Auto_Farm then
                if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
                end
            end
        end
   end)
end)

spawn(function()
    while wait() do
        if _G.Auto_Farm then
            pcall(function()			
                local QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
                if not string.find(QuestTitle, NameMon) then
                    MagnetLv = false
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                end
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    MagnetLv = false
                    CheckQuest()
                    repeat wait()
                        TP(CFrameQuest)
                    until (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Auto_Farm
                    if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                        wait(1.2)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
                        wait(0.5)
                    end
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                    CheckQuest()
                    if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                if v.Name == Mon then
                                    if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
                                        repeat task.wait()
                                            Buso()
                                            EquipWeapon(_G.SelectWeapon)
                                            PosMon = v.HumanoidRootPart.CFrame
                                            TP(v.HumanoidRootPart.CFrame * CFrame.new(0,38,0))
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid.WalkSpeed = 0
                                            v.Head.CanCollide = false
                                            MagnetLv = true
                                            game:GetService'VirtualUser':CaptureController()
                                            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        until not _G.Auto_Farm or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                    else
                                        MagnetLv = false
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                    end
                                end
                            end
                        end
                    else
                        MagnetLv = false   
                        local Mob = game:GetService("ReplicatedStorage"):FindFirstChild(Mon) 
                        if Mob then
                            TP(Mob.HumanoidRootPart.CFrame * CFrame.new(0,38,0))
                        else
                            if game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y <= 1 then
                                game.Players.LocalPlayer.Character.Humanoid.Jump = true
                                task.wait()
                                game.Players.LocalPlayer.Character.Humanoid.Jump = false
                            end
                        end
                    end
                end
            end)
        end
    end
end)

spawn(function()
    while wait() do
        if _G.Auto_Farm then
            pcall(function()
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Dialogue.Visible == true then
                    for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.Dialogue.Cancel.MouseButton1Click)) do
                        v.Function()
                    end
                end
            end)
        end
    end
end)

spawn(function()
    while task.wait() do
        pcall(function()
            CheckQuest()
            for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if _G.Auto_Farm and MagnetLv and v.Name == Mon and (Mon == "Factory Staff [Lv. 800]" or Mon == "Monkey [Lv. 14]" or Mon == "Dragon Crew Warrior [Lv. 1575]" or Mon == "Dragon Crew Archer [Lv. 1600]") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 200 then
                    v.HumanoidRootPart.CFrame = PosMon
                    v.Humanoid:ChangeState(11)
                    if not v.HumanoidRootPart:FindFirstChild("BodyVelocity") then
                        local bv = Instance.new("BodyVelocity")
                        bv.Parent = v.HumanoidRootPart
                        bv.MaxForce = Vector3.new(100000,100000,100000)
                        bv.Velocity = Vector3.new(0,0,0)
                    end
                    sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                    delay(15,function()
                        v.Humanoid.Health = 0
                    end)
                elseif _G.Auto_Farm and MagnetLv and v.Name == Mon and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 330 then
                    v.HumanoidRootPart.CFrame = PosMon
                    v.Humanoid:ChangeState(11)
                    if not v.HumanoidRootPart:FindFirstChild("BodyVelocity") then
                        local bv = Instance.new("BodyVelocity")
                        bv.Parent = v.HumanoidRootPart
                        bv.MaxForce = Vector3.new(100000,100000,100000)
                        bv.Velocity = Vector3.new(0,0,0)
                    end
                    sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                    delay(15,function()
                        v.Humanoid.Health = 0
                    end)
                end
                if _G.Auto_Farm and getgenv().AutoBartilo and BartioQuestBring then
                    if v.Name == "Swan Pirate [Lv. 775]" and (v.HumanoidRootPart.Position - PosMonBarto.Position).Magnitude <= 350 and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        v.Humanoid:ChangeState(11)
                        v.HumanoidRootPart.CFrame = PosMonBarto
                        if not v.HumanoidRootPart:FindFirstChild("BodyVelocity") then
                            local bv = Instance.new("BodyVelocity")
                            bv.Parent = v.HumanoidRootPart
                            bv.MaxForce = Vector3.new(100000,100000,100000)
                            bv.Velocity = Vector3.new(0,0,0)
                        end
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                        delay(15,function()
                            v.Humanoid.Health = 0
                        end)
                    end
                end
            end
        end)
    end
end)
section1:addButton("Button", function()
	print("Clicked")
end)
section1:addTextbox("Notification", "Default", function(value, focusLost)
	print("Input", value)

	if focusLost then
		venyx:Notify("Title", value)
	end
end)

section2:addKeybind("Toggle Keybind", Enum.KeyCode.RightControl, function()
	print("Activated Keybind")
	venyx:toggle()
end, function()
	print("Changed Keybind")
end)
section2:addColorPicker("ColorPicker", Color3.fromRGB(50, 50, 50))
section2:addColorPicker("ColorPicker2")
section2:addSlider("Slider", 0, -100, 100, function(value)
	print("Dragged", value)
end)
section2:addDropdown("Dropdown", {"Hello", "World", "Hello World", "Word", 1, 2, 3})
section2:addDropdown("Dropdown", {"Hello", "World", "Hello World", "Word", 1, 2, 3}, function(text)
	print("Selected", text)
end)
section2:addButton("Button")

-- second page
local theme = venyx:addPage("Theme", 5012544693)
local colors = theme:addSection("Colors")

for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
	colors:addColorPicker(theme, color, function(color3)
		venyx:setTheme(theme, color3)
	end)
end

-- load
venyx:SelectPage(venyx.pages[1], true)

section1:addToggle("Fast Attack", _G.FastAttack, function(value)
_G.FastAttack = value
end)

spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.FastAttack then
            local Combat = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
            local Cemara = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework.CameraShaker)
            Cemara.CameraShakeInstance.CameraShakeState = {FadingIn = 3, FadingOut = 2, Sustained = 0, Inactive = 1}
            Combat.activeController.timeToNextAttack = 0
            Combat.activeController.hitboxMagnitude = 50
            Combat.activeController.increment = 3
        end
    end)
end) 
end)
 
 
spawn(function()
   game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if _G.FastAttack then
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
        end
    end)
end) 
end) 
