# Permissões e administração

## Access mode

Para servidores que vendem acesso ao FraseKill, `managed` é o modo recomendado: painel admin, acesso manual, ACE, jobs/grupos e Tebex trabalham juntos.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

Use ACE para o primeiro admin. Se `/frasekilladmin` for usado sem permissão, o recurso mostra a linha exata para copiar no `server.cfg`.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, gangs nativas QB/Qbox e um resolver custom podem ficar ativos ao mesmo tempo. Namespaces internos evitam colisões.

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
