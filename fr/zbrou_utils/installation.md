# Installation

### 1. Copiez la ressource

Placez `zbrou_utils` dans le dossier resources de votre serveur.

### 2. Ajoutez-la au `server.cfg`

`zbrou_utils` doit démarrer avant toute autre ressource zbrou qui en dépend.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Si vous utilisez déjà `ghmattimysql`, vous pouvez l'utiliser à la place de `oxmysql`. Les tables nécessaires sont créées automatiquement ; aucun import SQL manuel n'est normalement nécessaire.

### 3. Avatars Discord — optionnel

Ouvrez `zbrou_utils/server/private.lua` :

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Le bot **n'a besoin d'aucune permission, d'aucune commande et n'a pas besoin d'être présent sur un serveur Discord**. Il suffit d'un token de bot valide.
{% endhint %}

### 4. Démarrez le serveur

Redémarrez le serveur. Toutes les ressources zbrou utilisant `zbrou_utils` doivent démarrer après lui.
