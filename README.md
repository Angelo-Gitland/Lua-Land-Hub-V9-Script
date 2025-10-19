-- Lua Land Hub V9 - Dawid's Fluent UI Version with Scrollable Tabs
-- BY: LLH LUA LAND

local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Lua Land Hub V9",
    SubTitle = "BY: LLH LUA LAND",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true,
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl
})

local Tabs = {
    Games = Window:AddTab({ Title = "Script Games", Icon = "gamepad" }),
    Universal = Window:AddTab({ Title = "Universal Scripts", Icon = "globe" }),
    Admin = Window:AddTab({ Title = "Admin Scripts", Icon = "shield" }),
    Hub = Window:AddTab({ Title = "Script Hub", Icon = "code" }),
    Creations = Window:AddTab({ Title = "Creations", Icon = "sparkles" }),
    Scanner = Window:AddTab({ Title = "Backdoor Scanner", Icon = "search" }),
    Credits = Window:AddTab({ Title = "Credits", Icon = "info" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

local Sections = {}
for name, tab in pairs(Tabs) do
    Sections[name] = tab:AddSection("Scroll Area")
end

local function addScript(tabName, title, url)
    Sections[tabName]:AddButton({
        Title = title,
        Callback = function()
            loadstring(game:HttpGet(url, true))()
        end
    })
end

local function addClipboard(tabName, title, link)
    Sections[tabName]:AddButton({
        Title = title,
        Callback = function()
            setclipboard(link)
            Fluent:Notify({ Title = "Lua Land Hub", Content = "Link Copied To Clipboard!", Duration = 3 })
        end
    })
end

addScript("Games", "Murder Vs Sheriff", "https://gist.githubusercontent.com/Angelo-Gitland/2c27216aac9911404f990398aff463a7/raw/180ca414827686d3ab9caae3067ba4f09136f712/Lua%2520Land%2520Hub%2520100+%2520Supported%2520Games")
addScript("Games", "Toilet Tower Defense", "https://raw.githubusercontent.com/LOLking123456/Toilet6/main/Tower5")
addScript("Games", "Arise Crossover", "https://raw.githubusercontent.com/perfectusmim1/script/main/crossover")
addScript("Games", "Trench War", "https://exploitingis.fun/loader")
addScript("Games", "Climb and Jump Tower", "https://raw.githubusercontent.com/gumanba/Scripts/main/ClimbandJump")
addScript("Games", "Bomb to Mine", "https://raw.githubusercontent.com/gumanba/Scripts/main/BombtoMine")

addScript("Universal", "Go0bysworld f3x v2", "https://rawscripts.net/raw/Universal-Script-go0bysworld-f3x-v2-57826")
addScript("Universal", "Zero Executor", "https://pastebin.com/raw/g4QbgAHh")
addScript("Universal", "MOGExecutor", "https://pastebin.com/raw/sEK3Ys1w")
addScript("Universal", "YouTube In Roblox", "https://rawscripts.net/raw/Universal-Script-Youtube-in-Roblox-57836")
addScript("Universal", "PFFF3x Gui", "https://rawscripts.net/raw/Universal-Script-PFFF3XGUI-57834")
addScript("Universal", "Slime Executor", "https://pastebin.com/raw/8DvT8fsy")
addScript("Universal", "da esex Club Private Gui", "https://pastebin.com/raw/VF16ySJn")
addScript("Universal", "CraxyXploitzGui", "https://pastebin.com/raw/UUK42HeB")

addScript("Admin", "Infinite Yield", "https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source")
addScript("Admin", "Kohls Admin", "https://raw.githubusercontent.com/Stefanuk12/ROBLOX/master/Games/Kohls%20Admin%20House/DarkKohls/GUI.lua")
addScript("Admin", "Legs Admin", "https://raw.githubusercontent.com/leg1337/legadmv2/main/legadminv2.lua")
addScript("Admin", "Quirky Cmds [SOME GAMES]", "https://rawscripts.net/raw/Universal-Script-QuirkyCMD-FE-admin-8667")
addScript("Admin", "Brick Admin", "https://raw.githubusercontent.com/MariyaFurmanova/Library/main/un_AdminGUI")

addScript("Hub", "Fe Hub", "https://pastebin.com/raw/gGB65rMr")
addScript("Hub", "LDS Hub", "https://api.luarmor.net/files/v3/loaders/49f02b0d8c1f60207c84ae76e12abc1e.lua")
addScript("Hub", "Eiak's Script Hub V1", "https://pastebin.com/raw/nNbX1meX")
addScript("Hub", "RobHub", "https://pastebin.com/raw/KSvbtcPE")
addScript("Hub", "Lennon Hub", "https://pastefy.app/MJw2J4T6/raw")

addScript("Creations", "Lua Land Executor", "https://raw.githubusercontent.com/Angelo-Gitland/LuaLandHubExecutor/refs/heads/main/Lua%20Land%20Executor")
addScript("Creations", "c00lkidd Executor", "https://gist.githubusercontent.com/Angelo-Gitland/23f5d42e680644f651ff011d604ad1a4/raw/000e0a02cc25c5d23c597beb68944657aca14727/c00lkidd%2520executor")
addScript("Creations", "Fe AntiFling", "https://gist.githubusercontent.com/Angelo-Gitland/894182905a3962a42d9eacd2df673f15/raw/e18b63ec4cd3e86899e800f7cb9fab7638f9aeac/AntiFlingFeByLuaLand")
addScript("Creations", "Backdoor Executor", "https://raw.githubusercontent.com/Angelo-Gitland/LuaLandBackdoorExecutor/refs/heads/main/Lua%20Land%20Executor%20Backdoor")
addScript("Creations", "Billboard Gui", "https://pastebin.com/raw/7FeCFurr")

addScript("Scanner", "Doors Hub Backdoor Scanner", "https://doorhubs.pages.dev/DoorSystem.lua")
addScript("Scanner", "Starlight", "https://starlightrbx.netlify.app/")
addScript("Scanner", "Saturn Backdoor", "https://pastefy.app/8NyW2mEZ/raw")
addScript("Scanner", "Skibidi Hawk", "https://skibidihawkexecutor.fwh.is/scripts%20;D/skibidihawkexecutor-latest")
addScript("Scanner", "Jalon's Backdoor Scanner", "https://raw.githubusercontent.com/jLn0n/scripts/main/backdoor-executor/backdoor-executor.lua")

Sections.Credits:AddParagraph({
    Title = "Credits",
    Content = "Script Made By: LLH Lua Land\nScript Director: Eric_3337\nScript Testers: BaconDaGoofyCreator"
})
addClipboard("Credits", "Join Lua Land Hub", "https://discord.gg/G6Te5p2NeC")
addClipboard("Credits", "Join Eric_3337", "https://discord.gg/TPwmVMXJHN")
addClipboard("Credits", "Join BaconDaGoofyCreator", "https://discord.gg/Q8vUUhgw8A")

SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)
SaveManager:IgnoreThemeSettings()
SaveManager:SetIgnoreIndexes({})
InterfaceManager:SetFolder("LuaLandHub")
SaveManager:SetFolder("LuaLandHub/Configs")
InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)

Window:SelectTab(1)
Fluent:Notify({ Title = "Lua Land Hub", Content = "Script Loaded Successfully!", Duration = 8 })
SaveManager:LoadAutoloadConfig()
