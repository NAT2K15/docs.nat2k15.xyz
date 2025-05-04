---
description: >-
  A very basic script that administrators can use for staff tasks like setting
  up admin areas. As a result, other players are aware of the staff issue.
---

# FiveM Admin Zone



***

### 📁 File: `config.lua`

#### Full Example:

```lua
config = {}

config.message = "~r~You are near an staff situation, please stay away."
config.text = {
    x = 0.45,
    y = 0.0
}

config.defaultRadius = 100  -- Default radius for the zone (in game units/metres)
config.maxRadius = 100      -- Maximum allowed radius

config.perms = {
    useFramework = true,
    frameworkName = "framework",      -- Your framework resource name (e.g., "esx", "qb-core")
    departmentLevel = "admin_level",  -- The permission key/level inside your framework

    acePerms = "zone.clear"           -- Fallback ACE permission if framework is disabled
}
```

***

### 🔔 What It Does

* Displays a **warning message** on screen when a player is near an active staff situation or zone.
* Uses either **framework-based permissions** or **ACE permissions** to allow staff to manage these zones.
* Supports radius configuration to define how close a player can get before receiving the alert.

***

### 🧾 Configuration Breakdown

#### 🧨 `config.message`

This is the message displayed to players who enter the restricted zone.

```lua
config.message = "~r~You are near an staff situation, please stay away."
```

> You can use in-game color codes (e.g., `~r~` for red, `~b~` for blue).

***

#### 🧭 `config.text`

Sets the screen coordinates for the warning message:

```lua
config.text = {
    x = 0.45,
    y = 0.0
}
```

* `x`: Horizontal position (0.0 left to 1.0 right)
* `y`: Vertical position (0.0 top to 1.0 bottom)

***

#### 📏 `config.defaultRadius` & `config.maxRadius`

Defines the distance (in meters) around the staff zone where the warning becomes active.

```lua
config.defaultRadius = 100
config.maxRadius = 100
```

> The system may allow setting custom radii on a per-zone basis, up to `maxRadius`.

***

### 🔐 Permissions Setup

You can control who can create or manage these zones using either a framework or ACE permissions.

#### ✅ Framework Mode

```lua
config.perms.useFramework = true
config.perms.frameworkName = "framework"
config.perms.departmentLevel = "admin_level"
```

* **useFramework**: Enables permission checking through your framework.
* **frameworkName**: Name of the framework resource (e.g., `"framework"`).
* **departmentLevel**: Key used to identify admins (e.g., check if `PlayerData.dept == "admin"` or similar department in your framework).

***

#### 🔒 ACE Permissions Mode

If your server doesn’t use a framework or you prefer ACE-based permissions:

```lua
config.perms.useFramework = false
config.perms.acePerms = "zone.clear"
```

To grant access:

In your `server.cfg`, add:

```
add_ace group.admin "zone.clear" allow
```

***

### ✅ Summary

| Setting         | Purpose                                                |
| --------------- | ------------------------------------------------------ |
| `message`       | The warning shown to players                           |
| `text`          | Where the message appears on screen                    |
| `defaultRadius` | Default warning zone size                              |
| `maxRadius`     | Max limit for warning zones                            |
| `perms`         | Handles who can create/manage zones (framework or ACE) |

***
