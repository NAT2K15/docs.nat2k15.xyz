---
description: in this page you will find all the change logs for the Framework
---

# ✒️ Change Logs



<details>

<summary>Change Log 2.2.2 Auto Editor and more</summary>



## Changelog

#### Fixes

* Fixed some people not seeing the character UI when loading in. (`client/client.lua`)
* Fixed the `/loadout` command not working.
* Fixed the config not saving via admin panel (`html/js/script.js`).
* Fixed the shot spotter not working (`server/server.lua`).
* Fixed `/me` not displaying when in a vehicle.
* Fixed the issue with people falling through the map when spawning.
* Fixed disabling `/do` not working.

#### Improvements

* Made it so editing the config through the admin panel once saved will automatically change the variables without needing to restart the server.
* Changed image hosting to [ImgBB](https://imgbb.com/) due to issues with Imgur.
* Increased the character limit design.
* The config editor now works faster and automatically; no need to restart the server/resource anymore.
* Removed the blue border from every button and input.
* Added a small fade-in effect when using `/fw` or `/framework`.
* Improved console logging when the framework is started.
* Changed how the `version_checker` is used.

#### Additions

* Added a timestamp in the Discord logging.
* Added the user ID when using the OOC command.
* Added a config option for admins to have access to all departments.

</details>

<details>

<summary>Change Log 2.1.2 Beta Fixes</summary>

Thank you everyone for finding the bugs and reporting them after a deep dive of looking at the errors I was able to fix the two major ones. If you are still having issues make sure you replace all the files including the config.

#### Fixes

* fixed the hide is not defined (script.js)
* fixed the adminchat not working (commands.lua)
* fixed 911 commands typo (server folder, client folder)

</details>

<details>

<summary>Change Log 2.1 Much Needed Update</summary>



Yes after hundreds of requests we have added the blip system back. View below what else has been added. A lot of issues not listed in here have been fixed including exploits found my clients. Keep in mind this is in beta until I 100% am sure that not issues are found.

#### Add/Remove

* Added Blip System
* Added a age for Sonoran cad when creating a new character
* Added syntax highlighting for the config editor in the admin panel
* Added an option to change the play as button
* Added a setting to move the hud (client side)
* Added a message for calladmin /calladmin (optional)
* Added some database stuff for exporting (auto)
* Remove lua error checking for the config in the admin panel

#### Fixes/Changes

* Cloud spawning
* hud not moving when changing the config
* Commands causing the chat to freeze
* /telp command not working
* door lock
* default images and custom images
* Cursor not displaying when having a loadingscreen
* /calladmin sending duplicated
* loc = nil error
* Framework settings features
* Sonoran cad API issues
* All Commands have been tested and fixed, aswell as logs to discord
* made the auto import SQL much faster and better.

</details>

<details>

<summary>Change Log 2.0 BETA</summary>

### Added

* Added a mute system
* Added a loading bar
* Added an option to switch the position of your framework
* Added a new logging system
* Added a config to disable the last location
* Added the ability for admins to lock/unlock doors.
* Added a more UI friendly/design for some of the main UI buttons
* Added a config option to remove "Do not Teleport"
* Added the option for the whitelist system to use ACE perms
* Added a custom background image in the client settings
* Added a scrollbar if the user's characters hit over 12.
* Added the option to add more than just 25 characters. (It is up to you now there is no max)
* Added text when reaching the maximum number of characters
* Added back some icons to display on the buttons
* Added the option to add components in the loadout system
* Added back the highly requested shot spotter.
* Added the option to add postal to the shot spotter
* Added a new design for all our huds. We now use HTML
* Added a street label Hud
* Added a blip system for the panic
* Added the option to have your department's alphabetic orders within the config.
* Redesigned the characters section in the admin panel to be more user appealing
* Added the option to search a user's characters by discord
* Added a department name in the info section within the admin panel
* Added a little fade with all the buttons to create a better experience
* Added a different colour into our framework.
* Added the effect of the colour changing when hovering over something
* Added a little bit of space in the admin panel so it doesn't seem so lacerated

### Changes

* Changed the required files to use a CDN in stade of a local file.
* Changed some functions around
* Changed some of the colours within the Framework UI
* Changed the text of the you are playing as.
* Changed the panic and Shot spotter text
* Changed the website button to stay within the Framework panel
* Changed the discord button to stay within the Framework panel
* Changed how the door lock works to improve permofermnce
* Changed the door lock to use HTML notification
* Changed the Framework.RegisterCommand to work with our new mute system
* Changed quite a bit of the config (Read below for more info)
* Changed how the discord-rich presence to allow better configurable options
* Changed how some of our debug systems work
* Changed our Auto Upload SQL. **DO NOT DELETE sql.sql** (unless you know what you're doing)

### Fixes

* Fixed the connection issue a lot of people were having
* Fixed some sync issues with the door lock
* Fixed an issue with the door lock when respawning
* Fixed the issue with your game crashing when switching characters
* Fixed the discord button not working
* Fixed the website button not working
* Fixed the info button not displaying icons in the Framework UI
* Fixed an issue when the background duplicated when its too small
* Fixed most known bugs as well as found bugs when working on the framework
* Fixed the auto SQL system

## Notable Changes

#### Framework Performance

Some parts of the framework have been written to improve performance and after successfully fixing and changing a lot of things we are proud to say: Our Framework should sit at 2-4% ms when in the Framework UI, and stay at 6-8& when in the game. The framework has dropped a significant amount (it used to sit at 14-17%)

#### HTML Huds

As mentioned in our additions above we have migrated from default GTA text into HTML huds. We have asked a lot of clients and most people would prefer it that way.

#### Shot Spotter

YES. Shot spotter has been added back and it is better than ever. When our team tested the system we found it to be much more accurate and better performance.

#### Removed our ban system

We have decided to remove our ban system from the admin panel. After reviewing and listening to our customers we have noticed that the ban system doesn't get used much and causing some issues.

#### Switched from MySQL to oxmysql

After being asked numerous times to switch we have finally done it. if you currently use MySQL-Async here is a guide on how to install oxmysql https://overextended.dev/oxmysql#download-the-latest-release

#### Config Changes

We have changed how our config is set up. We changed how departments get created within the config. We have also made the option to allow everyone access much easier. Ensure to redo all the config because a lot has changed.

#### Door lock

After so many users have told us how much they like the door lock and how buggy it is sometimes. We have decided to rework parts of the code to make it much more user-friendly as well as do some needed optimization.

#### File Structure

We have changed how our file structure works. **Ensure you replace all the files and start editing your config from scratch** Before you open a ticket ensure you changed your entire config.

</details>



{% embed url="https://store.nat2k15.xyz/store/framework-v2" %}
