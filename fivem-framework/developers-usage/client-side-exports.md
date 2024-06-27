---
description: >-
  This docs is fairly new does not have all of the export we provide please be
  patient while we slowly work on this.
---

# Client Side Exports

At the top of your client file. You will need to call the Framework's exports. This step is very crucial for all the exports to work properly.&#x20;

```
Framework = exports["framework"]:getClientFunctions()    
```

The "framework" will be the folder name the FiveM owner has in its resource. We recommend making this option configurable as not all users will have the default folder called framework.



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

