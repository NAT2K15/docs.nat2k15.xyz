---
description: >-
  There are two main configs you need to edit the rest are all commands trough
  discord
---

# Editing the Config

## vehicle-whitelist/config.lua

***

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**1. Basic Configuration**

* **`config.deleteOldVehicles = true`**
  * **Description**: This setting determines whether old vehicles should be automatically deleted when certain conditions are met.
  * **Default Value**: `true`
  * **Usage**: Set this to `true` to enable automatic deletion of old vehicles, or `false` to keep them.

**2. Text Configuration**

Customize the messages displayed to users in various scenarios by modifying the `config.text` table.

* **`deleteMessage`**
  * **Description**: Message displayed when a player tries to access a vehicle they do not have permission for.
  * **Default Value**: `"You do not have access to this personal vehicle."`
* **`notYourVehicleToTrustMsg`**
  * **Description**: Message shown when a player tries to grant or revoke access to a vehicle they do not own.
  * **Default Value**: `'You do not own the inputted vehicle, therefore you cannot trust/untrust another player to drive it.'`
* **`maxSlots`**
  * **Description**: Message displayed when a player attempts to add more users to their vehicle than the allowed limit.
  * **Default Value**: `"You cannot trust anymore players to use your vehicle (Max slot limit reached)."`

**3. Menu Configuration**

The `config.menu` table controls how the vehicle keys menu is accessed and displayed.

* **`menu_title`**
  * **Description**: Sets the title of the vehicle keys menu.
  * **Default Value**: `"Vehicle Keys"`
* **`use_command_to_open`**
  * **Description**: Determines if a command can be used to open the vehicle keys menu.
  * **Default Value**: `true`
  * **Usage**: Set to `true` to enable the command or `false` to disable it.
* **`command_to_open`**
  * **Description**: The command players need to type to open the vehicle keys menu.
  * **Default Value**: `"keys"`
* **`use_keybind_to_open`**
  * **Description**: Determines if a keybind can be used to open the vehicle keys menu.
  * **Default Value**: `false`
  * **Usage**: Set to `true` to enable the keybind or `false` to disable it.
* **`keybind_to_open`**
  * **Description**: The keybind players can use to open the vehicle keys menu if keybinds are enabled.
  * **Default Value**: `'F6'`
  * **Note**: This keybind is only active if `use_keybind_to_open` is set to `true`.
* **`owned_menu_emoji`**
  * **Description**: Emoji displayed next to vehicles the player owns in the menu.
  * **Default Value**: `'🔑'`
* **`shared_menu_emoji`**
  * **Description**: Emoji displayed next to vehicles the player has access to but doesn’t own.
  * **Default Value**: `'🔑'`

***

## vehicle-whitelist/config.json

<figure><img src="../.gitbook/assets/image (8).png" alt="" width="375"><figcaption></figcaption></figure>

**1. Token Configuration**

* **`token`**
  * **Description**: This is the bot's token, which is required for the bot to connect to Discord.
  * **Value**: Replace `"tokengoeshere"` with your actual bot token.

**2. Database Configuration**

* **`databasecheck`**
  * **Description**: This parameter likely controls how often the bot checks the database. The value `5` might represent a time interval or a number of retries.
  * **Default Value**: `5`
* **`database`**
  * **Description**: Contains the necessary information to connect to the database where your application's data is stored.
  * **`host`**: The hostname of your database server. `"localhost"` indicates that the database is hosted on the same machine as the bot.
  * **`user`**: The username used to connect to the database. Typically `"root"` for local development.
  * **`password`**: The password for the database user. An empty string `""` indicates no password is set.
  * **`database`**: The name of the specific database your application will use. In this case, it's `"fivem"`.

**3. Presence Configuration**

* **`presence`**
  * **Description**: This section configures how the bot appears on Discord, including its status and activity.
  * **`updateTime`**: How frequently (in minutes or seconds) the bot’s presence information is updated. Here, it's set to `3`.
  * **`status`**: The bot’s online status. `"online"` means the bot will appear as online.
  * **`activity`**: The text displayed as the bot’s current activity. `"NAT RP"` indicates that the bot is "Playing NAT RP".
  * **`type`**: The type of activity the bot is showing. `"PLAYING"` indicates the bot is showing a "Playing" status.

**4. Embed Configuration**

* **`embed`**
  * **Description**: Defines the appearance and details of embeds (rich message formats) the bot sends on Discord.
  * **`name`**: The name displayed in the embed, in this case `"NAT RP"`.
  * **`footer`**: The text displayed in the footer of the embed, also `"NAT RP"`.
  * **`color`**: The color of the embed's sidebar. `"BLUE"` sets the color to blue.

**5. Permissions Configuration**

* **`permissions`**
  * **Description**: This section defines which users or roles have permissions for specific bot commands or actions.
  * **`guild`**: The ID of the Discord server (guild) where the bot is active. The value `"800444740729307177"` is the server’s unique ID.
  * **`roles`**: An array of role IDs that have specific permissions. In this case, the role ID `"800444938793123871"` is listed, meaning members with this role have the required permissions.

**6. Logging Configuration**

* **`logging`**
  * **Description**: This section specifies where the bot logs certain actions, such as when users are added, removed, or trusted.
  * **`added`**: The channel ID where logs related to adding users or vehicles will be sent. The ID `"1255329863498338385"` indicates the specific channel.
  * **`removed`**: The channel ID for logs when users or vehicles are removed, using the same ID.
  * **`trusted`**: The channel ID where logs related to trusting users with vehicles are sent, also using the same ID.

#### Final Remarks

Make sure to customize these configurations to suit the unique requirements of your server. The provided settings are designed to be flexible, enabling you to fine-tune the personal vehicle system for an optimal player experience. Adjust the messages, commands, and menu options to align with your server's gameplay style and rules. You can confirm that everything is functioning correctly if your server console displays the following output:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
