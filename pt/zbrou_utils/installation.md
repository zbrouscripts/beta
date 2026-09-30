# Instalação

### 1. Copie o recurso

Coloque `zbrou_utils` na pasta de recursos do servidor.

### 2. Adicione ao `server.cfg`

`zbrou_utils` deve iniciar antes de qualquer outro recurso zbrou que dependa dele.

```cfg
ensure oxmysql
ensure zbrou_utils
```

Se já usa `ghmattimysql`, pode usá-lo no lugar de `oxmysql`. As tabelas necessárias são criadas automaticamente; normalmente não é preciso importar SQL manualmente.

### 3. Avatares do Discord — opcional

Abra `zbrou_utils/server/private.lua`:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
O bot **não precisa de permissões, comandos nem estar em nenhum servidor do Discord**. Você só precisa de um token de bot válido.
{% endhint %}

### 4. Inicie o servidor

Reinicie o servidor. Todos os recursos zbrou que usam `zbrou_utils` devem iniciar depois dele.
