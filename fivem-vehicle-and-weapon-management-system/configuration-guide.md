---
description: >-
  This document explains how to edit your config.lua file to set up your Discord
  bot token and server-specific settings properly.
---

# Configuration Guide

***

### 📁 File: `config.lua`

#### Sample Config:

```lua
config = {}

config.token = ""  -- Your Discord bot token goes here
config.serverId = "800444740729307177"

config.commandName = "vehicleconfig"  -- Command to open or trigger vehicle config features
config.adminRefreshRoles = "refresh-roles"  -- Admin-only command to refresh someone's roles

config.allowAdminBypass = true  -- If true, users with admin roles can bypass restrictions

config.adminRoles = {
    "800444938793123871"  -- Role IDs that are allowed to use admin commands
}
```

***

### 🧾 How to Edit

#### 1. 🔐 **Insert Your Bot Token**

Get your token from the [Discord Developer Portal](https://discord.com/developers/applications):

* Go to your bot application
* Navigate to **Bot > Token > Click "Copy"**
* Paste it into `config.token`:

```lua
config.token = "YOUR_BOT_TOKEN_HERE"
```

⚠️ **Do NOT share this token with anyone!**

***

#### 2. 🆔 **Set the Server ID**

Replace the existing `config.serverId` with the **ID of the Discord server** your bot will operate in:

```lua
config.serverId = "YOUR_SERVER_ID"
```

You can right-click your server in Discord (developer mode enabled) to copy the ID.

***

#### 3. 🔁 **Change Command Names (Optional)**

You can customize the slash commands used in Discord:

```lua
config.commandName = "vehicleconfig"  -- Main command
config.adminRefreshRoles = "refresh-roles"  -- Admin-only subcommand
```

***

#### 4. 👮‍♂️ **Enable or Disable Admin Bypass**

This allows users with the defined admin roles to bypass restrictions (like checks or cooldowns):

```lua
config.allowAdminBypass = true  -- or false
```

***

#### 5. 🎖️ **Configure Admin Roles**

Replace the role IDs with your server's admin role(s). You can add multiple role IDs:

```lua
config.adminRoles = {
    "ROLE_ID_1",
    "ROLE_ID_2"
}
```

To get a role ID in Discord:

* Enable Developer Mode (User Settings > Advanced > Developer Mode)
* Right-click a role > **Copy ID**

***

### ✅ Example Final Config

```lua
config.token = "MzYzNzEyMzEyMzEyMzEyMzEyMzEy"  -- Your bot token
config.serverId = "123456789012345678"

config.commandName = "vehconfig"
config.adminRefreshRoles = "reloadroles"
config.allowAdminBypass = true

config.adminRoles = {
    "987654321098765432",  -- Admin role 1
    "876543210987654321"   -- Admin role 2
}
```

***
