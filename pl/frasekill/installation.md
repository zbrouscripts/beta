# Instalacja

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Wymagania

Wymagana zależność: **oxmysql**. ESX, QBCore, Qbox i zasoby medical są opcjonalne. `zbrou_utils` nie jest zależnością.

## Steps

1. Skopiuj `zbrou_frasekill` do folderu resources.
2. Uruchom `oxmysql` przed FraseKill.
3. Sprawdź `config.lua`, `config_server.lua` i `server/webhooks.lua`.
4. Uruchom zasób. Tabele są automatycznie tworzone/migrowane przy `Config.Storage.AutoCreate = true`.

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
