---
description: >-
  Managing EUP has never been this easy. Forget about SQL, messy configs, or
  constant edits. With Discord role integration and a simple, clean menu system,
  you can create unlimited departments.
---

# FiveM EUP V2

### Installation

You can also edit the config trough our config generator: [https://config.nat2k15.xyz ](https://config.nat2k15.xyz/)

#### 1. Prerequisites

* **Discord Bot Integration** (for role permissions)
* **NativeUI** (included in the script)

#### 2. File Structure

```
FiveM Eup V2/
├── client/
│   ├── NativeUI.lua          # NativeUI library
│   ├── client.lua            # Main client-side logic
│   └── editmenu.lua          # Admin edit menu
├── server/
│   ├── discord.lua           # Discord integration
│   └── server.lua            # Server-side logic
├── config.lua                # Client configuration
├── svConfig.lua              # Server configuration (Discord)
└── fxmanifest.lua            # Resource manifest
```

#### 3. Installation Steps

1. **Download and Extract**
   * Place the FiveM EUP V2folder in your server's `resources/` directory
2.  **Configure Discord Integration**

    * Edit `svConfig.lua`:

    ```lua
    configS.bot_token = "YOUR_DISCORD_BOT_TOKEN"
    configS.server_id = "YOUR_DISCORD_SERVER_ID"
    ```
3.  **Set Admin Roles**

    * Edit `config.lua` and add Discord role IDs to `adminRoles`:

    ```lua
    adminRoles = {
        "800444938793123871",  -- Replace with your admin role ID
        "123456789012345678",  -- Add more role IDs as needed
    }
    ```
4.  **Add to server.cfg**

    ```
    ensure eup-menu
    ```
5. **Restart Server**

### Configuration

#### Client Configuration (`config.lua`)

```lua
config = {
    debug = false,                    -- Enable debug logging
    defaultMenuPosition = "right",    -- Menu position: "right", "left"
    width = 80,                      -- Menu width
    menuName = "EUP Menu",           -- Main menu title
    menuSubtitle = "Your Subtitle",  -- Menu subtitle
    banner = {
        enabled = false,             -- Enable custom banner
        url = "https://example.com/banner.png"  -- Banner image URL
    },
    adminRoles = {
        "800444938793123871",        -- Discord role IDs with admin access
    }
}
```

#### Server Configuration (`svConfig.lua`)

```lua
configS = {
    bot_token = "YOUR_BOT_TOKEN",    -- Discord bot token
    server_id = "YOUR_SERVER_ID"     -- Discord server ID
}
```

### Usage

#### For Players

* **Command**: `/eup`
* Navigate through departments using the menu
* Click on outfit names to apply them
* Use arrow indicators (→) to enter sub-menus
* Use "← Go Back" to return to parent menus

#### For Administrators

* Use the `/eupedit` command
* Admins will see additional options in the edit menu
* Can create, edit, and delete departments and outfits
* Can assign role requirements to specific items



### Permission System

#### Role-Based Access

* Assign Discord role IDs to departments or individual outfits
* Players must have the required role to see/use the item
* Admins (configured in `adminRoles`) can access everything

#### Setting Permissions

```lua
-- Department with role requirement
{
    name = "Police Department",
    requiredRole = "123456789012345678",
    children = { ... }
}

-- Individual outfit with role requirement
{
    label = "SWAT Gear",
    requiredRole = "987654321098765432",
    clothing = { ... }
}
```

### Troubleshooting

#### Common Issues

1. **Menu Not Opening**
   * Check console for errors
   * Verify Discord integration is working
   * Enable debug mode: `config.debug = true`
2. **Outfits Not Applying**
   * Check clothing data structure
   * Verify drawable/texture values are valid
   * Enable debug logging to see application process
3. **Permission Issues**
   * Verify Discord role IDs are correct
   * Check bot token and server ID
   * Ensure bot has proper permissions
4. **Admin Menu Not Accessible**
   * Verify your Discord role ID is in `config.adminRoles`
   * Check Discord integration is functioning
   * Restart the resource after config changes

#### Debug Mode

Enable debug logging by setting `config.debug = true` in `config.lua`. This will provide detailed console output for:

* Clothing application process
* Permission checks
* Menu operations
* Server-side tree operations

#### Console Commands

* `/eup` - Open the EUP menu

### Advanced Features

#### Custom Banners

Enable custom menu banners by configuring:

```lua
banner = {
    enabled = true,
    url = "https://your-image-url.com/banner.png"
}
```

#### Menu Positioning

Configure default menu position:

* `"left"` - Left side of screen
* `"right"` - Right side of screen
* `nil` or other - Center position

### Data Storage

* Outfit configurations are stored in FiveM's Key-Value Pair (KVP) system
* Data persists across server restarts
* Admins can modify configurations in real-time

### Support

For issues or questions:

1. Check the console for error messages
2. Enable debug mode for detailed logging
3. Verify all configuration values are correct
4. Ensure Discord integration is properly set up

[https://discord.gg/RquDVTfDwu](https://discord.gg/RquDVTfDwu)

