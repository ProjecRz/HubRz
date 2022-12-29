CreateKey
CreateKey only supports adfoc.us or ClicksFly. To get your 'userkey', follow these steps:

Go to Tools > Api / Developers Api.
Retrieve the key URL excluding the "&url=yourdestinationlink.com&alias=CustomAlias" and any additional parameters after the key.
Copy code
local KeyUrl = HubRz:CreateKey({
  Title = "HubRz",
  AsciiLogo = (
    ██╗░░██╗██╗░░░██╗██████╗░██████╗░███████╗
    ██║░░██║██║░░░██║██╔══██╗██╔══██╗╚════██║
    ███████║██║░░░██║██████╦╝██████╔╝░░███╔═╝
    ██╔══██║██║░░░██║██╔══██╗██╔══██╗██╔══╝░░
    ██║░░██║╚██████╔╝██████╦╝██║░░██║███████╗
    ╚═╝░░╚═╝░╚═════╝░╚═════╝░╚═╝░░╚═╝╚══════╝
  ),
  UserKey = "http://adfoc.us/api/?key=86242a3ea2003ba5584240a6e2cfe54d",
  PasteUserUrl = "", -- Recommended to leave this blank. If you want to use your pastebin user key, be aware that it will clutter your pastebin homepage.
  CheckpointsExpireDate = "5M", -- Options: [N]ever, [M]inutes, [H]our, [D]ays, [W]eeks, [M]onths, [Y]ears
  AmountOfCheckpoints = "2", -- Only use 2 / 4. Using any other value will split the user revenue between you and us.
})

print(KeyUrl)
VerifyKey
VerifyKey returns 1 for a valid key and 0 for an invalid key. You can use HubRz:VerifyKey(KeyInput) > 0 as a simpler way to check if the key is valid.

Copy code
if HubRz:VerifyKey(KeyInput) > 0 then
  print("Key Is Valid")
else
  print("Key Is Invalid")
end
