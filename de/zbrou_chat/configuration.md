# Konfiguration

`zbrou_chat` pode ser configurado diretamente no jogo através do menu `/zbrou`.

```
/zbrou
```

**CHAT → Konfiguration**

### Konfiguration

Pfad:

```
zbrou_chat/config.lua
```

**Owner — Konfiguration + Moderation**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — Nur Konfiguration**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```
