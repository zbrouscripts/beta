# Dipendenze

### Necessario

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Framework

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

Il rilevamento automatico è attivo per impostazione predefinita.

Percorso:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

Con `auto`, `zbrou_chat` rileva automaticamente il framework disponibile.
