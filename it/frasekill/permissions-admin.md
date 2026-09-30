# Permessi e amministrazione

## Access mode

Per server che vendono l’accesso FraseKill, `managed` è consigliato: pannello admin, accessi manuali, ACE, job/gruppi e Tebex lavorano insieme.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Usa ACE per il primo admin. Se `/frasekilladmin` viene usato senza permesso, la risorsa mostra la riga esatta da copiare in `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, gang native QB/Qbox e resolver custom possono essere attivi insieme. I namespace interni evitano collisioni.

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
