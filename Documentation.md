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

DISCLAIMER: HubRz's "tools" are made for educational purposes and with no intent in harming roblox servers (Physical), And any harm done using this "tool" will not be our responsibility for the action of the user whom uses this "tool", Any claims of Malicious code from this tool is false even though it's obfuscated, If you do wish to use this "tool" in anyway e.g: Using it in your script and anyone using the script, Is responsible for any conciquences caused by this tool, and by using the "tool" you hearby acknowlage that you are responsible for the conciquences caused by this tool, This tool can be used for your liking andor intention.
