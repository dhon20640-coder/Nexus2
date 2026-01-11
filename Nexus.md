-- QuestIlha.lua  (RODAR PRIMEIRO, arquivo separado)

local QuestIlha = {}

QuestIlha.QuestData = {
    [1] = {NameQuest = "BanditQuest1", LevelQuest = 1, Mon = "Bandit", CFrameQuest = CFrame.new(1059.37,16.5,1549.99), CFrameMon = CFrame.new(1045,17,1560)},
    [10] = {NameQuest = "JungleQuest", LevelQuest = 1, Mon = "Monkey", CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838), CFrameMon = CFrame.new(-1448.51806640625, 67.85301208496094, 11.46579647064209)},
    [15] = {NameQuest = "JungleQuest", LevelQuest = 2, Mon = "Gorilla", CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838), CFrameMon = CFrame.new(-1129.8836669921875, 40.46354675292969, -525.4237060546875)},
    [30] = {NameQuest = "BuggyQuest1", LevelQuest = 1, Mon = "Pirate", CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498), CFrameMon = CFrame.new(-1103.513427734375, 13.752052307128906, 3896.091064453125)},
    [40] = {NameQuest = "BuggyQuest1", LevelQuest = 2, Mon = "Brute", CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498), CFrameMon = CFrame.new(-1140.083740234375, 14.809885025024414, 4322.92138671875)},
    [60] = {NameQuest = "DesertQuest", LevelQuest = 1, Mon = "Desert Bandit", CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359), CFrameMon = CFrame.new(924.7998046875, 6.44867467880249, 4481.5859375)},
    [75] = {NameQuest = "DesertQuest", LevelQuest = 2, Mon = "Desert Officer", CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359), CFrameMon = CFrame.new(1608.2822265625, 8.614224433898926, 4371.00732421875)},
    [90] = {NameQuest = "SnowQuest", LevelQuest = 1, Mon = "Snow Bandit", CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796), CFrameMon = CFrame.new(1354.347900390625, 87.27277374267578, -1393.946533203125)},
    [100] = {NameQuest = "SnowQuest", LevelQuest = 2, Mon = "Snowman", CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796), CFrameMon = CFrame.new(1201.6412353515625, 144.57958984375, -1550.0670166015625)},
    [120] = {NameQuest = "MarineQuest2", LevelQuest = 1, Mon = "Chief Petty Officer", CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018), CFrameMon = CFrame.new(-4881.23095703125, 22.65204429626465, 4273.75244140625)},
    [150] = {NameQuest = "SkyQuest", LevelQuest = 1, Mon = "Sky Bandit", CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165), CFrameMon = CFrame.new(-4953.20703125, 295.74420166015625, -2899.22900390625)},
    [175] = {NameQuest = "SkyQuest", LevelQuest = 2, Mon = "Dark Master", CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165), CFrameMon = CFrame.new(-5259.8447265625, 391.3976745605469, -2229.035400390625)},
    [190] = {NameQuest = "PrisonerQuest", LevelQuest = 1, Mon = "Prisoner", CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514), CFrameMon = CFrame.new(5098.9736328125, -0.3204058110713959, 474.2373352050781)},
    [210] = {NameQuest = "PrisonerQuest", LevelQuest = 2, Mon = "Dangerous Prisoner", CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514), CFrameMon = CFrame.new(5654.5634765625, 15.633401870727539, 866.2991943359375)},
    [250] = {NameQuest = "ColosseumQuest", LevelQuest = 1, Mon = "Toga Warrior", CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534), CFrameMon = CFrame.new(-1820.21484375, 51.68385696411133, -2740.6650390625)},
    [275] = {NameQuest = "ColosseumQuest", LevelQuest = 2, Mon = "Gladiator", CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534), CFrameMon = CFrame.new(-1292.838134765625, 56.380882263183594, -3339.031494140625)},
    [300] = {NameQuest = "MagmaQuest", LevelQuest = 1, Mon = "Military Soldier", CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395), CFrameMon = CFrame.new(-5411.16455078125, 11.081554412841797, 8454.29296875)},
    [325] = {NameQuest = "MagmaQuest", LevelQuest = 2, Mon = "Military Spy", CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395), CFrameMon = CFrame.new(-5802.8681640625, 86.26241302490234, 8828.859375)},
    [375] = {NameQuest = "FishmanQuest", LevelQuest = 1, Mon = "Fishman Warrior", CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734), CFrameMon = CFrame.new(60878.30078125, 18.482830047607422, 1543.7574462890625)},
    [400] = {NameQuest = "FishmanQuest", LevelQuest = 2, Mon = "Fishman Commando", CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734), CFrameMon = CFrame.new(61922.6328125, 18.482830047607422, 1493.934326171875)},
    [450] = {NameQuest = "SkyExp1Quest", LevelQuest = 1, Mon = "Guarda de Deus", CFrameQuest = CFrame.new(-4721.88867, 843.874695, -1949.96643), CFrameMon = CFrame.new(-4710.04296875, 845.2769775390625, -1927.3079833984375)},
    [475] = {NameQuest = "SkyExp1Quest", LevelQuest = 2, Mon = "Shanda", CFrameQuest = CFrame.new(-7859.09814, 5544.19043, -381.476196), CFrameMon = CFrame.new(-7678.48974609375, 5566.40380859375, -497.2156066894531)},
    [525] = {NameQuest = "SkyExp2Quest", LevelQuest = 1, Mon = "Royal Squad", CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194), CFrameMon = CFrame.new(-7624.25244140625, 5658.13330078125, -1467.354248046875)},
    [550] = {NameQuest = "SkyExp2Quest", LevelQuest = 2, Mon = "Royal Soldier", CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194), CFrameMon = CFrame.new(-7836.75341796875, 5645.6640625, -1790.6236572265625)},
    [625] = {NameQuest = "FountainQuest", LevelQuest = 1, Mon = "Galley Pirate", CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293), CFrameMon = CFrame.new(5551.02197265625, 78.90135192871094, 3930.412841796875)},
    [650] = {NameQuest = "FountainQuest", LevelQuest = 2, Mon = "Galley Captain", CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293), CFrameMon = CFrame.new(5441.95166015625, 42.50205993652344, 4950.09375)},
    [700] = {NameQuest = "Area1Quest", LevelQuest = 1, Mon = "Raider", CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188), CFrameMon = CFrame.new(-728.3267211914062, 52.779319763183594, 2345.7705078125)},
    [725] = {NameQuest = "Area1Quest", LevelQuest = 2, Mon = "Mercenary", CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188), CFrameMon = CFrame.new(-1004.3244018554688, 80.15886688232422, 1424.619384765625)},
    [775] = {NameQuest = "Area2Quest", LevelQuest = 1, Mon = "Swan Pirate", CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898), CFrameMon = CFrame.new(1068.664306640625, 137.61428833007812, 1322.1060791015625)},
    [800] = {NameQuest = "Area2Quest", LevelQuest = 2, Mon = "Factory Staff", CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321), CFrameMon = CFrame.new(73.07867431640625, 81.86344146728516, -27.470672607421875)},
    [875] = {NameQuest = "MarineQuest3", LevelQuest = 1, Mon = "Marine Lieutenant", CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812), CFrameMon = CFrame.new(-2821.372314453125, 75.89727783203125, -3070.089111328125)},
    [900] = {NameQuest = "MarineQuest3", LevelQuest = 2, Mon = "Marine Captain", CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812), CFrameMon = CFrame.new(-1861.2310791015625, 80.17658233642578, -3254.697509765625)},
    [950] = {NameQuest = "ZombieQuest", LevelQuest = 1, Mon = "Zombie", CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061), CFrameMon = CFrame.new(-5657.77685546875, 78.96973419189453, -928.68701171875)},
    [975] = {NameQuest = "ZombieQuest", LevelQuest = 2, Mon = "Vampire", CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061), CFrameMon = CFrame.new(-6037.66796875, 32.18463897705078, -1340.6597900390625)},
    [1000] = {NameQuest = "SnowMountainQuest", LevelQuest = 1, Mon = "Snow Trooper", CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928), CFrameMon = CFrame.new(549.1473388671875, 427.3870544433594, -5563.69873046875)},
    [1050] = {NameQuest = "SnowMountainQuest", LevelQuest = 2, Mon = "Winter Warrior", CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928), CFrameMon = CFrame.new(1142.7451171875, 475.6398010253906, -5199.41650390625)},
    [1100] = {NameQuest = "IceSideQuest", LevelQuest = 1, Mon = "Lab Subordinate", CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852), CFrameMon = CFrame.new(-5707.4716796875, 15.951709747314453, -4513.39208984375)},
    [1125] = {NameQuest = "IceSideQuest", LevelQuest = 2, Mon = "Horned Warrior", CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852), CFrameMon = CFrame.new(-6341.36669921875, 15.951770782470703, -5723.162109375)},
    [1175] = {NameQuest = "FireSideQuest", LevelQuest = 1, Mon = "Magma Ninja", CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457), CFrameMon = CFrame.new(-5449.6728515625, 76.65874481201172, -5808.20068359375)},
    [1200] = {NameQuest = "FireSideQuest", LevelQuest = 2, Mon = "Lava Pirate", CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457), CFrameMon = CFrame.new(-5213.33154296875, 49.73788070678711, -4701.451171875)},
    [1250] = {NameQuest = "ShipQuest1", LevelQuest = 1, Mon = "Ship Deckhand", CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016), CFrameMon = CFrame.new(1212.0111083984375, 150.79205322265625, 33059.24609375)},
    [1275] = {NameQuest = "ShipQuest1", LevelQuest = 2, Mon = "Ship Engineer", CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016), CFrameMon = CFrame.new(919.4786376953125, 43.54401397705078, 32779.96875)},
    [1300] = {NameQuest = "ShipQuest2", LevelQuest = 1, Mon = "Ship Steward", CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125), CFrameMon = CFrame.new(919.4385375976562, 129.55599975585938, 33436.03515625)},
    [1325] = {NameQuest = "ShipQuest2", LevelQuest = 2, Mon = "Ship Officer", CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125), CFrameMon = CFrame.new(1036.0179443359375, 181.4390411376953, 33315.7265625)},
    [1350] = {NameQuest = "FrostQuest", LevelQuest = 1, Mon = "Arctic Warrior", CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984), CFrameMon = CFrame.new(5966.24609375, 62.97002029418945, -6179.3828125)},
    [1375] = {NameQuest = "FrostQuest", LevelQuest = 2, Mon = "Snow Lurker", CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984), CFrameMon = CFrame.new(5407.07373046875, 69.19437408447266, -6880.88037109375)},
    [1425] = {NameQuest = "ForgottenQuest", LevelQuest = 1, Mon = "Sea Soldier", CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193), CFrameMon = CFrame.new(-3028.2236328125, 64.67451477050781, -9775.4267578125)},
    [1450] = {NameQuest = "ForgottenQuest", LevelQuest = 2, Mon = "Water Fighter", CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193), CFrameMon = CFrame.new(-3352.9013671875, 285.01556396484375, -10534.841796875)},
    [1500] = {NameQuest = "PiratePortQuest", LevelQuest = 1, Mon = "Pirate Millionaire", CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984), CFrameMon = CFrame.new(-245.9963836669922, 47.30615234375, 5584.1005859375)},
    [1525] = {NameQuest = "PiratePortQuest", LevelQuest = 2, Mon = "Pistol Billionaire", CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984), CFrameMon = CFrame.new(-187.3301544189453, 86.23987579345703, 6013.513671875)},
    [1575] = {NameQuest = "DragonCrewQuest", LevelQuest = 1, Mon = "Dragon Crew Warrior", CFrameQuest = CFrame.new(6737, 127, -713), CFrameMon = CFrame.new(6737, 127, -713)},
    [1600] = {NameQuest = "DragonCrewQuest", LevelQuest = 2, Mon = "Dragon Crew Archer", CFrameQuest = CFrame.new(6737, 127, -713), CFrameMon = CFrame.new(6743, 484, 209)},
    [1625] = {NameQuest = "AmazonQuest2", LevelQuest = 1, Mon = "Female Islander", CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422), CFrameMon = CFrame.new(4685.25830078125, 735.8078002929688, 815.3425903320312)},
    [1650] = {NameQuest = "AmazonQuest2", LevelQuest = 2, Mon = "Giant Islander", CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422), CFrameMon = CFrame.new(4729.09423828125, 590.436767578125, -36.97627639770508)},
    [1700] = {NameQuest = "MarineTreeIsland", LevelQuest = 1, Mon = "Marine Commodore", CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498), CFrameMon = CFrame.new(2286.0078125, 73.13391876220703, -7159.80908203125)},
    [1725] = {NameQuest = "MarineTreeIsland", LevelQuest = 2, Mon = "Marine Rear Admiral", CFrameQuest = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813), CFrameMon = CFrame.new(3656.773681640625, 160.52406311035156, -7001.5986328125)},
    [1775] = {NameQuest = "DeepForestIsland3", LevelQuest = 1, Mon = "Fishman Raider", CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652), CFrameMon = CFrame.new(-10407.5263671875, 331.76263427734375, -8368.5166015625)},
    [1800] = {NameQuest = "DeepForestIsland3", LevelQuest = 2, Mon = "Capitão Homem-Peixe", CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652), CFrameMon = CFrame.new(-10994.701171875, 352.38140869140625, -9002.1103515625)},
    [1825] = {NameQuest = "DeepForestIsland", LevelQuest = 1, Mon = "Forest Pirate", CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137), CFrameMon = CFrame.new(-13274.478515625, 332.3781433105469, -7769.58056640625)},
    [1850] = {NameQuest = "DeepForestIsland", LevelQuest = 2, Mon = "Mythological Pirate", CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137), CFrameMon = CFrame.new(-13680.607421875, 501.08154296875, -6991.189453125)},
    [1900] = {NameQuest = "DeepForestIsland2", LevelQuest = 1, Mon = "Jungle Pirate", CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953), CFrameMon = CFrame.new(-12256.16015625, 331.73828125, -10485.8369140625)},
    [1925] = {NameQuest = "DeepForestIsland2", LevelQuest = 2, Mon = "Pirata Mosqueteiro", CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953), CFrameMon = CFrame.new(-13457.904296875, 391.545654296875, -9859.177734375)},
    [1975] = {NameQuest = "HauntedQuest1", LevelQuest = 1, Mon = "Reborn Skeleton", CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277), CFrameMon = CFrame.new(-8763.7236328125, 165.72299194335938, 6159.86181640625)},
    [2000] = {NameQuest = "HauntedQuest1", LevelQuest = 2, Mon = "Living Zombie", CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277), CFrameMon = CFrame.new(-10144.1318359375, 138.62667846679688, 5838.0888671875)},
    [2025] = {NameQuest = "HauntedQuest2", LevelQuest = 1, Mon = "Demonic Soul", CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533), CFrameMon = CFrame.new(-9505.8720703125, 172.10482788085938, 6158.9931640625)},
    [2050] = {NameQuest = "HauntedQuest2", LevelQuest = 2, Mon = "Posessed Mummy", CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533), CFrameMon = CFrame.new(-9582.0224609375, 6.251527309417725, 6205.478515625)},
    [2075] = {NameQuest = "NutsIslandQuest", LevelQuest = 1, Mon = "Peanut Scout", CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875), CFrameMon = CFrame.new(-2143.241943359375, 47.72198486328125, -10029.9951171875)},
    [2100] = {NameQuest = "NutsIslandQuest", LevelQuest = 2, Mon = "Peanut President", CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875), CFrameMon = CFrame.new(-1859.35400390625, 38.10316848754883, -10422.4296875)},
    [2125] = {NameQuest = "IceCreamIslandQuest", LevelQuest = 1, Mon = "Ice Cream Chef", CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438), CFrameMon = CFrame.new(-872.24658203125, 65.81957244873047, -10919.95703125)},
    [2150] = {NameQuest = "IceCreamIslandQuest", LevelQuest = 2, Mon = "Ice Cream Commander", CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438), CFrameMon = CFrame.new(-558.06103515625, 112.04895782470703, -11290.7744140625)},
    [2200] = {NameQuest = "CakeQuest1", LevelQuest = 1, Mon = "Cookie Crafter", CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295), CFrameMon = CFrame.new(-2374.13671875, 37.79826354980469, -12125.30859375)},
    [2225] = {NameQuest = "CakeQuest1", LevelQuest = 2, Mon = "Cake Guard", CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295), CFrameMon = CFrame.new(-1598.3070068359375, 43.773197174072266, -12244.5810546875)},
    [2250] = {NameQuest = "CakeQuest2", LevelQuest = 1, Mon = "Equipe de Confeitaria", CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391), CFrameMon = CFrame.new(-1887.8099365234375, 77.6185073852539, -12998.3505859375)},
    [2275] = {NameQuest = "CakeQuest2", LevelQuest = 2, Mon = "Head Baker", CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391), CFrameMon = CFrame.new(-2216.188232421875, 82.884521484375, -12869.2939453125)},
    [2300] = {NameQuest = "ChocQuest1", LevelQuest = 1, Mon = "Guerreiro de Cacau", CFrameQuest = CFrame.new(233.22836303710938, 29.876001358032227, -12201.2333984375), CFrameMon = CFrame.new(-21.55328369140625, 80.57499694824219, -12352.3876953125)},
    [2325] = {NameQuest = "ChocQuest1", LevelQuest = 2, Mon = "Chocolate Bar Battler", CFrameQuest = CFrame.new(233.22836303710938, 29.876001358032227, -12201.2333984375), CFrameMon = CFrame.new(582.590576171875, 77.18809509277344, -12463.162109375)},
    [2350] = {NameQuest = "ChocQuest2", LevelQuest = 1, Mon = "Sweet Thief", CFrameQuest = CFrame.new(150.5066375732422, 30.693693161010742, -12774.5029296875), CFrameMon = CFrame.new(165.1884765625, 76.05885314941406, -12600.8369140625)},
    [2375] = {NameQuest = "ChocQuest2", LevelQuest = 2, Mon = "Candy Rebel", CFrameQuest = CFrame.new(150.5066375732422, 30.693693161010742, -12774.5029296875), CFrameMon = CFrame.new(134.86563110351562, 77.2476806640625, -12876.5478515625)},
    [2400] = {NameQuest = "CandyQuest1", LevelQuest = 1, Mon = "Candy Pirate", CFrameQuest = CFrame.new(-1150.0400390625, 20.378934860229492, -14446.3349609375), CFrameMon = CFrame.new(-1310.5003662109375, 26.016523361206055, -14562.404296875)},
    [2425] = {NameQuest = "CandyQuest1", LevelQuest = 2, Mon = "Snow Demon", CFrameQuest = CFrame.new(-1150.0400390625, 20.378934860229492, -14446.3349609375), CFrameMon = CFrame.new(-880.2006225585938, 71.24776458740234, -14538.609375)},
    [2450] = {NameQuest = "TikiQuest1", LevelQuest = 1, Mon = "Isle Outlaw", CFrameQuest = CFrame.new(-16545.9355, 55.6863556, -173.230499), CFrameMon = CFrame.new(-16120.6035, 116.520554, -103.038849)},
    [2475] = {NameQuest = "TikiQuest1", LevelQuest = 2, Mon = "Island Boy", CFrameQuest = CFrame.new(-16545.9355, 55.6863556, -173.230499), CFrameMon = CFrame.new(-16751.3125, 121.226219, -264.015015)},
    [2500] = {NameQuest = "TikiQuest2", LevelQuest = 1, Mon = "Guerreiro Beijado pelo Sol", CFrameQuest = CFrame.new(-16539.078125, 55.68632888793945, 1051.5738525390625), CFrameMon = CFrame.new(-16294.6748, 32.7874393, 1062.4856)},
    [2525] = {NameQuest = "TikiQuest2", LevelQuest = 2, Mon = "Isle Champion", CFrameQuest = CFrame.new(-16539.078125, 55.68632888793945, 1051.5738525390625), CFrameMon = CFrame.new(-16933.2129, 93.3503036, 999.450989)}
}

