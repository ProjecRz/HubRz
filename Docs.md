# On This Page
- [On This Page](https://github.com/ProjecRz/HubRz/blob/main/Docs.md#on-this-page)
- [Usage](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#usage)
  - [KeySystem](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#createkey)
    - [CreateKey](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#createkey)
    - [VerifyKey](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#verifykey)
  - [FPS Booster](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#fps-booster)
  - [DoS (Server Crasher)](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#dos-server-crasher)
    - [Server Crashing Methods](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#server-crashing-methods)
  - [Obfuscator](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#obfuscator)
    - [Obfuscation Methods](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#obfuscation-methods)
  - [Espionage](https://github.com/ProjecRz/HubRz/blob/v1/Docs.md#nil)

# Usage
To use this you must have a text editor e.g: Notepad, Sublime Text, Notepad++ etc.. and to execute the script using an exploit api, Like Synapse X, ScriptWare, Krnl etc..

# KeySystem
The KeySystem can be custom made but it only supports 2 Linkshortener Services that can be used for the User/Developer/Scripter (You) and ProjectRz to profit on, The 50% or in which half of the revenue per user will go to your Adfoc.us / ClicksFly Account Balance, Do note that the first half of the keysystem is ours and the second half is yours, It's recommended to show your audience how to get the key from the keysystem, due to the complexity of both services, particularly **adfoc.us**.

## CreateKey
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

## VerifyKey
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

```lua
HubRz:Dos("Chat")
```

You can also use an *``array/table``* to attack using multiple methods.

```lua
local methods = {
  "Chat", 
  "Table", 
  "Teleport", 
  "Remote"
  }
HubRz:Dos(methods)
```

Alternatively / Fast way:

```lua
HubRz:Dos({"Chat", "Table", "Teleport", "Remote"})
```

### Server Crashing Methods:
- Chat
- Table
- Teleport
- Remote

# Obfuscator
Obfuscator requires you to use an *``array/table``* to obfuscate and/or to use multiple methods.

```lua
local Obfuscated = HubRz:Obfuscator({
  Code = "print(\"Hello World!\")",
  Methods = "Fast"
})
print(Obfuscated)
```

If your code is longer:

```lua
local code = ("
  print(\"Hello World!\")
  for n in 10 do
    print(n)
  end
   print(\"Done!\")
")

local Obfuscated = HubRz:Obfuscator({
  Code = code,
  Methods = "Fast"
})
print(Obfuscated)
```

If your using multiple methods, Make sure that every **``argument``** in Methods have an **``,``** at the end, Also note that depending on how you arrange the arguments, It will use the obfuscate method from the top to bottom of the arguments, It's recommend to use things like **``Garbage``** or **``Blocker``** on the top arguments, Before the code obfuscation methods are initialized.

```lua
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
    "Garbage",
    "Blocker",
    "Fast",
    "Normal",
    "Hard"
    }
})
print(Obfuscated)
```

### Obfuscation Methods:
- Code Obfuscation Methods
  - Fast
  - Normal
  - Hard
  - Expert
- Obscuration Methods
  - Garbage
  - Blocker 

DISCLAIMER: HubRz's "tools" are made for educational purposes and with no intent in harming roblox servers (Physical), And any harm done using this "tool" will not be our responsibility for the action of the user whom uses this "tool", Any claims of Malicious code from this tool is false even though it's obfuscated, If you do wish to use this "tool" in anyway e.g: Using it in your script and anyone using the script, Is responsible for any conciquences caused by this tool, and by using the "tool" you hearby acknowlage that you are responsible for the conciquences caused by this tool, This tool can be used for your liking andor intention.
