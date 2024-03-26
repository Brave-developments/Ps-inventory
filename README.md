

<img width="420" alt="1111" src="https://github.com/Brave-developments/Ps-inventory/assets/89262662/c1a6d5f2-7cb8-44d7-9909-2389db1a43de">



# Project-Sloth's FiveM Inventory System

Reskinned by @Brotatochips11 - Discord: brotatochips11

## Overview

Project-Sloth's FiveM Inventory System is a complete redesign aimed to mimic the look and feel of the NoPixel 4.0 inventory system. This redesign enhances the user experience by offering a clean, intuitive interface while maintaining the core functionalities we've come to appreciate in the original lj-inventory system.

### Note
I removed the item images for simplicity during the update process. Please use your own item images to match the aesthetic and functionality of your server.

## Credits

- **loljoshie**: For creating the lj-inventory system.
- **ok1ez and the Project Sloth dev team**: For updating and maintaining lj-inventory as ps-inventory.
- **root_**: For implementing droppable items with their respective props.
- **The Project Sloth Community**: Your support has been invaluable to this release.

## Importing

For those who've used the previous version, I've included descriptions/tags above all UI changes for an easier transition. Below are code snippets for integrating new features without diving deep into the code inspection.

### Personal Information Snippet

#### Client-Side LUA

```lua
-- QBCore.Functions.TriggerCallback('inventory:server:ConvertQuality', function(data)
  inventory = data.inventory
  other = data.other
  SendNUIMessage({
  action = "open",
  inventory = inventory,
  slots = Config.MaxInventorySlots,
  other = other,
  maxweight = Config.MaxInventoryWeight,
  Ammo = PlayerAmmo,
  maxammo = Config.MaximumAmmoValues,
  Name = PlayerData.charinfo.firstname .." ".. PlayerData.charinfo.lastname .." - [".. GetPlayerServerId(PlayerId()) .."]", 
  pName = PlayerData.charinfo.firstname .. PlayerData.charinfo.lastname, 
  pNumber = PlayerData.charinfo.phone,
  pCID = PlayerData.citizenid,
  pID = GetPlayerServerId(PlayerId()),
})

QBCore.Functions.TriggerCallback('inventory:server:ConvertQuality', function(data)
  inventory = data.inventory
  other = data.other
  SendNUIMessage({
  action = "open",
  inventory = inventory,
  slots = Config.MaxInventorySlots,
  other = other,
  maxweight = Config.MaxInventoryWeight,
  Ammo = PlayerAmmo,
  maxammo = Config.MaximumAmmoValues,
  Name = PlayerData.charinfo.firstname .." ".. PlayerData.charinfo.lastname .." - [".. GetPlayerServerId(PlayerId()) .."]", 
  pName = PlayerData.charinfo.firstname .. PlayerData.charinfo.lastname, 
  pNumber = PlayerData.charinfo.phone,
  pCID = PlayerData.citizenid,
  pID = GetPlayerServerId(PlayerId()),
})
