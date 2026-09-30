# Kurulum

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Gereksinimler

Zorunlu bağımlılık: **oxmysql**. ESX, QBCore, Qbox ve medical kaynakları isteğe bağlıdır. `zbrou_utils` bağımlılık değildir.

## Steps

1. `zbrou_frasekill` klasörünü resources içine kopyalayın.
2. FraseKill’den önce `oxmysql` başlatın.
3. `config.lua`, `config_server.lua` ve `server/webhooks.lua` dosyalarını kontrol edin.
4. Kaynağı başlatın. `Config.Storage.AutoCreate = true` iken tablolar otomatik oluşturulur/migre edilir.

```cfg
ensure oxmysql
ensure zbrou_frasekill
```

## Database

```lua
Config.Storage.AutoCreate = true
```

With this option enabled, the resource creates and migrates its tables automatically. `sql/install.sql` is available for manual installation.

## First administrator

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

If you run `/frasekilladmin` without permission, FraseKill shows the exact ACE line for your current license.