function QuestIlha.GetQuestForLevel(level)
    local selected, highest = nil, 0
    for req, data in pairs(QuestIlha.QuestData) do
        if level >= req and req > highest then
            highest = req
            selected = data
        end
    end
    return selected
end

-- expõe o módulo globalmente pra outros scripts do executor
getgenv().QuestIlha = QuestIlha
wait(1)
local PS=game:GetService("Players");local RS=game:GetService("ReplicatedStorage");local WS=game:GetService("Workspace")
local TS=game:GetService("TweenService");local VU=game:GetService("VirtualUser");local LT=game:GetService("Lighting")
local RSvc=game:GetService("RunService")
local Plr=PS.LocalPlayer;repeat task.wait() until Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart");task.wait(2)
local Remotes=RS:WaitForChild("Remotes",5);local CF=Remotes:FindFirstChild("CommF_")
local QuestIlha=getgenv().QuestIlha

getgenv().AF=false getgenv().AK=false getgenv().AB=false getgenv().AS=false getgenv().SA="Melee" getgenv().SP=1
getgenv().AR=false getgenv().SR="Human" getgenv().WP="Melee" getgenv().BM=true getgenv().BringMode=350 getgenv().AC=false
getgenv().CurrentQuestName=nil getgenv().CurrentQuestLevel=nil

