# Solución de problemas

**El menú no aparece**\
Comprueba que `zbrou_utils` esté iniciado antes de `zbrou_chat`.

**No puedes abrir Configuración**\
Abre:

```
zbrou_chat/config.lua
```

Para acceso de Owner:

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

Para acceso solo de configuración:

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Los avatares de Discord no aparecen**\
Abre:

```
zbrou_utils/server/private.lua
```

Comprueba que exista un token válido:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

Después comprueba los avatares desde:

```
/zbrou → CHAT → Configuración
```

**Aparecen dos chats**\
Comprueba que en `server.cfg` hayas quitado o comentado:

```cfg
# ensure chat
```

Y elimina o desactiva los recursos `esx_rpchat` y `esx_chat_theme`.

### Discord

Si sigues necesitando ayuda, entra en nuestro Discord.

