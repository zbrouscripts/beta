# Permissions & administration

## Access mode

For servers selling FraseKill access, `managed` is the recommended mode: admin panel, manual access, ACE, jobs/groups and Tebex work together.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Use ACE for the first admin. If `/frasekilladmin` is used without permission, the resource shows the exact line to copy into `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, native QB/Qbox gangs and a custom resolver can be enabled at the same time. Internal namespaces prevent groups with the same name from colliding.

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
