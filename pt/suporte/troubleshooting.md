# Solução de problemas

**O menu não aparece**\
`zbrou_utils` must start before `zbrou_chat`.

**Você não consegue abrir a Configuração**\
Caminho:

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

**Os avatares do Discord não aparecem**\
Caminho:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

**Aparecem dois chats**

```cfg
# ensure chat
```

Remove or disable `esx_rpchat` and `esx_chat_theme`.

### Discord

Se ainda precisar de ajuda, entre no nosso Discord.

