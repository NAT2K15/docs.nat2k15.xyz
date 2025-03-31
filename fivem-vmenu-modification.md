---
description: >-
  Elevate your server management with our enhanced logging modification for
  vMenu 3.6.5. Here’s what makes it stand out:
---

# FiveM vMenu Modification

**Step-by-Step Installation Guide for vMenu Logs**

1. **Extract the Files:**
   * Download the provided .rar file.
   * Use an extraction tool (like WinRAR or 7-Zip) to unzip the file.
2. **Replace the vMenu Folder:**
   * Locate the existing **vMenu** folder in your server directory.
   * Replace it with the new **vMenu** folder from the extracted files.
3. **Configure the Discord Webhook:**
   * Open the `server.lua` file using your preferred text editor.
   *   At the top of the file, find the line:

       ```lua
       local DISCORD_WEBHOOK_URL = "CHANGE ME"
       ```
   * Replace `"CHANGE ME"` with your actual Discord webhook URL.
   * Save the changes.
4. **Restart Your Server:**
   * Restart your server to apply the new changes and start logging.
