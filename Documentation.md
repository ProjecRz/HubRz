# On This Page
- KeySystem
  - CreateKey
  - VerifyKey
- FPS Booster
- DoS (Server Crasher)
- Obfuscator
- Espionage 

# CreateKey
CreateKey only supports [adfoc.us](https://adfoc.us/?refid=700817) or [ClicksFly](https://clicksfly.com/ref/104769173789973858228). To get your 'userkey', follow these steps:

1. Go to Tools > Api / Developers Api.

2. Retrieve the key URL excluding the "&url=yourdestinationlink.com&alias=CustomAlias" and any additional parameters after the key.
```lua
local KeyUrl = HubRz:CreateKey({
  Title = "HubRz"
  AsciiLogo = (
    ██╗░░██╗██╗░░░██╗██████╗░██████╗░███████╗
    ██║░░██║██║░░░██║██╔══██╗██╔══██╗╚════██║
    ███████║██║░░░██║██████╦╝██████╔╝░░███╔═╝
    ██╔══██║██║░░░██║██╔══██╗██╔══██╗██╔══╝░░
    ██║░░██║╚██████╔╝██████╦╝██║░░██║███████╗
    ╚═╝░░╚═╝░╚═════╝░╚═════╝░╚═╝░░╚═╝╚══════╝
  )
 UserKey = "http://adfoc.us/api/?key=86242a3ea2003ba5584240a6e2cfe54d"
 PasteUserUrl = "" -- <= Recommend leaving this blank, if you want to.. use your pastebin user key, but be warned it will clutter your pastebin homepage
 CheckpointsExpireDate = "5M" -- <= Usage: [N]ever, [M]inutes, [H]our, [D]ays, [W]eeks, [M]onths, [Y]ears
 AmountOfCheckpoints = "2" -- <= Only use 2 / 4, Because it will split the user revenue, to us and you.
})

print(KeyUrl)
```

# VerifyKey
VerifyKey returns **`1`** for a valid key, **`0`** for an invalid key, You can use the '**HubRz:VerifyKey(KeyInput) > 0**' as a simpler way to check if the key is valid.
```lua
if HubRz:VerifyKey(KeyInput) > 0 then
  print("Key Is Valid")
else
  print("Key Is Invalid")
end
```

# FPS Booster
Documentation in progress . . .

# DoS
DoS (Denial of Service / Server Crasher) feature is used to crash Roblox (Game) Servers.

``lua
HubRz:Dos("Chat")
``

You can also use an *``array/table``* to attack using multiple methods.

``lua
local methods = {"Chat", "Table", "Teleport", "Remote"}
HubRz:Dos(methods)
``

Alternatively / Fast way:

``lua
HubRz:Dos({"Chat", "Table", "Teleport", "Remote"})
``

Methods Server Crashing:
- Chat
- Table
- Teleport
- Remote

# Obfuscator
Obfuscator requires you to use an *``array/table``* to obfuscate and/or to use multiple methods.

``lua
local Obfuscated = HubRz:Obfuscator({
  Code = "print(\"Hello World!\")"
  Methods = "Fast"
})
print(Obfuscated)
``

If your code is longer:

``lua
local code = ("
  print(\"Hello World!\")
  for n in 10 do
    print(n)
  end
   print(\"Done!\")
")

local Obfuscated = HubRz:Obfuscator({
  Code = "print(\"Hello World!\")"
  Methods = "Fast"
})
print(Obfuscated)
``

If your using multiple methods, Make sure that every **``argument``** in Methods have an **``,``** at the end, Also note that depending on how you arrange the arguments, it will use the obfuscate method from the top to bottom of the arguments, it's recommend to use things like **``Garbage``** or **``Blocker``** on the top arguments, before the code obfuscation methods are initialized.

``lua
local code = ("
  print(\"Hello World!\")
  for n in 10 do
    print(n)
  end
   print(\"Done!\")
")

local Obfuscated = HubRz:Obfuscator({
  Code = "print(\"Hello World!\")"
  Methods = {
    "Fast",
    "Normal",
    "Hard"
    }
})
print(Obfuscated)
``

Methods:
- Code Obfuscation Methods
  - Fast
  - Normal
  - Hard
  - Expert
- Obscuration Methods
  - Garbage
  - Blocker 

DISCLAIMER: HubRz's "tools" are made for educational purposes and with no intent in harming roblox servers (Physical), And any harm done using this "tool" will not be our responsibility for the action of the user whom uses this "tool", Any claims of Malicious code from this tool is false even though it's obfuscated, If you do wish to use this "tool" in anyway e.g: Using it in your script and anyone using the script, Is responsible for any conciquences caused by this tool, and by using the "tool" you hearby acknowlage that you are responsible for the conciquences caused by this tool, This tool can be used for your liking andor intention.
