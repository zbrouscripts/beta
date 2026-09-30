# Bağımlılıklar

### Gerekli

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Frameworkler

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

Otomatik algılama varsayılan olarak açıktır.

Yol:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

`auto` ile `zbrou_chat` mevcut frameworkü otomatik olarak algılar.
