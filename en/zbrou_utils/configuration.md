# Configuration

`zbrou_utils` keeps configuration simple and focused on the universal menu.

### Appearance and menu

Path:

```
zbrou_utils/menu_config.lua
```

Use this file for the default style, language, branding and universal menu appearance.

### General options

Path:

```
zbrou_utils/config.lua
```

This file contains the resource's general options.

### Private Discord token

Path:

```
zbrou_utils/server/private.lua
```

Code:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="warning" %}
Never publish `server/private.lua` or expose the token in screenshots, public repositories or support messages.
{% endhint %}
