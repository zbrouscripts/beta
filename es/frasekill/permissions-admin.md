# Permisos y administración

## Access mode

El modo recomendado para servidores que venden FraseKill es `managed`: combina panel admin, accesos manuales, ACE, jobs/grupos y Tebex.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Para crear el primer admin usa ACE. Si ejecutas `/frasekilladmin` sin permiso, el propio recurso muestra la línea exacta que debes copiar.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Puedes activar simultáneamente Jobs, GuilleGangs V2, gangs nativas de QB/Qbox y un resolver custom. Internamente se usan namespaces para que dos grupos con el mismo nombre no se mezclen.

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
