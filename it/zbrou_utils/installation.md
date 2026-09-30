# Installazione

### 1. Copia la risorsa

Inserisci `zbrou_utils` nella cartella resources del server.

### 2. Aggiungila al `server.cfg`

`zbrou_utils` deve essere avviato prima di qualsiasi altra risorsa zbrou che dipende da esso.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Se usi già `ghmattimysql`, puoi usarlo al posto di `oxmysql`. Le tabelle necessarie vengono create automaticamente; normalmente non serve importare SQL manualmente.

### 3. Avatar Discord — opzionale

Apri `zbrou_utils/server/private.lua`:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Il bot **non ha bisogno di permessi, comandi né di essere presente in alcun server Discord**. Serve solo un token bot valido.
{% endhint %}

### 4. Avvia il server

Riavvia il server. Tutte le risorse zbrou che usano `zbrou_utils` devono essere avviate dopo di esso.
