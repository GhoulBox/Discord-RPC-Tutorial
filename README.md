## C# Discord RPC Tutorial
Start by downloading this file: https://www.mediafire.com/folder/oz5emcbi2uplw/DiscordRpcDemo

Open the C# project you want the RPC on. Right click on the file on solution explorer, and open your projects folder in repos. Drag the DiscordRpcDemo folder you just downloaded inside.

It should look something like this:
![](https://user-images.githubusercontent.com/46585903/124998022-86231500-e000-11eb-8902-3a18ab2a7875.png)

Now, go to visual studio, and go to your form. Use the following namespace listed down below.
```csharp
using DiscordRpcDemo;
```
Then, head over to the Discord Developer Portal. You can go there by clicking [here.](https://discord.com/developers/applications)
After that, double click your form, and paste in the following code on the form load.
```csharp
this.handlers = default(DiscordRpc.EventHandlers);
            DiscordRpc.Initialize("Your Client ID", ref this.handlers, true, null);
            this.handlers = default(DiscordRpc.EventHandlers);
            DiscordRpc.Initialize("Your Client ID", ref this.handlers, true, null);
            this.presence.details = "Your Text Here";
            this.presence.state = "Your Subtext Here";
            this.presence.largeImageKey = "Your Image Name";
            this.presence.smallImageKey = "Your Image Name";
            this.presence.largeImageText = "Your Image Text";
            this.presence.smallImageText = "Discord RPC Tutorial By GhoulBox#1000";
            DiscordRpc.UpdatePresence(ref this.presence);
```
Create a new application. Name it whatever you want. Then on the left, head over to the **Rich Prescence** tab.
Scroll down, click on **Add Image(s)**.
Upload the pictures you want on the RPC, then head over to the **General Information** tab. Copy your Application ID, and paste it into the code where it says **Your Client ID**. After that, for **Your Image Name**, paste in the image names you put for the **Rich Prescence** tab. After that, run the program.

The end results would be something like this:
![image](https://user-images.githubusercontent.com/46585903/125000577-8d005680-e005-11eb-84a3-416ab78c7863.png)

### Tutorial By: GhoulBox#1000