Plr.Idled:Connect(function()VU:CaptureController();VU:ClickButton2(Vector2.new())end)

local function GL()local ok,v=pcall(function()return Plr.Data.Level.Value end)return ok and v or 1 end
local function GS()local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart");if not hrp then return 1 end;local x,z=hrp.Position.X,hrp.Position.Z;if x>=-2000 and x<=2000 and z>=-2000 and z<=2000 then return 1 elseif x>2000 and x<=5000 and z>=-1000 and z<=5000 then return 2 elseif x<-2000 or x>5000 or z<-2000 or z>5000 then return 3 else return 1 end end
local function GQ()if not QuestIlha or not QuestIlha.GetQuestForLevel then return nil end;local q=QuestIlha.GetQuestForLevel(GL());if not q then return nil end;local qSea=q.Sea or 1;local pSea=GS();if qSea>pSea then local altQ=QuestIlha.GetLastQuestForSea and QuestIlha.GetLastQuestForSea(pSea);return altQ or q end;return q end
local function HQ()local ok,v=pcall(function()return Plr.PlayerGui.Main.Quest.Visible end)return ok and v end
local function CancelQuest()pcall(function()if CF and HQ()then CF:InvokeServer("AbandonQuest")task.wait(0.3)end end)end
local function IsFarmActive()return getgenv().AF or getgenv().AK or getgenv().AB end
local function SetNoclipLight(char,enable)if not char then return end;for _,p in ipairs(char:GetDescendants())do if p:IsA("BasePart")then if p.Name=="HumanoidRootPart"or p.Name=="UpperTorso"or p.Name=="LowerTorso"or p.Name=="Torso"then p.CanCollide=not enable end end end end
local function RestoreNormalPhysics()pcall(function()local c=Plr.Character;if not c then return end;local hrp=c:FindFirstChild("HumanoidRootPart");local hum=c:FindFirstChild("Humanoid");if not hrp or not hum then return end;SetNoclipLight(c,false);hrp.Anchored=false;hrp.AssemblyLinearVelocity=Vector3.new();hum:ChangeState(Enum.HumanoidStateType.RunningNoPhysics);task.wait(0.1);hum:ChangeState(Enum.HumanoidStateType.Freefall)end)end

local function ApplyFarmPhysics()if not IsFarmActive()then return end;local c=Plr.Character;local hrp=c and c:FindFirstChild("HumanoidRootPart");local hum=c and c:FindFirstChild("Humanoid");if not c or not hrp or not hum then return end;SetNoclipLight(c,true);hrp.Anchored=false;hrp.AssemblyLinearVelocity=Vector3.new();hum:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)end

local function InMyNetWork(o)if isnetworkowner then return isnetworkowner(o)end;local c=Plr.Character;if not c or not c:FindFirstChild("HumanoidRootPart")then return false end;return(o.Position-c.HumanoidRootPart.Position).Magnitude<=getgenv().BringMode end

local function BringMobs(n,playerPos)if not getgenv().BM then return 0 end;local c=Plr.Character;if not c or not c:FindFirstChild("HumanoidRootPart")then return 0 end;local h=c.HumanoidRootPart;local t=playerPos or h.CFrame*CFrame.new(0,-20,0);local b=0;local m=2;for _,e in pairs(WS.Enemies:GetChildren())do if b>=m then break end;if e.Name==n and e:FindFirstChild("Humanoid")and e:FindFirstChild("HumanoidRootPart")and e.Humanoid.Health>0 then local d=(e.HumanoidRootPart.Position-h.Position).Magnitude;if d<=getgenv().BringMode then if InMyNetWork(e.HumanoidRootPart)then pcall(function()e.HumanoidRootPart.CFrame=t;e.HumanoidRootPart.CanCollide=false;e.HumanoidRootPart.Size=Vector3.new(50,50,50);e.Head.CanCollide=false;e.Humanoid.WalkSpeed=0;e.Humanoid.JumpPower=0;e.Humanoid:ChangeState(14);e.Humanoid:ChangeState(11);if e.Humanoid:FindFirstChild("Animator")then e.Humanoid.Animator:Destroy()end;b=b+1 end)end end end end;if sethiddenproperty then pcall(function()sethiddenproperty(Plr,"SimulationRadius",math.huge)end)end;return b end

