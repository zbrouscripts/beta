# Installation

### 1. Copy the resource

Place `zbrou_utils` inside your server resources folder.

### 2. Add it to `server.cfg`

`zbrou_utils` must start before any other zbrou resource that depends on it.

```cfg
ensure oxmysql
ensure zbrou_utils
```

If you already use `ghmattimysql`, you can use it instead of `oxmysql`. Required tables are created automatically, so manual SQL import is not needed in a normal installation.

### 3. Discord avatars — optional

Open:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
The bot **does not need permissions, commands, or to be inside any Discord server**. You only need a valid bot token.
{% endhint %}

### 4. Start the server

Restart the server. Every zbrou resource that uses `zbrou_utils` must start after it.
