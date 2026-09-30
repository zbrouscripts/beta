# Risoluzione problemi

**Il menu non appare**\
`zbrou_utils` must start before `zbrou_chat`.

**Non riesci ad aprire Configurazione**\
Percorso:

```
zbrou_chat/config.lua
```

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Gli avatar Discord non appaiono**\
Percorso:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

**Appaiono due chat**

```cfg
# ensure chat
```

Remove or disable `esx_rpchat` and `esx_chat_theme`.

### Discord

Se hai ancora bisogno di aiuto, entra nel nostro Discord.

