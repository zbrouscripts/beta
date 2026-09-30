# Instalación

### 1. Copia el recurso

Coloca `zbrou_utils` dentro de la carpeta de recursos de tu servidor.

### 2. Añádelo al `server.cfg`

`zbrou_utils` debe iniciarse antes que cualquier otro recurso zbrou que dependa de él.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Si ya utilizas `ghmattimysql`, puedes usarlo en lugar de `oxmysql`. Las tablas necesarias se crean automáticamente; no tienes que importar SQL manualmente en una instalación normal.

### 3. Avatares de Discord — opcional

Abre:

```
zbrou_utils/server/private.lua
```

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
El bot **no necesita permisos, comandos ni estar dentro de ningún servidor de Discord**. Solo necesitas un token de bot válido.
{% endhint %}

### 4. Inicia el servidor

Reinicia el servidor. Todos los recursos zbrou que utilicen `zbrou_utils` deben iniciarse después de él.
