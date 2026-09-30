# Dependencias

### Necesario

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` debe estar iniciado antes de `zbrou_chat`.

### Frameworks

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

La detección automática viene activada por defecto. Puedes comprobarlo en:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

Con `auto`, `zbrou_chat` detecta automáticamente el framework disponible.
