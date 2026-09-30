# Configuração

## `config.lua`

Configuração compartilhada e visual. Não coloque segredos aqui.

### Character limit

```lua
Config.MaxCharacters = 70
```

### Default slot mode

```lua
Config.DefaultSlotMode = 'fixed' -- fixed | random
```

### Default visual values

```lua
Config.Text.Default = 'Nos vemos en el respawn'
Config.Text.DefaultGlowEnabled = true
Config.Text.DefaultGlowColor = '#0e58d8'
Config.Text.DefaultFont = 'system'
Config.Text.DefaultAnimation = 'soft'
Config.Text.DefaultAnimationSpeed = 1.0
```

### Custom starter presets

```lua
Config.DefaultSlots = {
    [1] = { animation='pop', color='#ffffff' },
    [2] = { text='GG' }
}
```

### Display mode

`death_state` é recomendado: a FraseKill fica visível até o revive, com failsafe de segurança.

```lua
Config.Display = {
    Mode = 'death_state', -- timed | death_state | smart
    Seconds = 10,
    MaxSeconds = 20,
    FailsafeSeconds = 120,
    MinVisibleMs = 850
}
```

### Medical adapter

```lua
Config.Death.Adapter = 'auto'
```

Auto-detection supports `esx_ambulancejob`, `qb-ambulancejob`, `qbx_medical` and standalone.

## `config_server.lua`

Configuração privada do servidor: permissões, grupos, Tebex, moderação e armazenamento.

```lua
Config.Storage.Identifier = 'license' -- license | character | custom
Config.Access.Mode = 'managed'       -- everyone | managed | ace | custom
```

## `server/webhooks.lua`

Webhooks do Discord. Use este arquivo para as URLs.
