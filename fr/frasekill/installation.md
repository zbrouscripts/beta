# Installation

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Prérequis

Dépendance obligatoire : **oxmysql**. ESX, QBCore, Qbox et les ressources médicales sont optionnels. `zbrou_utils` n’est pas requis.

## Steps

1. Copiez `zbrou_frasekill` dans votre dossier resources.
2. Démarrez `oxmysql` avant FraseKill.
3. Vérifiez `config.lua`, `config_server.lua` et `server/webhooks.lua`.
4. Démarrez la ressource. Les tables sont créées/migrées automatiquement avec `Config.Storage.AutoCreate = true`.

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
