# Dependencies

### Required

* `oxmysql`
* `zbrou_utils`

`zbrou_utils` must start before `zbrou_chat`.

### Frameworks

* ESX / ESX Legacy
* QBCore
* Qbox
* Standalone

Automatic detection is enabled by default. Check:

```
zbrou_chat/config.lua
```

```lua
Config.Framework = 'auto'
```

With `auto`, `zbrou_chat` automatically detects the available framework.
