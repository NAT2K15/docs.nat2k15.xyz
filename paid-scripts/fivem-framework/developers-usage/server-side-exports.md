---
description: Working on this docs! [NOT FINISHED]
---

# Server Side Exports

At the top of your server file. You will need to call the Framework's exports. This step is very crucial for all the exports to work properly.&#x20;

```lua
Framework = exports["framework"]:getServerFunctions()    
```

The "framework" will be the folder name the FiveM owner has in its resource. We recommend making this option configurable as not all users will have the default folder called framework.



<details>

<summary>Framework.getPlayers()</summary>

Using this export you will be able to get all the active players with all their character info and  print it. here is an exmaple

```lua
for _, player in pairs(Framework.getPlayers()) do 
    print(json.encode(player))
end
```

</details>

<details>

<summary>Framework.getPlayer()</summary>

Using this export you can get any  player as long as they are in the server and logged in.

```lua
RegisterCommand("dob", function(source, args, message)
    local player = Framework.getPlayer(source)
    if(player) then    
        TriggerClientEvent('chatMessage', player.src, player.dob)
    else 
        TriggerClientEvent('chatMessage', source, "You are on in the framework")
    end
end)
```

</details>

<details>

<summary>Framerwork.getDiscord()</summary>

There are two ways you can get someones discord. If they are logged in the framework. Use the Framework.getPlayer() otherwise Framework.getDiscord(). Here is an example

```lua
RegisterCommand('discord', function(source, args, message) 
    local player = Framework.getPlayer(source)
    -- If the player isn't online in the framework it will use the native way.
    if(player) then    
        TriggerClientEvent('chatMessage', player.src, player.discord)
    else
        local discord = Framework.getDiscord(source)
        if(discord) then
            TriggerClientEvent('chatMessage', source, discord)
        else     
            TriggerClientEvet('chatMessage', source, "Your discord isnt linked")
        end
    end 
end)
```

</details>

<details>

<summary>Framework.getSteam()</summary>

There are two ways you can get someones discord. If they are logged in the framework. Use the Framework.getPlayer() otherwise Framework.getSteam(). Here is an example:&#x20;

```lua
RegisterCommand('steam', function(source, args, message) 
    local player = Framework.getPlayer(source)
    -- If the player isn't online in the framework it will use the native way.
    if(player) then    
        TriggerClientEvent('chatMessage', player.src, player.steam)
    else
        local steam = Framework.getSteam(source)
        if(steam) then
            TriggerClientEvent('chatMessage', source, steam )
        end
    end 
end)
```



</details>

<details>

<summary>Framework.checkAdmin()</summary>

To check if a user is an admin is very simple. This will also check if they are logged into the framework. here is an exmaple

```lua
RegisterCommand('checkadmin', function(source, message, args) 
    if(Framework.checkAdmin(source) then    
        TriggerClientEvent('chatMessage', source, "you are an admin your cool")
    else 
        TriggerClientEvent('chatMessage', source, "You are not an admin")
    end
end)
```



</details>

<details>

<summary>Framework.extractIdentifier()</summary>

Very usful function to extract all a players identifiers. Below a simple way to display someones identifier. Please note this also grabs ips as well.

```lua
RegisterCommand("extract", function(source, args, message)
    local everything = Framework.extractIdentifier(source)
    print(json.encode(everything); -- display everything
    print(everything.discord); -- display users discord

end)
```

</details>
