# Sorun Giderme

**Menü görünmüyor**\
`zbrou_utils` must start before `zbrou_chat`.

**Yapılandırma açılamıyor**\
Yol:

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

**Discord avatarları görünmüyor**\
Yol:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

**İki sohbet görünüyor**

```cfg
# ensure chat
```

Remove or disable `esx_rpchat` and `esx_chat_theme`.

### Discord

Yardıma ihtiyacınız devam ederse Discord sunucumuza katılın.

