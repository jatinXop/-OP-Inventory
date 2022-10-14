
## Credits:
>### JATIN OP - Op-inventory

# How to install Op-inventory
* Download source files from github
* Drag source files into your resources folder
* Rename folder from `qb-inventory-withdecay-main` to `qb-inventory`



```lua
["created"] = nil
["decay"] = 28.0 -- for 28 days
```

### REPLACE ADDITEM EVENT
```lua
TriggerServerEvent("QBCore:Server:AddItem, item, 1)
```

### TO
```lua
exports['op-inventory']:toggleItem(1, itemName, 1)
```

### REPLACE REMOVEITEM EVENT
```lua
TriggerServerEvent("QBCore:Server:RemoveItem, item, 1)
```

### TO
```lua
exports['op-inventory']:toggleItem(0, itemName, 1)
```


### REPLACE HASITEM CALLBACK
```lua
QBCore.Functions.TriggerCallback('QBCore:HasItem', function(result)
        if hasitem then
              -- Has Item
        end
end, "sandwich")
```

### TO
```lua
      if QBCore.Functions.HasItem("sandwich") then
             -- Has Item
      end
```
