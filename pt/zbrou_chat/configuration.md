# Configuração

`zbrou_chat` pode ser configurado diretamente no jogo através do menu `/zbrou`.

```
/zbrou
```

**CHAT → Configuração**

### Configuração

Caminho:

```
zbrou_chat/config.lua
```

**Owner — Configuração + moderação**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — Apenas configuração**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```
