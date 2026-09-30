# Installation

### 1. Copy the resources

Place `zbrou_utils` and `zbrou_chat` inside your server resources folder.

### 2. Remove the previous chat

To avoid two chat interfaces at the same time:

* remove or disable `esx_rpchat`;
* remove or disable `esx_chat_theme`;
* remove or comment `ensure chat` in `server.cfg`.

### 3. Add your Rockstar license

Open `zbrou_chat/config.lua`. There are two different access levels:

**Owner — configuration + moderation**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — configuration only**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

The appropriate access lets you configure the chat in-game with `/zbrou`. Use `Owners` if you also need moderation tools.

### 4. Discord avatars — optional

Open:

```
zbrou_utils/server/private.lua
```

Paste only the token:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
The bot **does not need permissions, commands, or to be inside any Discord server**. You only need a valid bot token.
{% endhint %}

### 5. Recommended `server.cfg` order

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

If you use `ghmattimysql`, you can start it instead of `oxmysql`. You do not need to import SQL manually: required tables are created automatically when a compatible driver is available.

### 6. Start and configure

Restart the server, join the game and run:

```
/zbrou
```

Then open **CHAT → Configuration**.
