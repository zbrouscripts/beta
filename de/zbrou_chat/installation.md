# Installation

### 1. Ressourcen kopieren

Lege `zbrou_utils` und `zbrou_chat` in den resources-Ordner deines Servers.

### 2. Alten Chat entfernen

Damit nicht zwei Chat-Oberflächen gleichzeitig laufen:

* `esx_rpchat` entfernen oder deaktivieren;
* `esx_chat_theme` entfernen oder deaktivieren;
* `ensure chat` in `server.cfg` entfernen oder auskommentieren.

### 3. Rockstar license hinzufügen

Öffne `zbrou_chat/config.lua`. Es gibt zwei Zugriffsarten:

**Owner — Konfiguration + Moderation**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — nur Konfiguration**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

Mit dem passenden Zugriff kannst du den Chat im Spiel über `/zbrou` konfigurieren. Verwende `Owners`, wenn du zusätzlich Moderationswerkzeuge brauchst.

### 4. Discord-Avatare — optional

Öffne `zbrou_utils/server/private.lua` und füge nur den Token ein:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Der Bot **benötigt keine Berechtigungen, keine Commands und muss auf keinem Discord-Server sein**. Du brauchst nur einen gültigen Bot-Token.
{% endhint %}

### 5. Empfohlene Reihenfolge in `server.cfg`

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

Wenn du `ghmattimysql` verwendest, kannst du es anstelle von `oxmysql` starten. SQL muss nicht manuell importiert werden: die benötigten Tabellen werden mit einem kompatiblen Driver automatisch erstellt.

### 6. Starten und konfigurieren

Starte den Server neu, betrete das Spiel und führe `/zbrou` aus. Öffne danach **CHAT → Konfiguration**.
