# ClientGuard — Mod Detection

<img src="assets/clientguard-icon.png" width="128" alt="ClientGuard icon">

**[View ClientGuard on SpigotMC](https://www.spigotmc.org/resources/clientguard-mod-detection.139970/)** · **[Download the latest JAR](https://github.com/xDiamondBeerx/ClientGuard-Releases/releases/latest/download/ClientGuard.jar)**

Client and mod detection for Paper/Purpur 26.2. Requires Java 25.

Download [ClientGuard.jar](https://github.com/xDiamondBeerx/ClientGuard-Releases/releases/latest), put it in `plugins` and restart your server.

Open `/cg` to view players, detected mods and previous alerts. Give staff `clientguard.staff` to access the menu. Each staff member can turn their chat notifications on or off. OPs also have access to settings and updates.

ClientGuard checks client brands, network channels, reported mods and supported resource checks during login. Detection depends on what the client exposes. A detected mod does not prove its features are enabled, and some mods cannot be detected reliably. ClientGuard does not ban players.

Discord is optional. Set your own webhook or DiscordSRV destination in the configuration.

## Features

- Recognize supported client and mod signals, including Freecam and Tweakeroo.
- Allow or block specific mods through config.yml. Warning and Critical mods are blocked by default; OPs and bypass players are exempt.
- Review alerts and evidence in `/cg`, with a personal notification toggle for staff.
- Keep flagged player history without creating another entry for each repeat join with the same flags.
- Send optional Discord notifications and install verified updates at the next server restart.

## Updates

Updates are checked 30 seconds after startup and every six hours. With automatic updates enabled, verified downloads are installed on the next server restart. OPs receive update notices. No GitHub token is needed.

## Upgrading from 1.12.x

This version renames the plugin and permissions. Install it manually once:

1. Stop the server and back up your plugin data.
2. Remove the old plugin JAR and any queued copy from `plugins/update`.
3. Add `ClientGuard.jar`. Keep only one installed copy.
4. Change your permission grants to `clientguard.*` before starting the server. Update bypass and skip-probes grants too.
5. Start the server. The previous data folder is moved to `plugins/ClientGuard` automatically. If both data folders already contain files, they are left untouched; choose the correct folder while the server is stopped.

Existing config, rules, history and notification preferences move with the folder. If you use a webhook environment variable, use `CLIENTGUARD_WEBHOOK` and set `discord.webhook-env` accordingly.

## Permissions

| Permission | Purpose |
|---|---|
| `clientguard.staff` | Staff menu and notifications |
| `clientguard.bypass` | Allow joining with blocked mods; keep monitoring records private to OPs |
| `clientguard.skip-probes` | Skip join resource checks |

Administration requires actual OP status. OP players are excluded from monitoring.

