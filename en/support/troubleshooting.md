# Troubleshooting

**The menu does not appear**\
Make sure `zbrou_utils` starts before `zbrou_chat`.

**You cannot open Configuration**\
Open:

```
zbrou_chat/config.lua
```

For Owner access:

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

For configuration-only access:

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Discord avatars do not appear**\
Open:

```
zbrou_utils/server/private.lua
```

Check that a valid token is set:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

Then check avatars from:

```
/zbrou → CHAT → Configuration
```

**Two chats appear**\
Make sure `server.cfg` no longer starts the stock chat:

```cfg
# ensure chat
```

Also remove or disable `esx_rpchat` and `esx_chat_theme`.

### Discord

If you still need help, join our Discord.

