---
description: >-
  This docs is fairly new does not have all of the export we provide please be
  patient while we slowly work on this.
---

# Client Side Exports

At the top of your client file. You will need to call the Framework's exports. This step is very crucial for all the exports to work properly.&#x20;

```lua
Framework = exports["framework"]:getClientFunctions()    
```

The "framework" will be the folder name the FiveM owner has in its resource. We recommend making this option configurable as not all users will have the default folder called framework.



<details>

<summary>Framework.isPlayerLoadedIn()</summary>

This will check if the player is fully loaded in to a character. It will return either a false or true here is an example.

```lua
Citizen.CreateThread(function()
    while true do 
        Citizen.Wait(500)
        if Framework.isPlayerLoadedIn() then
            print("Player is loaded in")
        else 
            print("Player is not loaded in")
        end
    end
end)
```

</details>

<details>

<summary>Framework.getPlayer(Framework.serverId)</summary>

In the client side you can only request the clients data. We have disabled the option to allow you to request any users data as it should all be done on the server side. To simply request the data do&#x20;

```lua
local player = Framework.getPlayer(Framework.serverId) 
print(json.encode(player)) -- this will print all of the users data
```

Here is an example of it working in a command

```lua
RegisterCommand("whatsmyname", function(source, args, message)
    local player = Framework.getPlayer(Framework.serverId)
    if(player) then
        TriggerEvent('chatMessage', "Your name is " .. player.char_name)
    else 
        TriggerEvent('chatMessage', "you are not loaded in via the framework")
    end
end)
```

</details>

<details>

<summary>Framework.getAop()</summary>

Will return the current AOP you have in the server. If the AOP is disabled in the framework it will return a nil value.

{% code title="Command example" %}
```lua
RegisterCommand("getcurrentaop", function(source, args, message) then
    local aop = Framework.getAop()
    if(aop) then    
        print("The current AOP is " .. aop)
    else 
        print("AOP has been disabled in the framework")
    end
end)
```
{% endcode %}

</details>

<details>

<summary>Framework.ShowInfo()</summary>

If you want to show text on the bottom left of the screen above the hud you can now simply do that with this export

```lua
RegisterCommand('showinfo', function(source, args, message) 
    Framework.ShowInfo("This is a test message")
end)
```



<img src="https://i.imgur.com/zpppdMh.png" alt="" data-size="original">

</details>

<details>

<summary>Framework.DisplayHelpText()</summary>

This export will display the message on the top left of your screen.&#x20;

```lua
RegisterCommand('showhelp', function(source, args, message) 
    Framework.DisplayHelpText("I need help")
end)
```

<img src="https://i.imgur.com/xLP16Im.png" alt="" data-size="original">

</details>

<details>

<summary>Framework.setHealth()</summary>

Very simple export that will set the players health. It will set the clients health to the amount provided.

```
Framework.setHealth(100)
```

</details>

<details>

<summary>Framework.setArmor()</summary>



Very simple export that will set the players armor. It will set the clients armor to the amount provided.

```
Framework.setArmor(100)
```

</details>

