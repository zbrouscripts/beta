# Abhängigkeiten

### Erforderlich

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Frameworks

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

Die automatische Erkennung ist standardmäßig aktiviert.

Pfad:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

Mit `auto` erkennt `zbrou_chat` das verfügbare Framework automatisch.
