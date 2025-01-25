---
description: >-
  When working with our frameworks, you may encounter some challenges. Here are
  some common issues and how to resolve them. If your issue is not in here open
  a ticket and we will assist you.
---

# ❌ Frequent Issues

***

<details>

<summary><em>Cursor Not Displaying</em></summary>

If you are experiencing an issue where the cursor does not appear on your server, it may be due to the use of a function called `ShutdownLoadingScreenNui();` in a loading screen. This function removes the cursor from the user interface framework. Follow the steps below to resolve the issue:

1. **Navigate to Your Loading Script Folder**: Locate your loading script folder and find the client script file. The file is usually named `client.lua`, but it may have a different name.
2. **Open the Client Script**: Open the client script file in a text editor. We recommend using Visual Studio Code, but any text editor will work.
3. **Locate the `ShutdownLoadingScreenNui()` Function**: Search for the function `ShutdownLoadingScreenNui()` in the client script.
4.  **Comment Out the Function**: Once you have located the function, comment it out by adding two dashes (`--`) before the function name. This will disable the function and prevent it from removing the cursor.

    ```lua
    -- ShutdownLoadingScreenNui();
    ```
5. **Save the Changes**: After commenting out the function, save the changes to the client script file.
6. **Restart Your Server**: Restart your server for the changes to take effect.

After completing these steps, the cursor should now display properly on your server. If you continue to experience issues, double-check the changes and ensure the server has been restarted properly.

</details>

<details>

<summary><em>Discord Rich Presence</em></summary>

### Configuration

Below is the configuration breakdown and instructions on how to set up the Rich Presence feature.

#### Config Options

```lua
Config.richPresence = {
    enabled = true,  -- Enable or disable the rich presence feature
    clientid = 801534049944207381, -- Your Discord bot application ID
    
    displayPlayingAs = "Currently playing as %s [%s]",
    -- This string defines how player information is displayed
    -- The first %s represents the player's name, the second %s represents their department
    -- Set to false to disable

    icons = {
        small = {
            text = "discord.gg/RquDVTfDwu",
            icon = "https://i.imgur.com/ZsuQUE3.png",  -- URL to the small icon
        },
        big = {
            text = "NAT2K15 RP",
            icon = "https://i.imgur.com/ZsuQUE3.png",  -- URL to the big icon
        }
    },

    discordButtons = {
        enabled = true,  -- Enable or disable Discord buttons
        button1 = {
            label = "Discord",  -- Button label
            url = "https://discord.gg/RquDVTfDwu"  -- Button link
        },
        button2 = {
            enabled = true,
            label = "Connect",  -- Button label
            url = "fivem://connect/IP:30120"  -- FiveM direct connect URL
        }
    }
}
```

### Step-by-Step Setup

#### 1. Setting Up Discord Application

1. Go to [Discord Developer Portal](https://discord.com/developers/applications).
2. Click **New Application** and give it a name.
3. Copy the `Application ID` and paste it into the `clientid` field in the config.

#### 2. Customizing Rich Presence

* **Player Display Format:**
  * Modify the `displayPlayingAs` field to change how player information appears.
  *   Example:

      ```lua
      displayPlayingAs = "Active: %s | Role: %s"
      ```
* **Icons:**
  * Change the small and big icon URLs by uploading your own image to [Imgur](https://imgur.com/) or any direct image host.

#### 3. Configuring Discord Buttons

* Ensure `discordButtons.enabled` is set to `true` to activate buttons.
* Modify the labels and URLs to fit your server's needs.
*   Example of button configuration:

    ```lua
    button1 = {
        label = "Join Discord",
        url = "https://discord.gg/YOURSERVER"
    }
    ```





</details>



