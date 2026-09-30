# Kurulum

### 1. Kaynakları kopyalayın

`zbrou_utils` ve `zbrou_chat` klasörlerini sunucunuzun resources klasörüne yerleştirin.

### 2. Eski chat kaynağını kaldırın

Aynı anda iki chat arayüzünün açılmasını önlemek için:

* `esx_rpchat` kaynağını kaldırın veya devre dışı bırakın;
* `esx_chat_theme` kaynağını kaldırın veya devre dışı bırakın;
* `server.cfg` içindeki `ensure chat` satırını kaldırın veya yorum satırı yapın.

### 3. Rockstar license ekleyin

`zbrou_chat/config.lua` dosyasını açın. İki farklı erişim seviyesi vardır:

**Owner — yapılandırma + moderasyon**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — yalnızca yapılandırma**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

Uygun erişim ile `/zbrou` komutunu kullanarak chat ayarlarını oyun içinden yapabilirsiniz. Moderasyon araçlarına da ihtiyacınız varsa `Owners` kullanın.

### 4. Discord avatarları — isteğe bağlı

`zbrou_utils/server/private.lua` dosyasını açın ve yalnızca tokenı girin:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Botun **herhangi bir izne, komuta veya herhangi bir Discord sunucusunda bulunmaya ihtiyacı yoktur**. Yalnızca geçerli bir bot tokenı gerekir.
{% endhint %}

### 5. Önerilen `server.cfg` sırası

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

`ghmattimysql` kullanıyorsanız `oxmysql` yerine onu başlatabilirsiniz. SQL'i manuel olarak içe aktarmanız gerekmez: uyumlu bir driver olduğunda gerekli tablolar otomatik oluşturulur.

### 6. Başlatın ve yapılandırın

Sunucuyu yeniden başlatın, oyuna girin ve `/zbrou` komutunu çalıştırın. Ardından **CHAT → Yapılandırma** bölümünü açın.
