# Dependências

### Necessário

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Frameworks

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

A detecção automática está ativada por padrão.

Caminho:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

Com `auto`, o `zbrou_chat` detecta automaticamente o framework disponível.
