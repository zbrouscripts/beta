# Instalación

### 1. Copia los recursos

Coloca `zbrou_utils` y `zbrou_chat` dentro de la carpeta de recursos de tu servidor.

### 2. Quita el chat anterior

Para evitar dos chats abiertos al mismo tiempo:

* elimina `esx_rpchat`;
* elimina `esx_chat_theme`;
* abre `server.cfg` y quita o comenta `ensure chat`.

### 3. Añade tu Rockstar license

Abre `zbrou_chat/config.lua`. Hay dos accesos distintos:

**Owner — configuración + moderación**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — solo configuración del chat**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

Con cualquiera de los accesos correspondientes podrás configurar el chat desde el juego con `/zbrou`. Usa `Owners` si además necesitas las herramientas de moderación.

### 4. Avatares de Discord — opcional

Abre:

```
zbrou_utils/server/private.lua
```

Y pega únicamente el token:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
El bot **no necesita permisos, comandos ni estar dentro de ningún servidor de Discord**. Solo necesitas un token de bot válido.
{% endhint %}

### 5. Orden recomendado en `server.cfg`

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

Si utilizas `ghmattimysql`, puedes iniciarlo en lugar de `oxmysql`. No necesitas importar SQL manualmente: las tablas necesarias se crean automáticamente cuando hay un driver compatible.

### 6. Inicia y configura

Reinicia el servidor, entra al juego y ejecuta:

```
/zbrou
```

Después entra en **CHAT → Configuración**.
