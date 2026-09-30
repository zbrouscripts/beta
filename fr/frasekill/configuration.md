# Configuration

## `config.lua`

Configuration partagée et visuelle. Ne placez aucun secret ici.

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

`death_state` est recommandé : FraseKill reste visible jusqu’au revive, avec failsafe de sécurité.

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

Configuration privée serveur : permissions, groupes, Tebex, modération et stockage.

```lua
Config.Storage.Identifier = 'license' -- license | character | custom
Config.Access.Mode = 'managed'       -- everyone | managed | ace | custom
```

## `server/webhooks.lua`

Webhooks Discord. Utilisez ce fichier pour les URLs.
