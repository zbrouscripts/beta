# Installation

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Requirements

Required dependency: **oxmysql**. ESX, QBCore, Qbox and medical resources are optional. `zbrou_utils` is not a dependency.

## Steps

1. Copy `zbrou_frasekill` into your resources folder.
2. Start `oxmysql` before FraseKill.
3. Review `config.lua`, `config_server.lua` and `server/webhooks.lua`.
4. Start the resource. Tables are created/migrated automatically when `Config.Storage.AutoCreate = true`.

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
