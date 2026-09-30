# Dépannage

**Le menu ne s’affiche pas**\
`zbrou_utils` must start before `zbrou_chat`.

**Impossible d’ouvrir Configuration**\
Chemin:

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

**Les avatars Discord ne s’affichent pas**\
Chemin:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

**Deux chats apparaissent**

```cfg
# ensure chat
```

Remove or disable `esx_rpchat` and `esx_chat_theme`.

### Discord

Si vous avez encore besoin d’aide, rejoignez notre Discord.

