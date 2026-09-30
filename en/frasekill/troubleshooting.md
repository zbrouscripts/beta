# Troubleshooting

## `/frasekill` does not open

- Check `Config.Access.Mode`.
- Confirm the player has manual, ACE, group or Tebex access.
- Run `/frasekillstatus`.

## FraseKill does not appear after a kill

- The killer must be another player; NPC kills are ignored.
- Check the detected medical adapter.
- Killer and victim must be in the same routing bucket.
- Review `Config.Death.RequireServerDead`.
- Test a normal player-vs-player kill before debugging custom integrations.

## The phrase does not save

- Confirm `oxmysql` starts before FraseKill.
- Check `Config.MaxCharacters`.
- Check blocked URLs/words and the custom validator.
- Review SQL errors in the server console.

## QB/Qbox death systems

Use the default `auto` adapter unless you have a specific reason to force one. Supported QB ambulance resource names include `qb-ambulancejob` and the compatibility alias `qb_ambulancejob`.

## A font looks different

Web fonts use Google Fonts with local/system fallbacks. If CEF cannot load the remote font temporarily, FraseKill remains functional using its fallback.

## Database starts late

FraseKill retries database initialization automatically. If it never becomes ready, check `oxmysql` and your database connection.
