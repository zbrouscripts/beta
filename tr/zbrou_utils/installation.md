# Kurulum

### 1. Kaynağı kopyalayın

`zbrou_utils` klasörünü sunucunuzun resources klasörüne yerleştirin.

### 2. `server.cfg` dosyasına ekleyin

`zbrou_utils`, ona bağlı diğer tüm zbrou kaynaklarından önce başlatılmalıdır.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Zaten `ghmattimysql` kullanıyorsanız `oxmysql` yerine onu kullanabilirsiniz. Gerekli tablolar otomatik oluşturulur; normal kurulumda manuel SQL içe aktarımı gerekmez.

### 3. Discord avatarları — isteğe bağlı

`zbrou_utils/server/private.lua` dosyasını açın:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
Botun **herhangi bir izne, komuta veya herhangi bir Discord sunucusunda bulunmaya ihtiyacı yoktur**. Yalnızca geçerli bir bot tokenı gerekir.
{% endhint %}

### 4. Sunucuyu başlatın

Sunucuyu yeniden başlatın. `zbrou_utils` kullanan tüm zbrou kaynakları ondan sonra başlatılmalıdır.