local function Equip()pcall(function()local c=Plr.Character;if not c or not c:FindFirstChild("Humanoid")then return end;local bp,tool=Plr.Backpack;if getgenv().WP=="Sword"then for _,v in ipairs(bp:GetChildren())do if v:IsA("Tool")and(v.ToolTip=="Sword"or v.Name:find("Katana")or v.Name:find("Blade"))then tool=v break end end end;if not tool then tool=bp:FindFirstChild("Combat")end;if tool then c.Humanoid:EquipTool(tool)end end)end
local function FM(n)local nm,dist=nil,9e9;pcall(function()local c=Plr.Character;local hrp=c and c:FindFirstChild("HumanoidRootPart");if not hrp then return end;for _,m in ipairs(WS.Enemies:GetChildren())do if m.Name==n then local h=m:FindFirstChild("Humanoid");local r=m:FindFirstChild("HumanoidRootPart");if h and r and h.Health>0 then local d=(hrp.Position-r.Position).Magnitude;if d<dist then dist,nm=d,m end end end end end)return nm end
local function GR()local ok,v=pcall(function()return Plr.Data.Race.Value end)return ok and v or"Unknown"end
local function GF()local ok,v=pcall(function()return Plr.Data.Fragments.Value end)return ok and v or 0 end
local function RR()if GF()<3000 or not CF then return false end;local ok=pcall(function()CF:InvokeServer("BlackbeardReward","Reroll","2")end)return ok end
local function FP()pcall(function()LT.GlobalShadows=false;LT.FogEnd=9e9;settings().Rendering.QualityLevel=Enum.QualityLevel.Level01;for _,v in ipairs(WS:GetDescendants())do if v:IsA("BasePart")or v:IsA("UnionOperation")or v:IsA("MeshPart")then v.Material=Enum.Material.Plastic;v.Reflectance=0 elseif v:IsA("Decal")or v:IsA("Texture")then v.Transparency=1 elseif v:IsA("ParticleEmitter")or v:IsA("Trail")then v.Lifetime=NumberRange.new(0)elseif v:IsA("Fire")or v:IsA("SpotLight")or v:IsA("Smoke")or v:IsA("Sparkles")then v.Enabled=false end end end)end
local function AutoHaki()pcall(function()local c=Plr.Character;if not c then return end;if c:FindFirstChild("Buso Haki")or c:FindFirstChild("Enhancement")then return end;local VIM=game:GetService("VirtualInputManager");VIM:SendKeyEvent(true,"J",false,game);task.wait(0.05);VIM:SendKeyEvent(false,"J",false,game)end)end

local ActiveTween=nil;local FollowHB=nil;local GroundTween=nil
local function TweenFollow25(hrp,targetHRP,speed)if not hrp or not targetHRP then return end;speed=speed or 300;local yOffset=25;if ActiveTween then ActiveTween:Cancel();ActiveTween=nil end;if FollowHB then FollowHB:Disconnect();FollowHB=nil end;local targetCF=targetHRP.CFrame*CFrame.new(0,yOffset,0);local distance=(hrp.Position-targetCF.Position).Magnitude;local time=math.max(distance/speed,0.05);ActiveTween=TS:Create(hrp,TweenInfo.new(time,Enum.EasingStyle.Linear),{CFrame=targetCF});ActiveTween:Play();ActiveTween.Completed:Once(function()FollowHB=RSvc.Heartbeat:Connect(function()if not targetHRP or not targetHRP.Parent or not IsFarmActive()then FollowHB:Disconnect();FollowHB=nil;return end;hrp.CFrame=targetHRP.CFrame*CFrame.new(0,yOffset,0)end)end)end

local function TweenToGround(hrp,targetCF,speed)
    if not hrp then return end
    speed=speed or 250
    if GroundTween then 
        GroundTween:Cancel()
        GroundTween=nil 
    end
    local distance=(hrp.Position-targetCF.Position).Magnitude
    local time=math.max(distance/speed,0.1)
    GroundTween=TS:Create(hrp,TweenInfo.new(time,Enum.EasingStyle.Linear),{CFrame=targetCF})
    GroundTween:Play()
    GroundTween.Completed:Wait()
    GroundTween=nil
end

local function StopAllTweens()
    if ActiveTween then 
        ActiveTween:Cancel()
        ActiveTween=nil 
    end
    if FollowHB then 
        FollowHB:Disconnect()
        FollowHB=nil 
    end
    if GroundTween then
        GroundTween:Cancel()
        GroundTween=nil
    end
end

local Fl=loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local Win=Fl:CreateWindow({Title="Nexus Hub V3",SubTitle="Blox Fruits Delta",TabWidth=160,Size=UDim2.fromOffset(580,460),Theme="Darker"})
local TabM=Win:AddTab({Title="Main",Icon="home"});local TabS=Win:AddTab({Title="Shop",Icon="shopping-bag"})
local TabF=Win:AddTab({Title="Farm",Icon="swords"});local TabSt=Win:AddTab({Title="Status",Icon="trending-up"})
local TabSe=Win:AddTab({Title="Settings",Icon="settings"})

TabM:AddParagraph({Title="Nexus Hub V3",Content="Versao Estavel Delta"})
TabM:AddButton({Title="Discord",Description="Copiar link",Callback=function()setclipboard("https://discord.gg/29BDQqHYbJ")end})

TabS:AddSection("Shop")
TabS:AddButton({Title="Comprar Haki",Description="25k Beli",Callback=function()if CF then CF:InvokeServer("BuyHaki","Buso")end end})
TabS:AddButton({Title="Comprar Race",Description="3k Frags (1x)",Callback=function()RR()end})
TabS:AddDropdown("RaceSel",{Title="Selecionar Race",Values={"Human","Mink","Shark","Angel"},Default=1}):OnChanged(function(v)getgenv().SR=v end)
local TG_AR=TabS:AddToggle("AutoR",{Title="Auto Reroll Race",Description="Para ao conseguir",Default=false})
TG_AR:OnChanged(function(v)getgenv().AR=v end)

TabF:AddSection("Farming")
TabF:AddDropdown("Weap",{Title="Weapon Style",Values={"Melee","Sword"},Default=1}):OnChanged(function(v)getgenv().WP=v end)
TabF:AddToggle("AF",{Title="Auto Farm Level",Description="0-2800",Default=false}):OnChanged(function(v)getgenv().AF=v;if v then getgenv().AK=false getgenv().AB=false else RestoreNormalPhysics()end end)
local TG_AK=TabF:AddToggle("AK",{Title="Auto Katakuri",Description="Sea3 Lv1500+",Default=false})
TG_AK:OnChanged(function(v)if v and(GL()<1500 or GS()~=3)then TG_AK:SetValue(false);return end;getgenv().AK=v;if v then getgenv().AF=false getgenv().AB=false else RestoreNormalPhysics()end end)
local TG_AB=TabF:AddToggle("AB",{Title="Auto Bone",Description="Sea3 Lv1500+",Default=false})
TG_AB:OnChanged(function(v)if v and(GL()<1500 or GS()~=3)then TG_AB:SetValue(false);return end;getgenv().AB=v;if v then getgenv().AF=false getgenv().AK=false else RestoreNormalPhysics()end end)

TabSt:AddSlider("Pts",{Title="Pontos por Upgrade",Default=1,Min=1,Max=100,Rounding=0}):OnChanged(function(v)getgenv().SP=v end)
TabSt:AddDropdown("Stat",{Title="Selecionar Status",Values={"Melee","Defense","Sword","Gun","Blox Fruit"},Default=1}):OnChanged(function(v)local m={Melee="Melee",Defense="Defense",Sword="Sword",Gun="Gun",["Blox Fruit"]="Fruit"};getgenv().SA=m[v]end)
TabSt:AddToggle("AS",{Title="Auto Status",Default=false}):OnChanged(function(v)getgenv().AS=v end)

