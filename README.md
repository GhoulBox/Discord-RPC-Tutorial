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
            DiscordRpc.Initialize("844742911017877544", ref this.handlers, true, null);
            this.handlers = default(DiscordRpc.EventHandlers);
            DiscordRpc.Initialize("844742911017877544", ref this.handlers, true, null);
            this.presence.details = "Your Text Here";
            this.presence.state = "Your Subtext Here";
            this.presence.largeImageKey = "asdf";
            this.presence.smallImageKey = "ghoul";
            this.presence.largeImageText = "";
            this.presence.smallImageText = "By GhoulBox#0001";
            DiscordRpc.UpdatePresence(ref this.presence);
```
