# Installazione

### 1. Copia le risorse

Inserisci `zbrou_utils` e `zbrou_chat` nella cartella resources del server.

### 2. Rimuovi la chat precedente

Per evitare due interfacce chat contemporaneamente:

* rimuovi o disattiva `esx_rpchat`;
* rimuovi o disattiva `esx_chat_theme`;
* rimuovi o commenta `ensure chat` nel `server.cfg`.

### 3. Aggiungi la tua Rockstar license

Apri `zbrou_chat/config.lua`. Esistono due livelli di accesso:

**Owner — configurazione + moderazione**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — solo configurazione**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

L'accesso corretto permette di configurare la chat in gioco con `/zbrou`. Usa `Owners` se ti servono anche gli strumenti di moderazione.

### 4. Avatar Discord — opzionale

Apri `zbrou_utils/server/private.lua` e incolla solo il token:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Il bot **non ha bisogno di permessi, comandi né di essere presente in alcun server Discord**. Serve solo un token bot valido.
{% endhint %}

### 5. Ordine consigliato nel `server.cfg`

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

Se usi `ghmattimysql`, puoi avviarlo al posto di `oxmysql`. Non serve importare SQL manualmente: le tabelle necessarie vengono create automaticamente con un driver compatibile.

### 6. Avvia e configura

Riavvia il server, entra in gioco ed esegui `/zbrou`. Poi apri **CHAT → Configurazione**.
