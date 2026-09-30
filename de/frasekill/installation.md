# Installation

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Voraussetzungen

Pflichtabhängigkeit: **oxmysql**. ESX, QBCore, Qbox und Medical-Ressourcen sind optional. `zbrou_utils` ist keine Abhängigkeit.

## Steps

1. Kopiere `zbrou_frasekill` in deinen resources-Ordner.
2. Starte `oxmysql` vor FraseKill.
3. Prüfe `config.lua`, `config_server.lua` und `server/webhooks.lua`.
4. Starte die Ressource. Tabellen werden mit `Config.Storage.AutoCreate = true` automatisch erstellt/migriert.

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
