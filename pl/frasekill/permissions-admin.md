# Uprawnienia i administracja

## Access mode

Dla serwerów sprzedających dostęp do FraseKill zalecany jest tryb `managed`: panel admina, dostęp ręczny, ACE, joby/grupy i Tebex działają razem.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Pierwszego admina dodaj przez ACE. Bez uprawnień `/frasekilladmin` pokaże dokładną linię do wklejenia do `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, natywne gangi QB/Qbox i custom resolver mogą działać równocześnie. Namespace zapobiega kolizjom nazw.

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
