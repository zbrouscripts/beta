# Yapılandırma

`zbrou_chat` pode ser configurado diretamente no jogo através do menu `/zbrou`.

```
/zbrou
```

**CHAT → Yapılandırma**

### Yapılandırma

Yol:

```
zbrou_chat/config.lua
```

**Owner — Yapılandırma + moderasyon**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — Yalnızca yapılandırma**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```
