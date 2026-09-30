# Configuration

Most `zbrou_chat` settings are managed directly in-game.

Open:

```
/zbrou
```

Then go to **CHAT → Configuration**.

From there you can enable or disable features, edit messages, colors, distances, avatars, commands, 3D Text, announcements, moderation, default chat appearance, emojis and more.

You can also **create custom chat commands** and define their behavior from the configurator: global or proximity range, distance, colors, 3D Text, job alerts and other available options.

### Configurator access

To allow someone to configure the chat in-game, open:

```
zbrou_chat/config.lua
```

**Owner — configuration + moderation**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — configuration only**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

Use `Owners` for people who also need moderation access. Use `Editors` for people who only need to configure the chat through `/zbrou`.
