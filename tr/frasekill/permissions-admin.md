# İzinler ve yönetim

## Access mode

FraseKill erişimi satan sunucular için `managed` önerilir: admin paneli, manuel erişim, ACE, job/grup ve Tebex birlikte çalışır.

```lua
Config.Access = {
    Mode = 'managed',
    AcePermission = 'zbrou.frasekill.use',
    AllowAdmins = true
}
```

## First admin

İlk admin için ACE kullanın. Yetkisiz `/frasekilladmin` çalıştırılırsa kaynak `server.cfg` için kopyalanacak satırı gösterir.

```cfg
add_ace identifier.license:YOUR_LICENSE zbrou.frasekill.admin allow
```

## Group access

Jobs, GuilleGangs V2, yerel QB/Qbox gangleri ve custom resolver aynı anda aktif olabilir. Namespace sistemi isim çakışmalarını önler.

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
