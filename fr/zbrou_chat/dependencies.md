# Dépendances

### Requis

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Frameworks

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

La détection automatique est activée par défaut.

Chemin:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

Avec `auto`, `zbrou_chat` détecte automatiquement le framework disponible.
