
![Goat Gatage](https://i.ibb.co/z7NnrcT/image-2024-02-05-130541704.png)

## Support Server:
Discord: https://discord.gg/WVU5RcnXd3

## How to setup:

1. **Stop** or **delete** current garage system in your server
2. Customize the `config.lua` and change the **framework** to your ==server framework
3. Start the goat-garage script in your server
4. Done ✅

### Config Example:
```lua
Config = {}

Config.Mysql = 'oxmysql' --

Config.Framework = 'QBCore' -- ESX / QBCore

Config.ImpoundPrice = 300

Config.ShowVehicleByGarageName = true             -- true / false

Config.ResetImpoundListAfterRestartServer = false -- true / false

Config.FixVehicleAfterBackFromImpound = true

Config.PayMethod = 'money' -- bank / money

Config.useLegacyFuel = false

Config.GarageCoords = {
    ['A Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(213.613190, -809.696716, 30.998535),
        vehicle = "car", -- boat / aircraft
        garageType = "normal",
        npcHeading = 337.0,
        parking = vector3(215.68, -792.62, 30.13),
        parkoutPoints = { vector3(236.109894, -797.815369, 30.122314), vector3(235.331863, -800.479126, 30.105469), vector3(234.395599, -802.865906, 30.088623), vector3(233.432968, -805.384644, 30.088623) },
        preview = { spawn = vector3(241.529678, -773.248352, 30.358276), heading = 158.0 },
        camera = vector3(242.228577, -780.276917, 30.610962),
        heading = 68.03,
        ['UI'] = { 25, 148, 255 }, -- For ui color
        ["hueRotation"] = "0deg"   -- for image color rotation

    },
    ['Police Garage'] = {
        allowedJob = "police",
        npc = vector3(459.072540, -1017.138489, 28.150879),
        vehicle = "car", -- boat / aircraft
        garageType = "normal",
        npcHeading = 93.543304,
        parking = vector3(454.470337, -1020.725281, 27.502612),
        parkoutPoints = { vector3(446.637360, -1025.709839, 28.235107), vector3(443.142853, -1025.459351, 28.285767), vector3(439.239563, -1025.169189, 28.336304), vector3(435.454956, -1025.050537, 28.386841) },
        preview = { spawn = vector3(415.490112, -1013.868103, 28.841797), heading = 223.937012 },
        camera = vector3(416.993408, -1020.870300, 29.077637),
        heading = 354.330719,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
    ['B Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(100.101105, -1072.892334, 29.364136),
        vehicle = "car", -- boat / aircraft
        garageType = "normal",
        npcHeading = 257.9,
        parking = vector3(131.670334, -1059.402222, 28.378711),
        parkoutPoints = { vector3(121.371429, -1082.057129, 28.841797), vector3(125.024178, -1081.951660, 28.841797), vector3(128.558243, -1081.859375, 28.841797), vector3(132.290115, -1081.951660, 28.841797) },
        preview = { spawn = vector3(148.129669, -1070.004507, 29.178711), heading = 159.9 },
        camera = vector3(149.076935, -1076.492310, 29.178711),
        heading = 00.00,
        ['UI'] = { 50, 168, 82 },  -- For ui color
        ["hueRotation"] = "250deg" -- for image color rotation
    },
    ['C Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(1736.861572, 3709.622070, 34.115723),
        vehicle = "car",       -- boat / aircraft
        garageType = "normal", -- normal / impound
        npcHeading = 31.0,
        parking = vector3(1736.980225, 3720.342773, 33.214648),
        parkoutPoints = { vector3(1721.221924, 3714.118652, 33.846191), vector3(1723.437378, 3715.397705, 33.829346), vector3(1726.021973, 3716.518799, 33.795654), vector3(1728.567017, 3717.652832, 33.761963) },
        preview = { spawn = vector3(1734.329712, 3727.839502, 33.947266), heading = 164.4 },
        camera = vector3(1735.767090, 3721.331787, 34.014648),
        heading = 19.00,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
    ['D Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(-904.364807, -2338.628662, 6.701050),
        vehicle = "car",       -- boat / aircraft
        garageType = "normal", -- normal / impound
        npcHeading = 323.0,
        parking = vector3(-891.929688, -2318.426270, 5.801050),
        parkoutPoints = { vector3(-897.323059, -2338.232910, 6.347290), vector3(-895.727478, -2335.265869, 6.347290), vector3(-893.934082, -2332.193359, 6.347290), vector3(-892.246155, -2329.318604, 6.347290) },
        preview = { spawn = vector3(-889.595581, -2306.690186, 6.701050), heading = 190.0 },
        camera = vector3(-888.474731, -2313.718750, 6.701050),
        heading = 59.15,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
    ['E Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(-1478.136230, -519.323059, 34.722290),
        vehicle = "car",       -- boat / aircraft
        garageType = "normal", -- normal / impound
        npcHeading = 28.3,
        parking = vector3(-1474.668091, -501.441742, 31.901514),
        parkoutPoints = { vector3(-1495.767090, -506.505493, 32.447632), vector3(-1492.997803, -504.804382, 32.447632), vector3(-1490.360474, -503.037354, 32.447632), vector3(-1487.709839, -501.336273, 32.447632) },
        preview = { spawn = vector3(-1498.021973, -521.063721, 32.801514), heading = 158.74 },
        camera = vector3(-1498.127441, -528.145081, 32.801514),
        heading = 215.43,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
    ['F Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(-1709.815430, 74.756042, 65.860840),
        vehicle = "car",       -- boat / aircraft
        garageType = "normal", -- normal / impound
        npcHeading = 221.102371,
        parking = vector3(-1710.276978, 67.199997, 65.161914),
        parkoutPoints = { vector3(-1713.098877, 57.085716, 65.961914), vector3(-1710.514282, 54.580219, 65.793457), vector3(-1707.995605, 52.048355, 65.608032), vector3(-1705.384644, 49.490112, 65.389038) },
        preview = { spawn = vector3(-1680.501099, 42.751652, 63.316528), heading = 158.74 },
        camera = vector3(-1679.314331, 35.142860, 63.518677),
        heading = 291.968506,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
    ['G Garage'] = {
        allowedJob = nil,
        jobDefaultCars = {},
        jobLimited = false,
        npc = vector3(-72.883514, -2003.564819, 18.260132),
        vehicle = "car",       -- boat / aircraft
        garageType = "normal", -- normal / impound
        npcHeading = 170.078735,
        parking = vector3(-88.602196, -2018.571411, 17.207324),
        parkoutPoints = { vector3(-50.268131, -2020.892334, 17.653442), vector3(-53.617584, -2021.934082, 17.653442), vector3(-57.204391, -2023.160400, 17.653442), vector3(-60.738457, -2024.479126, 17.653442) },
        preview = { spawn = vector3(-83.841759, -1992.356079, 18.007324), heading = 198.74 },
        camera = vector3(-82.272522, -1998.065918, 18.007324),
        heading = 17.0,
        ['UI'] = { 69, 3, 252 }, -- For ui color
        ["hueRotation"] = "0deg" -- for image color rotation
    },
}

Config.Locales = {
    ['pressE'] = "<FONT FACE='GoogoGaga'>Press [E]",
    ['Egarage'] = "<FONT FACE='GoogoGaga'>[E] GARAGE",
    ['not_owner'] = "You are not the owner of this vehicle",
    ['not_found_car'] = "There is no car in your garage",
    ['not_enough_money'] = "Not enough Money",
    ['veh_block'] = "Vehicle Spawn point is Blocked!",
}

Config.UI = {
    ['mainColor'] = { 69, 3, 252 }, --You Can Set UI Theme With Change This Value
    ['speed'] = "SPEED",
    ['impound'] = "Impound",
    ['all_cars'] = "All Cars",
    ['impound_prompt'] = "This car is impound do you want to restore it for",
    ['restore'] = "RESTORE",
    ['select'] = "SELECT",
    ['restorePriceSymbol'] = "$",
}

Config.blip = {
    ['normal'] = {
        name = "Garage",
        blip = 357,
        color = 26,
        scale = 0.7
    },
    ['impound'] = {
        name = "Impound",
        blip = 524,
        color = 1,
        scale = 0.7
    },
}

function GetFrameworkObject()
    local object = nil
    if Config.Framework == "ESX" then
        object = exports["es_extended"]:getSharedObject()
    end
    if Config.Framework == "QBCore" then
        object = exports['qb-core']:GetCoreObject()
    end
    return object
end

Config.NotFoundBrand = "UNKNOWN"

Config.VehicleBrands = {
    ["blade"] = "Vapid",
    ["buccaneer"] = "Albany",
    ["buccaneer2"] = "Albany",
    ["chino"] = "Vapid",
    ["chino2"] = "Vapid",
    ["coquette3"] = "Invetero",
    ["dominator"] = "Vapid",
    ["dukes"] = "Imponte",
    ["gauntlet"] = "Bravado",
    ["hotknife"] = "Vapid",
    ["faction"] = "Willard",
    ["faction2"] = "Willard",
    ["faction3"] = "Willard",
    ["nightshade"] = "Imponte",
    ["phoenix"] = "Imponte",
    ["picador"] = "Cheval",
    ["sabregt"] = "Declasse",
    ["sabregt2"] = "Declasse",
    ["slamvan3"] = "Vapid",
    ["tampa"] = "Declasse",
    ["virgo"] = "Albany",
    ["vigero"] = "Declasse",
    ["voodoo"] = "Declasse",
    ["330661258"] = "Dinka",
    ["brioso"] = "Grotti",
    ["issi2"] = "Weeny",
    ["blista"] = "Dinka",
    ["panto"] = "Benefactor",
    ["prairie"] = "Bollokan",
    ["bison"] = "Declasse",
    ["bobcatxl"] = "Vapid",
    ["burrito3"] = "Declasse",
    ["gburrito2"] = "Declasse",
    ["gburrito"] = "Declasse",
    ["camper"] = "Brute",
    ["journey"] = "Zirconium",
    ["minivan"] = "Vapid",
    ["moonbeam"] = "Declasse",
    ["moonbeam2"] = "Declasse",
    ["paradise"] = "Bravado",
    ["rumpo"] = "Bravado",
    ["rumpo3"] = "Bravado",
    ["surfer"] = "BF",
    ["youga"] = "Bravado",
    ["youga2"] = "Bravado",
    ["asea"] = "Declasse",
    ["cognoscenti"] = "Enus",
    ["emperor"] = "Cheval",
    ["glendale"] = "Benefactor",
    ["intruder"] = "Karin",
    ["premier"] = "Declasse",
    ["primo2"] = "Albany",
    ["regina"] = "Dundreary",
    ["cogcabri"] = "Enus",
    ["schafter2"] = "Benefactor",
    ["stretch"] = "Dundreary",
    ["superd"] = "Enus",
    ["tailgater"] = "Obey",
    ["warrener"] = "Vulcar",
    ["washington"] = "Albany",
    ["baller2"] = "Gallivanter",
    ["baller3"] = "Gallivanter",
    ["cavalcade2"] = "Albany",
    ["contender"] = "Vapid",
    ["dubsta"] = "Benefactor",
    ["dubsta2"] = "Benefactor",
    ["fq2"] = "Fathom",
    ["granger"] = "Declasse",
    ["gresley"] = "Bravado",
    ["huntley"] = "Enus",
    ["landstalker"] = "Dundreary",
    ["mesa"] = "Canis",
    ["mesa3"] = "Canis",
    ["patriot"] = "Mammoth",
    ["radi"] = "Vapid",
    ["rocoto"] = "Obey",
    ["seminole"] = "Canis",
    ["xls"] = "Benefactor",
    ["btype"] = "Albany",
    ["btype3"] = "Albany",
    ["btype2"] = "Albany",
    ["casco"] = "Lampadati",
    ["coquette2"] = "Invetero",
    ["manana"] = "Albany",
    ["monroe"] = "Pegassi",
    ["pigalle"] = "Lampadati",
    ["stinger"] = "Grotti",
    ["stingergt"] = "Grotti",
    ["feltzer3"] = "Benefactor",
    ["ztype"] = "Truffade",
    ["bifta"] = "BF",
    ["bfinjection"] = "BF",
    ["blazer"] = "Nagasaki",
    ["blazer4"] = "Nagasaki",
    ["brawler"] = "Coil",
    ["dubsta3"] = "Benefactor",
    ["dune"] = "MTL",
    ["guardian"] = "Vapid",
    ["rebel2"] = "Karin",
    ["sandking"] = "Vapid",
    ["monster"] = "Vapid",
    ["trophytruck"] = "Vapid",
    ["trophytruck2"] = "Vapid",
    ["cogcabrio"] = "Enus",
    ["exemplar"] = "Dewbauchee",
    ["f620"] = "Ocelot",
    ["felon"] = "Lampadati",
    ["felon2"] = "Lampadati",
    ["jackal"] = "Ocelot",
    ["oracle2"] = "Übermacht",
    ["sentinel"] = "Übermacht",
    ["sentinel2"] = "Übermacht",
    ["windsor"] = "Lampadati",
    ["windsor"] = "Enus",
    ["windsor2"] = "Enus",
    ["zion"] = "Übermacht",
    ["zion2"] = "Übermacht",
    ["ninef"] = "Obey",
    ["ninef2"] = "Obey",
    ["alpha"] = "Albany",
    ["banshee"] = "Bravado",
    ["bestiagts"] = "Grotti",
    ["buffalo"] = "Bravado",
    ["buffalo2"] = "Bravado",
    ["carbonizzare"] = "Grotti",
    ["comet2"] = "Pfister",
    ["coquette"] = "Invetero",
    ["tampa2"] = "Declasse",
    ["elegy2"] = "Annis",
    ["feltzer2"] = "Benefactor",
    ["furoregt"] = "Lampadati",
    ["fusilade"] = "Schyster",
    ["jester"] = "Dinka",
    ["jester2"] = "Dinka",
    ["khamelion"] = "Hijak",
    ["kuruma"] = "Karin",
    ["lynx"] = "Ocelot",
    ["mamba"] = "Declasse",
    ["massacro"] = "Dewbauchee",
    ["massacro2"] = "Dewbauchee",
    ["omnis"] = "Obey",
    ["penumbra"] = "Maibatsu",
    ["rapidgt"] = "Dewbauchee",
    ["rapidgt2"] = "Dewbauchee",
    ["schafter3"] = "Benefactor",
    ["seven70"] = "Dewbauchee",
    ["sultan"] = " Karin",
    ["surano"] = "Benefactor",
    ["tropos"] = "Lampadati",
    ["verlierer2"] = "Bravado",
    ["adder"] = "Truffade",
    ["banshee2"] = "Bravado",
    ["bullet"] = "Vapid",
    ["cheetah"] = "Grotti",
    ["entityxf"] = "Överflöd",
    ["sheava"] = "Emperor",
    ["fmj"] = "Vapid",
    ["infernus"] = "Pegassi",
    ["osiris"] = "Pegassi",
    ["pfister811"] = "Pfister",
    ["le7b"] = "Annis",
    ["reaper"] = "Pegassi",
    ["sultanrs"] = "Karin",
    ["t20"] = "Progen",
    ["turismor"] = "Grotti",
    ["tyrus"] = "Progen",
    ["vacca"] = "Pegassi",
    ["voltic"] = "Coil",
    ["prototipo"] = "Grotti",
    ["zentorno"] = "Pegassi",
    ["AKUMA"] = "Dewbauchee",
    ["avarus"] = "Liberty City Cycles",
    ["bagger"] = "Western Motorcycle Company",
    ["bati"] = "Pegassi",
    ["bati2"] = "Pegassi",
    ["bf400"] = "Nagasaki",
}
```

