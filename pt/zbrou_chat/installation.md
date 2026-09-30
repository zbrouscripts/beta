# Instalação

### 1. Copie os recursos

Coloque `zbrou_utils` e `zbrou_chat` na pasta de recursos do servidor.

### 2. Remova o chat anterior

Para evitar duas interfaces de chat ao mesmo tempo:

* remova ou desative `esx_rpchat`;
* remova ou desative `esx_chat_theme`;
* remova ou comente `ensure chat` no `server.cfg`.

### 3. Adicione sua Rockstar license

Abra `zbrou_chat/config.lua`. Existem dois níveis de acesso:

**Owner — configuração + moderação**

```lua
Config.ModerationPermissions.Owners = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

**Editor — somente configuração**

```lua
Config.ScriptConfiguration.Editors = {
    'license:YOUR_ROCKSTAR_LICENSE'
}
```

O acesso correspondente permite configurar o chat no jogo com `/zbrou`. Use `Owners` se também precisar das ferramentas de moderação.

### 4. Avatares do Discord — opcional

Abra `zbrou_utils/server/private.lua` e cole apenas o token:

```lua
ZBrouPrivate.DiscordBotToken = 'YOUR_DISCORD_BOT_TOKEN'
```

{% hint style="info" %}
O bot **não precisa de permissões, comandos nem estar em nenhum servidor do Discord**. Você só precisa de um token de bot válido.
{% endhint %}

### 5. Ordem recomendada no `server.cfg`

```cfg
ensure oxmysql
ensure zbrou_utils
ensure zbrou_chat
```

Se usar `ghmattimysql`, pode iniciá-lo no lugar de `oxmysql`. Não é necessário importar SQL manualmente: as tabelas são criadas automaticamente quando há um driver compatível.

### 6. Inicie e configure

Reinicie o servidor, entre no jogo e execute `/zbrou`. Depois abra **CHAT → Configuração**.
