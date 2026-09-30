# Configuración

La configuración de `zbrou_utils` se mantiene sencilla y centrada en el menú universal.

### Apariencia y menú

Ruta:

```
zbrou_utils/menu_config.lua
```

Aquí puedes ajustar el estilo predeterminado, idioma, branding y apariencia del menú universal.

### Opciones generales

Ruta:

```
zbrou_utils/config.lua
```

Aquí están las opciones generales del recurso.

### Token privado de Discord

Ruta:

```
zbrou_utils/server/private.lua
```

Código:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="warning" %}
No publiques `server/private.lua` ni muestres el token en capturas, repositorios públicos o mensajes de soporte.
{% endhint %}
