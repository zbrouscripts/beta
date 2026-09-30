# Instalação

**Route:** `resources/[zbrou]/zbrou_frasekill/`

## Requisitos

Dependência obrigatória: **oxmysql**. ESX, QBCore, Qbox e recursos médicos são opcionais. `zbrou_utils` não é uma dependência.

## Steps

1. Copie `zbrou_frasekill` para a pasta de resources.
2. Inicie `oxmysql` antes do FraseKill.
3. Revise `config.lua`, `config_server.lua` e `server/webhooks.lua`.
4. Inicie o recurso. As tabelas são criadas/migradas automaticamente com `Config.Storage.AutoCreate = true`.

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
