# Permissions et administration

## Access mode

Pour les serveurs qui vendent l’accès à FraseKill, `managed` est recommandé : panel admin, accès manuel, ACE, jobs/groupes et Tebex fonctionnent ensemble.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Utilisez ACE pour le premier admin. Sans permission, `/frasekilladmin` affiche la ligne exacte à copier dans `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, gangs natives QB/Qbox et resolver custom peuvent être activés ensemble. Les namespaces internes évitent les collisions.

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
