# Berechtigungen & Administration

## Access mode

Für Server, die FraseKill verkaufen, ist `managed` empfohlen: Admin-Panel, manueller Zugriff, ACE, Jobs/Gruppen und Tebex arbeiten zusammen.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Für den ersten Admin ACE verwenden. Ohne Rechte zeigt `/frasekilladmin` die exakte Zeile für `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, native QB/Qbox-Gangs und ein Custom Resolver können gleichzeitig aktiv sein. Namespaces verhindern Namenskollisionen.

```text
job:police
guille:ballas
frameworkgang:vagos
custom:vip
```

Minimum grade:

```text
job:police@2
```

## Admin panel

`/frasekilladmin` allows you to:

- Grant or revoke player access.
- Grant access by job/group and minimum grade.
- Create permanent or timed access.
- Search players and existing FraseKills.
- Edit/reset/delete a player's configuration.
- Leave internal admin notes.
- Send an admin message to an online player.
- See the access source and remaining time.

## Diagnostics

```text
/frasekillstatus
```

Shows database, framework, medical adapter and group integration status to administrators.
