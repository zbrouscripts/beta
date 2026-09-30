# Instalación

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Requisitos

Dependencia obligatoria: **oxmysql**. ESX, QBCore, Qbox y los recursos médicos son opcionales. `zbrou_utils` no es una dependencia.

## Steps

1. Copia `zbrou_frasekill` dentro de tu carpeta de resources.
2. Asegúrate de iniciar `oxmysql` antes de FraseKill.
3. Revisa `config.lua`, `config_server.lua` y `server/webhooks.lua`.
4. Inicia el recurso. Las tablas se crean y migran automáticamente cuando `Config.Storage.AutoCreate = true`.

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
