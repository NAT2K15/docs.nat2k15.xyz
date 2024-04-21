---
description: >-
  Below you will find some of the issues you might run into when configuring the
  massive config file.
---

# ❌ Frequent Issues

***

## _Cursor Not Displaying:_

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
