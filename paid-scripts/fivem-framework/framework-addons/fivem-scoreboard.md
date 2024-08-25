---
description: >-
  Slick FiveM scoreboard designed to work with our framework. level up your
  server with a clean design.
icon: clipboard
cover: ../../../.gitbook/assets/feat-3zxreF5_B8xHiu52WTIohTFX9.png
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# FiveM Scoreboard

## Setup

1. Extract the zip folder into your resource folder and name the script `framework-scoreboard`&#x20;
2. Edit the config to your liking a breakdown of the config will be below.&#x20;
3. Start the resource after the framework&#x20;
4. Load in and test :smile:

```
ensure framework
ensure framework-scoreboard
```

## Configuration Documentation

```lua
config = {}
config.delay = 1500 -- Delay in milliseconds between each check
config.key = 27 -- Key to open the menu

config.uiSettings = {
    serverName = "NAT RP - {playercount}", -- Possible varibles {playercount}
    banner = {
        enabled = true,
        url = "https://i.ibb.co/hFRM77G/faxsstore.png"
    },
    ping = {
        enabled = false
    }
}
```

### Global Configuration

* **`config.delay`**:\
  Sets the delay in milliseconds between each check.
  * **Type**: Integer
  * **Default**: `1500`
* **`config.key`**:\
  Specifies the key used to open the menu.
  * **Type**: Integer
  * **Default**: `27` (This usually corresponds to the 'ESC' key)

### UI Settings (`config.uiSettings`)

The `config.uiSettings` table contains settings related to the user interface.

#### Server Name (`serverName`)

* **`serverName`**:\
  The name of the server displayed in the UI.
  * **Type**: String
  * **Default**: `"NAT RP - {playercount}"`
  * **Description**: You can use the `{playercount}` variable to dynamically display the current number of players.

#### Banner (`banner`)

* **`banner.enabled`**:\
  Enables or disables the display of a banner in the UI.
  * **Type**: Boolean
  * **Default**: `true`
* **`banner.url`**:\
  The URL of the image used as the banner.
  * **Type**: String
  * **Default**: `"https://i.ibb.co/hFRM77G/faxsstore.png"`

#### Ping (`ping`)

* **`ping.enabled`**:\
  Enables or disables the display of the ping information in the UI.
  * **Type**: Boolean
  * **Default**: `false`

### Known Issues

if you have changed the default name of the framework to lets say rp-framework. You will need to modify the server.lua. \


1. Go into `Framework-scoreboard/server/server.lua`&#x20;
2. Edit the framework to match your resource name. Only edit what's in the "framework"

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Framework-scoreboard/server/server.lua</p></figcaption></figure>



