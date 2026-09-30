# Installazione

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Requisiti

Dipendenza obbligatoria: **oxmysql**. ESX, QBCore, Qbox e risorse medical sono opzionali. `zbrou_utils` non è una dipendenza.

## Steps

1. Copia `zbrou_frasekill` nella cartella resources.
2. Avvia `oxmysql` prima di FraseKill.
3. Controlla `config.lua`, `config_server.lua` e `server/webhooks.lua`.
4. Avvia la risorsa. Le tabelle vengono create/migrate automaticamente con `Config.Storage.AutoCreate = true`.

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