TabSe:AddSection("Server HOP")
TabSe:AddButton({Title="Rejoin",Description="Reconectar",Callback=function()game:GetService("TeleportService"):Teleport(game.PlaceId,Plr)end})
TabSe:AddButton({Title="Hop Server",Description="Poucos players",Callback=function()task.spawn(function()pcall(function()local HS=game:GetService("HttpService");local TS2=game:GetService("TeleportService");local srvs={};local ok,res=pcall(function()return game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100")end);if ok then local d=HS:JSONDecode(res);if d and d.data then for _,s in ipairs(d.data)do if s.playing and s.playing>=1 and s.playing<=8 and s.id~=game.JobId then table.insert(srvs,s.id)end end end end;if #srvs>0 then TS2:TeleportToPlaceInstance(game.PlaceId,srvs[math.random(1,#srvs)],Plr)else TS2:Teleport(game.PlaceId,Plr)end end)end)end})
TabSe:AddButton({Title="FPS Boost",Description="Tirar Lag",Callback=FP})
TabSe:AddSection("Settings Farming")
TabSe:AddToggle("BM",{Title="Bring Mob (2)",Description="Puxa 2 NPC prox.",Default=true}):OnChanged(function(v)getgenv().BM=v end)
TabSe:AddToggle("AC",{Title="Auto Click",Default=false}):OnChanged(function(v)getgenv().AC=v end)

local SG=Instance.new("ScreenGui");SG.Name="NexusToggle";SG.ResetOnSpawn=false;SG.Parent=Plr:WaitForChild("PlayerGui")
local BTN=Instance.new("TextButton");BTN.Size=UDim2.fromOffset(60,60);BTN.Position=UDim2.new(0,20,0,20);BTN.BackgroundColor3=Color3.fromRGB(25,25,35);BTN.Text="N";BTN.TextColor3=Color3.fromRGB(255,165,0);BTN.TextSize=18;BTN.Font=Enum.Font.GothamBold;BTN.Parent=SG
local UIC=Instance.new("UICorner");UIC.CornerRadius=UDim.new(0,12);UIC.Parent=BTN;local UIS=Instance.new("UIStroke");UIS.Color=Color3.fromRGB(255,165,0);UIS.Thickness=2;UIS.Parent=BTN
BTN.MouseButton1Click:Connect(function()Win.Root.Visible=not Win.Root.Visible end)

local RA,RH;task.spawn(function()task.wait(2);pcall(function()local M=RS:WaitForChild("Modules",5);if M then local N=M:FindFirstChild("Net");if N then RA=N:FindFirstChild("RE/RegisterAttack");RH=N:FindFirstChild("RE/RegisterHit")end end end)end)

task.spawn(function()while task.wait(0.1)do if(getgenv().AF or getgenv().AK or getgenv().AB)and RA and RH then pcall(function()local tgts,tName={},nil;for _,m in ipairs(WS.Enemies:GetChildren())do if m:FindFirstChild("Head")and m:FindFirstChild("Humanoid")and m.Humanoid.Health>0 then if getgenv().AF then local q=GQ();if q and m.Name==(q.M or q.Mon)then table.insert(tgts,{m,m.Head});tName=(q.M or q.Mon)end elseif getgenv().AK and GS()==3 then if m.Name=="Cookie Crafter"or m.Name=="Cake Guard"or m.Name=="Baking Staff"or m.Name=="Head Baker"then table.insert(tgts,{m,m.Head});tName=m.Name end elseif getgenv().AB and GS()==3 then if m.Name=="Reborn Skeleton"or m.Name=="Living Zombie"or m.Name=="Demonic Soul"or m.Name=="Posessed Mummy"then table.insert(tgts,{m,m.Head});tName=m.Name end end end end;if #tgts>0 then local c=Plr.Character;local hrp=c and c:FindFirstChild("HumanoidRootPart");if hrp and tName then local targetMob=tgts[1][1];if targetMob and targetMob:FindFirstChild("HumanoidRootPart")then local dist=(hrp.Position-targetMob.HumanoidRootPart.Position).Magnitude;if dist<=50 then BringMobs(tName,hrp.CFrame*CFrame.new(0,-20,0))end end end;RA:FireServer(0.1);RH:FireServer(tgts[1][2],tgts)end end)end end end)

task.spawn(function()while task.wait(0.1)do if getgenv().AC and RA and RH then pcall(function()local c=Plr.Character;local hrp=c and c:FindFirstChild("HumanoidRootPart");if not hrp then return end;local tgts={};for _,m in ipairs(WS.Enemies:GetChildren())do if m:FindFirstChild("Head")and m:FindFirstChild("Humanoid")and m.Humanoid.Health>0 and m:FindFirstChild("HumanoidRootPart")then local dist=(hrp.Position-m.HumanoidRootPart.Position).Magnitude;if dist<=50 then table.insert(tgts,{m,m.Head})end end end;for _,p in ipairs(PS:GetPlayers())do if p~=Plr and p.Character and p.Character:FindFirstChild("Head")and p.Character:FindFirstChild("Humanoid")and p.Character.Humanoid.Health>0 and p.Character:FindFirstChild("HumanoidRootPart")then local dist=(hrp.Position-p.Character.HumanoidRootPart.Position).Magnitude;if dist<=50 then table.insert(tgts,{p.Character,p.Character.Head})end end end;if #tgts>0 then RA:FireServer(0.1);RH:FireServer(tgts[1][2],tgts)end end)end end end)

task.spawn(function()while task.wait(0.1)do pcall(function()local c=Plr.Character;if not c then return end;local hrp=c:FindFirstChild("HumanoidRootPart");local hum=c:FindFirstChild("Humanoid");if not hrp or not hum then return end;if hum.Health<=0 and IsFarmActive()then StopAllTweens();repeat task.wait()until Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")and Plr.Character:FindFirstChild("Humanoid")and Plr.Character.Humanoid.Health>0;c=Plr.Character;hrp=c.HumanoidRootPart;hum=c.Humanoid;task.wait(1)end;local function farmFlag(flag,mobSingle,listNames)if not getgenv()[flag]then StopAllTweens();return end;AutoHaki();Equip();local tm;if listNames then for _,n in ipairs(listNames)do tm=FM(n);if tm then break end end else tm=mobSingle end;if tm then local h=tm:FindFirstChild("Humanoid");local r=tm:FindFirstChild("HumanoidRootPart");if h and r and h.Health>0 then SetNoclipLight(c,true);hum:ChangeState(Enum.HumanoidStateType.RunningNoPhysics);TweenFollow25(hrp,r,300);while tm.Parent and h.Health>0 and getgenv()[flag]and hum.Health>0 do hrp.AssemblyLinearVelocity=Vector3.new();Equip();task.wait(0.05)end;StopAllTweens()end else StopAllTweens()end end;if IsFarmActive()then local hasMob=false;if getgenv().AF then local q=GQ();if q then local mobName=q.M or q.Mon;if FM(mobName)then hasMob=true end end elseif getgenv().AK and GS()==3 then for _,n in ipairs({"Cookie Crafter","Cake Guard","Baking Staff","Head Baker"})do if FM(n)then hasMob=true break end end elseif getgenv().AB and GS()==3 then for _,n in ipairs({"Reborn Skeleton","Living Zombie","Demonic Soul","Posessed Mummy"})do if FM(n)then hasMob=true break end end end;if not hasMob then StopAllTweens();SetNoclipLight(c,false);hrp.Anchored=false;hrp.AssemblyLinearVelocity=Vector3.new();hrp.AssemblyAngularVelocity=Vector3.new();if hrp.Position.Y>15 then local ray=Ray.new(hrp.Position,Vector3.new(0,-1000,0));local hit,pos=WS:FindPartOnRay(ray,c);if hit then local targetY=pos.Y+5;local groundCF=CFrame.new(hrp.Position.X,targetY,hrp.Position.Z);TweenToGround(hrp,groundCF,250);task.wait(0.3)end end;hum:ChangeState(Enum.HumanoidStateType.Freefall);task.wait(0.5);hrp.AssemblyLinearVelocity=Vector3.new();hrp.AssemblyAngularVelocity=Vector3.new()else SetNoclipLight(c,true);hum:ChangeState(Enum.HumanoidStateType.RunningNoPhysics);hrp.AssemblyLinearVelocity=Vector3.new()end else StopAllTweens();SetNoclipLight(c,false);hrp.Anchored=false end;if getgenv().AF then local q=GQ();if not q then return end;local questName=q.N or q.NameQuest;local questLevel=q.L or q.LevelQuest;local mobName=q.M or q.Mon;local mobSpawnCF=q.SC or q.CFrameMon;if getgenv().CurrentQuestName~=questName or getgenv().CurrentQuestLevel~=questLevel then CancelQuest();getgenv().CurrentQuestName=nil;getgenv().CurrentQuestLevel=nil;StopAllTweens();task.wait(0.5)end;if not HQ()and CF then local success=pcall(function()CF:InvokeServer("StartQuest",questName,questLevel)end);if success then getgenv().CurrentQuestName=questName;getgenv().CurrentQuestLevel=questLevel;task.wait(0.3)end end;local m=FM(mobName);if m and getgenv().AF then farmFlag("AF",m)else StopAllTweens();local spawnY=(mobSpawnCF.Position.Y>0)and mobSpawnCF.Position.Y or 50;local spawnCF=CFrame.new(mobSpawnCF.Position.X,spawnY,mobSpawnCF.Position.Z);TweenToGround(hrp,spawnCF,250);task.wait(0.5)end elseif getgenv().AK then if GS()==3 and GL()>=1500 then farmFlag("AK",nil,{"Cookie Crafter","Cake Guard","Baking Staff","Head Baker"})else getgenv().AK=false;TG_AK:SetValue(false);StopAllTweens()end elseif getgenv().AB then if GS()==3 and GL()>=1500 then farmFlag("AB",nil,{"Reborn Skeleton","Living Zombie","Demonic Soul","Posessed Mummy"})else getgenv().AB=false;TG_AB:SetValue(false);StopAllTweens()end end end)end end)

task.spawn(function()while task.wait(1)do if getgenv().AS and getgenv().SA and CF then pcall(function()CF:InvokeServer("AddPoint",getgenv().SA,getgenv().SP)end)end end end)
task.spawn(function()while task.wait(3)do if getgenv().AR and CF then pcall(function()if GR()==getgenv().SR then getgenv().AR=false;TG_AR:SetValue(false);return end;local ok=RR();if not ok then getgenv().AR=false;TG_AR:SetValue(false)end end)end end end)

Fl:Notify({Title="Nexus Hub V3",Content="Carregado! Sea: "..GS().." | Lv: "..GL(),Duration=5})
-- ============================
-- MÓDULO AUTO SABER - NEXUS HUB V3 (CORRIGIDO SEQUÊNCIA)
-- ============================

getgenv().AutoSaber = false
local SS = {H=false,T=false,C=false,CF=false,SM=false,RM=false,ML=false,R=false,D=false,B=false}
local ATw,AHB,NCLoop=nil,nil,nil

-- PATHS DOS OBJETOS
local PATHS = {
    Torch = {"Map","Jungle","Torch"},
    TorchToDesert = {"Map","Desert","Burn","Cup"}, -- Tocha vai pro deserto
    Cup = {"Map","Desert","Burn","Cup"},
    Lava = {"Map","Desert","Burn","Lava"},
    SickMan = {"Map","Jungle","QuestPlates","Plate1"},
    RichMan = {"Map","Mysterious Merchant","Mysterious Merchant"},
    Relic = {"Map","Jungle","QuestPlates","Plate2"},
    RelicToDesert = {"Map","Desert","Burn","Part"}, -- Relíquia vai pra porta
    DesertDoor = {"Map","Desert","Burn","Part"},
    FinalSaber = {"Map","Desert","Burn","Saber"},
    JungleFinal = {"Map","Jungle","Final"}
}

-- FUNÇÕES AUXILIARES
local function Stop()
    if ATw then ATw:Cancel()ATw=nil end
    if AHB then AHB:Disconnect()AHB=nil end
    if NCLoop then NCLoop:Disconnect()NCLoop=nil end
end

local function CI(n)
    local ok,r=pcall(function()return Plr.Backpack:FindFirstChild(n)or(Plr.Character and Plr.Character:FindFirstChild(n))end)
    return ok and r~=nil
end

local function HS()return CI("Saber")or CI("Saber Expert")end

local function GetCF(pathTable)
    local obj = WS
    for _, key in ipairs(pathTable) do
        obj = obj:FindFirstChild(key)
        if not obj then return nil end
    end
    if obj:IsA("Model")then
        local p=obj.PrimaryPart or obj:FindFirstChild("HumanoidRootPart")or obj:FindFirstChildWhichIsA("BasePart")
        return p and p.CFrame
    elseif obj:IsA("BasePart")then return obj.CFrame
    elseif obj:FindFirstChild("Handle")then return obj.Handle.CFrame end
    return nil
end

-- NOCLIP
local function EnableNoClip(char)
    if not char then return end
    pcall(function()
        if NCLoop then NCLoop:Disconnect()end
        NCLoop = RSvc.Stepped:Connect(function()
            if not getgenv().AutoSaber then if NCLoop then NCLoop:Disconnect()NCLoop=nil end return end
            pcall(function()for _,v in pairs(char:GetDescendants())do if v:IsA("BasePart")then v.CanCollide=false v.Velocity=Vector3.new()v.RotVelocity=Vector3.new()end end end)
        end)
    end)
end

local function DisableNoClip()
    if NCLoop then NCLoop:Disconnect()NCLoop=nil end
    pcall(function()local c=Plr.Character if c then for _,v in pairs(c:GetDescendants())do if v:IsA("BasePart")and v.Name~="HumanoidRootPart"then v.CanCollide=true end end end end)
end

-- ATUALIZAR STATUS
local function US()
    pcall(function()
        SS.H=HS()SS.T=CI("Torch")SS.C=CI("Cup")
        local co=Plr.Backpack:FindFirstChild("Cup")or(Plr.Character and Plr.Character:FindFirstChild("Cup"))
        if co and co:FindFirstChild("Handle")then local c=co.Handle.Color SS.CF=(c.R>0.9 and c.G<0.1 and c.B<0.1)else SS.CF=false end
        if WS.Map:FindFirstChild("Jungle")and WS.Map.Jungle:FindFirstChild("QuestPlates")then
            local d=WS.Map.Jungle.QuestPlates:FindFirstChild("Door")SS.SM=d and d.CanCollide==false else SS.SM=false end
        if WS.Map:FindFirstChild("Jungle")and WS.Map.Jungle:FindFirstChild("Final")then
            local p=WS.Map.Jungle.Final:FindFirstChild("Part")SS.B=p and p.Transparency==1 else SS.B=false end
        SS.RM=Plr.Character and Plr.Character:FindFirstChild("RichSight")~=nil
        SS.ML=not WS.Enemies:FindFirstChild("Saber Expert")SS.R=CI("Relic")
        if WS.Map:FindFirstChild("Desert")and WS.Map.Desert:FindFirstChild("Burn")then
            local dp=WS.Map.Desert.Burn:FindFirstChild("Part")SS.D=dp and dp.Transparency==1 else SS.D=false end
    end)
end

-- TWEEN
local function ST(tCF,spd)
    if not getgenv().AutoSaber or not tCF then return false end
    local c=Plr.Character local hrp=c and c:FindFirstChild("HumanoidRootPart")
    local hum=c and c:FindFirstChild("Humanoid")
    if not hrp or not hum then return false end
    local dst=(hrp.Position-tCF.Position).Magnitude
    if dst<5 then return true end
    Stop()spd=spd or 300 local tm=math.max(dst/spd,0.1)
    EnableNoClip(c)hrp.Anchored=false hrp.AssemblyLinearVelocity=Vector3.new()
    if hum then hum:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)end
    local ti=TweenInfo.new(tm,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut)
    ATw=TS:Create(hrp,ti,{CFrame=tCF})
    AHB=RSvc.Heartbeat:Connect(function()
        if not getgenv().AutoSaber or not hrp or not hrp.Parent then Stop()return end
        pcall(function()hrp.AssemblyLinearVelocity=Vector3.new()for _,v in pairs(c:GetDescendants())do if v:IsA("BasePart")then v.CanCollide=false end end end)
    end)
    ATw:Play()local cmp=false ATw.Completed:Connect(function()cmp=true end)
    local w=0 while not cmp and w<tm+2 and getgenv().AutoSaber do task.wait(0.1)w=w+0.1 end
    Stop()if hrp and hrp.Parent then hrp.Anchored=false hrp.AssemblyLinearVelocity=Vector3.new()end
    task.wait(0.3)return getgenv().AutoSaber
end

-- CLICK/PROXIMITY
local function ClickObj(p)if not p then return false end pcall(function()local cd=p:FindFirstChildOfClass("ClickDetector")if cd then fireclickdetector(cd)end end)return true end
local function ProxObj(o)if not o then return false end pcall(function()local pp=o:FindFirstChildOfClass("ProximityPrompt")if pp then fireproximityprompt(pp,5)end end)return true end

-- INTERAGIR COM OBJETO
local function Interact(path,useFP,attempts)
    attempts=attempts or 12
    local cf=GetCF(path)if not cf then print("[Auto Saber] Objeto não encontrado:",table.concat(path,"/"))return false end
    if not ST(cf,300)then return false end task.wait(0.5)
    local success=false
    pcall(function()
        local obj=WS for _,k in ipairs(path)do obj=obj:FindFirstChild(k)if not obj then return end end
        local target=obj:FindFirstChild("Handle")or obj
        local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")if not hrp then return end
        EnableNoClip(Plr.Character)
        for i=1,attempts do 
            if not getgenv().AutoSaber then break end
            hrp.CFrame=target.CFrame task.wait(0.2)
            if useFP then ProxObj(target)else ClickObj(target)end
            task.wait(0.3)US()
            -- Verifica se completou baseado no path
            if path==PATHS.Torch and SS.T then success=true break end
            if path==PATHS.Cup and SS.C then success=true break end
            if path==PATHS.Lava and SS.CF then success=true break end
            if path==PATHS.SickMan and SS.SM then success=true break end
            if path==PATHS.Relic and SS.R then success=true break end
        end
    end)
    DisableNoClip()task.wait(1)US()return success
end

-- ATIVAR BOTÕES
local function AB()
    if SS.B then return true end if not getgenv().AutoSaber then return false end
    local finalObj=nil pcall(function()local j=WS.Map:FindFirstChild("Jungle")if j then finalObj=j:FindFirstChild("Final")end end)
    if not finalObj then print("[Auto Saber] Jungle/Final não encontrado!")return false end
    local firstButton=nil
    for _,o in ipairs(finalObj:GetDescendants())do if o:IsA("Part")and o.Name=="Part"and o.Transparency<1 then firstButton=o break end end
    if not firstButton then return false end
    if not ST(firstButton.CFrame+Vector3.new(0,5,0),300)then return false end task.wait(0.5)
    pcall(function()
        local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")if not hrp then return end
        EnableNoClip(Plr.Character)
        for _,o in ipairs(finalObj:GetDescendants())do
            if not getgenv().AutoSaber then break end
            if o:IsA("Part")and o.Name=="Part"and o.Transparency<1 then
                for i=1,5 do if not getgenv().AutoSaber then break end
                    hrp.CFrame=o.CFrame+Vector3.new(0,3,0)task.wait(0.3)ClickObj(o)task.wait(0.3)US()if SS.B then break end
                end if SS.B then break end
            end
        end
    end)
    DisableNoClip()task.wait(1)US()return SS.B
end

-- PEGAR TOCHA (vai pra Jungle)
local function GT()
    if SS.T then return true end 
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo pegar Tocha na Jungle...")
    return Interact(PATHS.Torch,true)
end

-- PEGAR CUP (vai pro Deserto)
local function GC()
    if SS.C then return true end 
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo pegar Cup no Deserto...")
    return Interact(PATHS.Cup,false)
end

-- ENCHER CUP (fica no Deserto)
local function FC()
    if SS.CF then return true end 
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Enchendo Cup com Lava...")
    return Interact(PATHS.Lava,false)
end

-- SICK MAN (volta pra Jungle)
local function TSM()
    if SS.SM then return true end 
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo falar com Sick Man na Jungle...")
    return Interact(PATHS.SickMan,false)
end

-- RICH MAN
local function TRM()
    if SS.RM then return true end if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo falar com Rich Man...")
    local cf=GetCF(PATHS.RichMan)if not cf then return false end
    if not ST(cf,300)then return false end task.wait(0.5)
    pcall(function()
        local m=WS.Map:FindFirstChild("Mysterious Merchant")if not m then return end
        local n=m:FindFirstChild("Mysterious Merchant")
        if not n or not n:FindFirstChild("HumanoidRootPart")then return end
        local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")if not hrp then return end
        for i=1,12 do if not getgenv().AutoSaber then break end
            hrp.CFrame=n.HumanoidRootPart.CFrame task.wait(0.3)ClickObj(n)task.wait(0.5)US()if SS.RM then break end
        end
    end)
    task.wait(1.5)US()return SS.RM
end

-- DERROTAR BOSS
local function DML()
    if SS.ML then return true end if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo derrotar Saber Expert...")
    -- Busca posição do boss dinamicamente
    local bossCF=nil
    pcall(function()
        local boss=WS.Enemies:FindFirstChild("Saber Expert")
        if boss and boss:FindFirstChild("HumanoidRootPart")then
            bossCF=boss.HumanoidRootPart.CFrame
        end
    end)
    -- Se não encontrou, vai pra área aproximada
    if not bossCF then bossCF=CFrame.new(-2950,123,5400)end
    ST(bossCF+Vector3.new(0,20,0),300)task.wait(1)
    local mw,w=120,0
    while getgenv().AutoSaber and w<mw do US()if SS.ML then return true end
        local m=WS.Enemies:FindFirstChild("Saber Expert")
        if m then local h=m:FindFirstChild("Humanoid")local r=m:FindFirstChild("HumanoidRootPart")
            if h and r and h.Health>0 then local c=Plr.Character local hrp=c and c:FindFirstChild("HumanoidRootPart")
                if hrp then repeat if not getgenv().AutoSaber then break end
                    pcall(function()AutoHaki()Equip()EnableNoClip(c)hrp.AssemblyLinearVelocity=Vector3.new()hrp.CFrame=r.CFrame*CFrame.new(0,15,0)end)
                    task.wait(0.1)until not m.Parent or h.Health<=0 or not getgenv().AutoSaber
                end
            end
        end task.wait(1)w=w+1
    end DisableNoClip()US()return SS.ML
end

-- PEGAR RELIC (volta pra Jungle)
local function GR()
    if SS.R then return true end 
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Indo pegar Relíquia na Jungle...")
    return Interact(PATHS.Relic,false)
end

-- ABRIR PORTA (vai pro Deserto com Relíquia)
local function OD()
    if SS.D then return true end 
    if not getgenv().AutoSaber then return false end
    if not SS.R then print("[Auto Saber] ERRO: Tentando abrir porta sem Relíquia!")return false end
    print("[Auto Saber] Indo abrir Porta no Deserto com Relíquia...")
    local cf=GetCF(PATHS.DesertDoor)if not cf then print("[Auto Saber] Porta não encontrada!")return false end
    if not ST(cf,300)then return false end task.wait(0.5)
    pcall(function()
        local dr=WS.Map.Desert.Burn:FindFirstChild("Part")if not dr then return end
        local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")if not hrp then return end
        EnableNoClip(Plr.Character)
        for i=1,12 do if not getgenv().AutoSaber then break end
            hrp.CFrame=dr.CFrame task.wait(0.3)ClickObj(dr)task.wait(0.5)US()if SS.D then break end
        end
    end)
    DisableNoClip()task.wait(1.5)US()return SS.D
end

-- COLETAR SABER
local function CS()
    if not getgenv().AutoSaber then return false end
    print("[Auto Saber] Coletando Saber final...")
    local cf=GetCF(PATHS.FinalSaber)if not cf then print("[Auto Saber] Saber não encontrado!")return false end
    if not ST(cf,300)then return false end task.wait(1)
    pcall(function()
        local sb=WS.Map.Desert.Burn:FindFirstChild("Saber")
        if not sb or not sb:FindFirstChild("Handle")then return end
        local hrp=Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")if not hrp then return end
        EnableNoClip(Plr.Character)
        for i=1,25 do if not getgenv().AutoSaber then break end
            hrp.CFrame=sb.Handle.CFrame task.wait(0.2)US()if SS.H then break end
        end
    end)
    DisableNoClip()task.wait(1)US()return SS.H
end

-- PRÉ-REQUISITOS
local function CanProceed(s)
    if s=="B"then return true end 
    if s=="T"then return SS.B end
    if s=="C"then return SS.B and SS.T end 
    if s=="CF"then return SS.B and SS.T and SS.C end
    if s=="SM"then return SS.B and SS.T and SS.C and SS.CF end
    if s=="RM"then return SS.B and SS.T and SS.C and SS.CF and SS.SM end
    if s=="ML"then return SS.B and SS.T and SS.C and SS.CF and SS.SM and SS.RM end
    if s=="R"then return SS.B and SS.T and SS.C and SS.CF and SS.SM and SS.RM and SS.ML end
    if s=="D"then return SS.B and SS.T and SS.C and SS.CF and SS.SM and SS.RM and SS.ML and SS.R end
    return false
end

-- UI
local TabQI=Win:AddTab({Title="Quests & Itens",Icon="package"})
TabQI:AddSection("Auto Saber Quest")
TabQI:AddParagraph({Title="Status do Saber",Content="Sistema automático de Quest do Saber"})
local SL=TabQI:AddParagraph({Title="Progresso",Content="Aguardando ativação..."})
local TG=TabQI:AddToggle("AutoSaber",{Title="Auto Saber",Description="Completa a Quest do Saber automaticamente",Default=false})

TG:OnChanged(function(v)
    getgenv().AutoSaber=v
    if v then Fl:Notify({Title="Auto Saber",Content="Auto Saber ativado!",Duration=3})
    else Stop()DisableNoClip()SL:SetDesc("⏸️ Auto Saber pausado")Fl:Notify({Title="Auto Saber",Content="Auto Saber desativado.",Duration=3})end
end)

-- LOOP PRINCIPAL
task.spawn(function()
    while task.wait(2)do if getgenv().AutoSaber then pcall(function()US()
        if SS.H then getgenv().AutoSaber=false TG:SetValue(false)DisableNoClip()
            SL:SetDesc("✅ Saber obtido com sucesso!")Fl:Notify({Title="Auto Saber",Content="Saber obtido! Quest completa.",Duration=5})return end
        
        -- SEQUÊNCIA CORRETA COM VALIDAÇÃO DE PRÉ-REQUISITOS
        if not SS.B then 
            SL:SetDesc("🔘 [1/9] Ativando botões na Jungle...")AB()
        elseif not SS.T and CanProceed("T")then 
            SL:SetDesc("🔥 [2/9] Pegando Tocha (Jungle → Item)...")GT()
        elseif not SS.C and CanProceed("C")then 
            SL:SetDesc("🍵 [3/9] Pegando Cup (Tocha → Deserto)...")GC()
        elseif not SS.CF and CanProceed("CF")then 
            SL:SetDesc("🌋 [4/9] Enchendo Cup com Lava (Deserto)...")FC()
        elseif not SS.SM and CanProceed("SM")then 
            SL:SetDesc("💬 [5/9] Falando com Sick Man (Cup → Jungle)...")TSM()
        elseif not SS.RM and CanProceed("RM")then 
            SL:SetDesc("💰 [6/9] Falando com Rich Man...")TRM()
        elseif not SS.ML and CanProceed("ML")then 
            SL:SetDesc("⚔️ [7/9] Derrotando Saber Expert...")DML()
        elseif not SS.R and CanProceed("R")then 
            SL:SetDesc("📿 [8/9] Coletando Relíquia (Jungle)...")GR()
        elseif not SS.D and CanProceed("D")then 
            SL:SetDesc("🚪 [9/9] Abrindo Porta (Relíquia → Deserto)...")OD()
        elseif SS.D and SS.R then 
            SL:SetDesc("⚔️ [FINAL] Coletando Saber (Deserto)...")CS()
        else 
            SL:SetDesc("⏳ Aguardando conclusão de etapa anterior...")task.wait(2)
        end
    end)end end
end)
-- ============================
-- MÓDULO AUTO SEA 2 - NEXUS HUB V3
-- Cole abaixo do módulo Auto Saber
-- ============================

getgenv().AutoSea2 = false
local QuestStep = 1
local BossDefeated = false

-- Função de Notificação
local function Notify(text)
    Fl:Notify({Title="Auto Sea 2", Content=text, Duration=5})
end

-- Verificar Level
local function CheckLevel()
    return Plr.Level.Value >= 700
end

-- Verificar se tem a chave
local function HasKey()
    local ok, r = pcall(function()
        return Plr.Backpack:FindFirstChild("Key") or (Plr.Character and Plr.Character:FindFirstChild("Key"))
    end)
    return ok and r ~= nil
end

-- Tween suave com Heartbeat
local function TweenTo(targetCF, speed)
    speed = speed or 300
    local Character = Plr.Character
    if not Character then return false end
    
    local HRP = Character:FindFirstChild("HumanoidRootPart")
    if not HRP then return false end
    
    local distance = (HRP.Position - targetCF.Position).Magnitude
    local duration = distance / speed
    
    local tweenInfo = TweenInfo.new(duration, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut)
    local tween = TS:Create(HRP, tweenInfo, {CFrame = targetCF})
    
    -- NoClip durante movimento
    local connection
    connection = RSvc.Heartbeat:Connect(function()
        if not getgenv().AutoSea2 then
            connection:Disconnect()
            return
        end
        for _, v in pairs(Character:GetDescendants()) do
            if v:IsA("BasePart") then
                v.CanCollide = false
            end
        end
    end)
    
    tween:Play()
    tween.Completed:Wait()
    
    if connection then connection:Disconnect() end
    task.wait(0.5)
    return getgenv().AutoSea2
end

-- Interagir com NPC
local function TalkToNPC(npcName, position)
    if not TweenTo(position, 300) then return false end
    
    local attempts = 0
    while attempts < 15 and getgenv().AutoSea2 do
        local npc = WS.NPCs:FindFirstChild(npcName)
        if npc and npc:FindFirstChild("HumanoidRootPart") then
            local HRP = Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")
            if HRP then
                HRP.CFrame = npc.HumanoidRootPart.CFrame
                task.wait(0.3)
                
                -- Click no NPC
                pcall(function()
                    local clickDetector = npc:FindFirstChildOfClass("ClickDetector")
                    if clickDetector then
                        fireclickdetector(clickDetector)
                    end
                end)
                task.wait(0.5)
            end
        end
        attempts = attempts + 1
        task.wait(0.5)
    end
    return true
end

-- Abrir porta com chave
local function OpenDoor(doorPosition)
    if not HasKey() then return false end
    if not TweenTo(doorPosition, 300) then return false end
    
    local attempts = 0
    while attempts < 15 and getgenv().AutoSea2 do
        local door = WS.Map:FindFirstChild("Ice")
        if door then door = door:FindFirstChild("Door") end
        
        if door then
            local HRP = Plr.Character and Plr.Character:FindFirstChild("HumanoidRootPart")
            if HRP then
                HRP.CFrame = door.CFrame
                task.wait(0.2)
                
                pcall(function()
                    local clickDetector = door:FindFirstChildOfClass("ClickDetector")
                    if clickDetector then
                        fireclickdetector(clickDetector)
                    end
                end)
                task.wait(0.3)
            end
        end
        attempts = attempts + 1
        task.wait(0.5)
    end
    return true
end

-- Farm Ice Admiral
local function FarmBoss(spawnPosition)
    TweenTo(spawnPosition, 300)
    task.wait(1)
    
    local maxTime = 120
    local elapsed = 0
    
    while getgenv().AutoSea2 and elapsed < maxTime do
        local boss = WS.Enemies:FindFirstChild("Ice Admiral")
        
        if boss then
            local humanoid = boss:FindFirstChild("Humanoid")
            local bossHRP = boss:FindFirstChild("HumanoidRootPart")
            
            if humanoid and bossHRP and humanoid.Health > 0 then
                local Character = Plr.Character
                local HRP = Character and Character:FindFirstChild("HumanoidRootPart")
                
                if HRP then
                    repeat
                        if not getgenv().AutoSea2 then break end
                        
                        pcall(function()
                            AutoHaki()
                            Equip()
                            HRP.CFrame = bossHRP.CFrame * CFrame.new(0, 20, 15)
                        end)
                        
                        task.wait(0.1)
                    until not boss.Parent or humanoid.Health <= 0 or not getgenv().AutoSea2
                    
                    BossDefeated = true
                    return true
                end
            end
        end
        
        task.wait(1)
        elapsed = elapsed + 1
    end
    
    return BossDefeated
end

-- Sequência da Quest
local function StartSea2Quest()
    if not CheckLevel() then
        Notify("Você precisa de Level 700+!")
        getgenv().AutoSea2 = false
        return
    end
    
    -- Passo 1: Military Detective (pegar chave)
    if QuestStep == 1 and not HasKey() then
        Notify("Indo ao Military Detective...")
        TalkToNPC("Military Detective", CFrame.new(5084.8, 5.68, 743.2))
        task.wait(3)
        if HasKey() then
            QuestStep = 2
        end
    end
    
    -- Passo 2: Abrir porta na Ice Cave
    if QuestStep == 2 then
        Notify("Indo para Ice Cave abrir a porta...")
        OpenDoor(CFrame.new(1266.5, 9.0, -1245.1))
        task.wait(2)
        QuestStep = 3
    end
    
    -- Passo 3: Derrotar Ice Admiral
    if QuestStep == 3 and not BossDefeated then
        Notify("Derrotando Ice Admiral...")
        if FarmBoss(CFrame.new(1316.7, 26.9, -1338.1)) then
            QuestStep = 4
        end
    end
    
    -- Passo 4: Retornar ao Military Detective
    if QuestStep == 4 then
        Notify("Retornando ao Military Detective...")
        TalkToNPC("Military Detective", CFrame.new(5084.8, 5.68, 743.2))
        task.wait(2)
        QuestStep = 5
    end
    
    -- Passo 5: Experienced Captain
    if QuestStep == 5 then
        Notify("Finalizando com Experienced Captain...")
        TalkToNPC("Experienced Captain", CFrame.new(-4914.8, 717.7, -2622.3))
        task.wait(2)
        
        Notify("Quest do Second Sea completa! ✅")
        getgenv().AutoSea2 = false
    end
end

-- TOGGLE (Cole após o Toggle do Auto Saber)
local Sea2Toggle = TabQI:AddToggle("AutoSea2", {
    Title = "Auto Sea 2",
    Description = "lvl 700+",
    Default = false
})

Sea2Toggle:OnChanged(function(value)
    getgenv().AutoSea2 = value
    
    if value then
        QuestStep = 1
        BossDefeated = false
        Notify("Auto Sea 2 ativado!")
    else
        Notify("Auto Sea 2 desativado")
    end
end)

-- Loop Principal
task.spawn(function()
    while task.wait(2) do
        if getgenv().AutoSea2 then
            pcall(function()
                StartSea2Quest()
            end)
        end
    end
end)
