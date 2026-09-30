# Tebex i wygaśnięcia

FraseKill can grant access using Tebex Game Server Commands. No Tebex API key is stored inside the resource.

## Enable Tebex

```lua
Config.Tebex.Enabled = true
```

## Plans

```lua
Config.Tebex.Plans = {
    week = { Label = '1 semana', Days = 7 },
    month = { Label = '1 mes', Days = 30 },
    year = { Label = '1 año', Days = 365 },
    permanent = { Label = 'Permanente', Permanent = true }
}
```

Supported durations: `Minutes`, `Hours`, `Days`, `Weeks`, `Months`, `Years`, or `Permanent=true`.

## Initial / renewal command

```text
frasekill_tebex {id} month {transaction}
```

## Refund / chargeback

```text
frasekill_tebex_revoke {id} {transaction}
```

Each Tebex transaction is stored separately. Revoking one transaction does not remove unrelated purchases or renewals. Normal timed plans expire automatically.

## Expiration notifications

```lua
Config.ExpiryNotifications = {
    Enabled = true,
    CheckSeconds = 60,
    Thresholds = { 86400, 3600, 600 }
}
```

The default thresholds are 24 hours, 1 hour and 10 minutes before expiration.
