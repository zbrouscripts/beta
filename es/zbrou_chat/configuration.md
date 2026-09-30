# Configuración

Toda la configuración habitual de `zbrou_chat` se realiza desde el propio juego.

Abre:

```
/zbrou
```

Después entra en **CHAT → Configuración**.

Desde ahí puedes activar o desactivar funciones, cambiar mensajes, colores, distancias, avatares, comandos, Texto3D, anuncios, moderación, el aspecto predeterminado del chat, emojis y mucho más.

También puedes **crear tus propios comandos de chat** y definir sus funciones desde el configurador: alcance global o por proximidad, distancia, colores, Texto3D, alertas por job y otras opciones disponibles.

### Acceso al configurador

Para permitir que una persona configure el chat desde el juego, abre:

```
zbrou_chat/config.lua
```

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

Usa `Owners` para quien también deba tener acceso a moderación. Usa `Editors` para quien solo necesite configurar el chat desde `/zbrou`.

El resto de la configuración habitual se realiza desde el menú del juego.
