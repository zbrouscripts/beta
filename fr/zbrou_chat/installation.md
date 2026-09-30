# Installation

### 1. Copiez les ressources

Placez `zbrou_utils` et `zbrou_chat` dans le dossier resources de votre serveur.

### 2. Supprimez l'ancien chat

Pour éviter deux interfaces de chat en même temps :

* supprimez ou désactivez `esx_rpchat` ;
* supprimez ou désactivez `esx_chat_theme` ;
* supprimez ou commentez `ensure chat` dans `server.cfg`.

### 3. Ajoutez votre Rockstar license

Ouvrez `zbrou_chat/config.lua`. Deux niveaux d'accès existent :

**Owner — configuration + modération**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — configuration uniquement**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

L'accès correspondant permet de configurer le chat en jeu avec `/zbrou`. Utilisez `Owners` si vous avez aussi besoin des outils de modération.

### 4. Avatars Discord — optionnel

Ouvrez `zbrou_utils/server/private.lua` et collez uniquement le token :

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Le bot **n'a besoin d'aucune permission, d'aucune commande et n'a pas besoin d'être présent sur un serveur Discord**. Il suffit d'un token de bot valide.
{% endhint %}

### 5. Ordre recommandé dans `server.cfg`

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

Si vous utilisez `ghmattimysql`, vous pouvez le démarrer à la place de `oxmysql`. Aucun import SQL manuel n'est nécessaire : les tables sont créées automatiquement avec un driver compatible.

### 6. Démarrez et configurez

Redémarrez le serveur, rejoignez le jeu et exécutez `/zbrou`. Ouvrez ensuite **CHAT → Configuration**.
