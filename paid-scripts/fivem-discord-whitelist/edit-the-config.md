# Edit the config

## Configuration

This script uses a `config.lua` file to manage its Discord-based whitelist/blacklist system. Below is a breakdown of each section and how to customize it.

***

## Top-Level Config

| Key                   | Type   | Description                                                                                               | Default                |
| --------------------- | ------ | --------------------------------------------------------------------------------------------------------- | ---------------------- |
| **`config.token`**    | string | The Discord bot token used to authenticate requests to the Discord API. This must be a valid bot token.   | `""` (empty string)    |
| **`config.serverId`** | string | The ID of your Discord server (guild). Used to fetch member roles and perform whitelist/blacklist checks. | `"800444740729307177"` |

***

### Messages

These are the user-facing messages displayed in different scenarios.

| Key                             | Type   | Description                                                                                                                           | Default                                                                                                                                                 |
| ------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`config.messages.whitelist`** | string | The message shown to a user who does not have the required roles when whitelist is enabled.                                           | `"Your account does not have the required roles to join this server."`                                                                                  |
| **`config.messages.blacklist`** | string | The message shown to a user who is blocked from joining because they hold a blacklisted role.                                         | `"Your account is blacklisted from this server."`                                                                                                       |
| **`config.messages.noroles`**   | string | The message shown if the script cannot retrieve the user's roles from Discord (e.g., Discord not connected or a temporary API issue). | `"We were unable to fetch your Discord roles. Please ensure your Discord is properly connected and try again. If the issue persists, contact support."` |

***

### Logging

Controls how the script logs connection events and other information to a Discord webhook.

| Key                          | Type    | Description                                                                                               | Default    |
| ---------------------------- | ------- | --------------------------------------------------------------------------------------------------------- | ---------- |
| **`config.logging.enabled`** | boolean | Enables or disables logging. If `true`, all relevant connection events are sent to the specified webhook. | `true`     |
| **`config.logging.webhook`** | string  | The URL of the Discord webhook to which logs are sent.                                                    | `"Change"` |
| **`config.logging.showIps`** | boolean | If `true`, the player's IP address is included in the logs. If `false`, the IP address is hidden.         | `true`     |

***

### Whitelist

If enabled, only users with roles listed in `allowedRoles` can join the server.

| Key                                 | Type    | Description                                                                                                         | Default                           |
| ----------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| **`config.whitelist.enabled`**      | boolean | Toggles the whitelist feature. If `true`, the script checks whether a player's roles match the allowed list.        | `false`                           |
| **`config.whitelist.allowedRoles`** | table   | A list of Discord role IDs permitted to join. Any user missing these roles will be denied entry if whitelist is on. | `{ "800444938793123871", "222" }` |

***

### Blacklist

If enabled, users with any of the roles listed in `blockedRoles` will be denied entry to the server.

| Key                                 | Type    | Description                                                                                                              | Default                           |
| ----------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------ | --------------------------------- |
| **`config.blacklist.enabled`**      | boolean | Toggles the blacklist feature. If `true`, any user with roles in the blocked list is automatically denied.               | `true`                            |
| **`config.blacklist.blockedRoles`** | table   | A list of Discord role IDs that are blocked from joining. If a user holds any of these roles, they will be denied entry. | `{ "800444938793123871", "222" }` |

***

### Example Usage

```lua
config.token = "YOUR_DISCORD_BOT_TOKEN"
config.serverId = "YOUR_DISCORD_SERVER_ID"

config.messages = {
    whitelist = "You do not meet the whitelist requirements.",
    blacklist = "You have been blacklisted from this server.",
    noroles = "Could not fetch roles. Please connect your Discord properly."
}

config.logging = {
    enabled = true,
    webhook = "YOUR_DISCORD_WEBHOOK_URL",
    showIps = true
}

config.whitelist = {
    enabled = false,
    allowedRoles = { "ROLE_ID_1", "ROLE_ID_2" }
}

config.blacklist = {
    enabled = true,
    blockedRoles = { "ROLE_ID_3", "ROLE_ID_4" }
}
```



