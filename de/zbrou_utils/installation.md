# Installation

### 1. Ressource kopieren

Lege `zbrou_utils` in den resources-Ordner deines Servers.

### 2. Zu `server.cfg` hinzufügen

`zbrou_utils` muss vor allen anderen zbrou-Ressourcen gestartet werden, die davon abhängen.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Wenn du bereits `ghmattimysql` verwendest, kannst du es anstelle von `oxmysql` nutzen. Die benötigten Tabellen werden automatisch erstellt; ein manueller SQL-Import ist normalerweise nicht nötig.

### 3. Discord-Avatare — optional

Öffne `zbrou_utils/server/private.lua`:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Der Bot **benötigt keine Berechtigungen, keine Commands und muss auf keinem Discord-Server sein**. Du brauchst nur einen gültigen Bot-Token.
{% endhint %}

### 4. Server starten

Starte den Server neu. Alle zbrou-Ressourcen, die `zbrou_utils` verwenden, müssen danach gestartet werden.
