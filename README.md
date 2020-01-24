# Oxide.Ext.RustEdit
An Oxide extension to allow further customisation in Rust maps

You can find the map editor at [rustedit.io](https://www.rustedit.io "rustedit.io")

**To Install**

You must have Oxide/uMod installed on your server to make use of the extension

Copy the Oxide.Ext.RustEdit.dll to your */serverroot/RustDedicated_Data/Managed* folder and restart your server

**Features**
* Establishes IO connections made in the editor
* Populates custom loot containers and ensures they respawn/refresh loot at the rates set in the associated loot profile
* Creates spawn handlers for all loot containers placed in the editor without a loot profile so they respawn/refresh loot at default rates
* Creates spawn handlers for all resource entities placed in the editor so manually placed resources will respawn
* Creates spawn handlers for all junk piles placed in the editor so manually placed junk piles will respawn
* Populates custom vending machines using the vending profile associated with them in the editor
* Overrides OceanPatrolPath generation with a custom path created in the editor
* Creates and manages custom APC paths created in the editor
* Fixes the spawn point prefab and ensures players will only spawn on them
* Updates itself automatically

**Chat Commands**
* All chat commands require that the player running them has admin privileges
* /rustedit - Show all available chat commands
* /rustedit.spawns.show <opt:time> - Show all current custom spawn points
* /rustedit.ocean.show <opt:time> - Show custom ocean patrol path points
* /rustedit.vending.restock - Re-stock the vending machine you are looking at with a random selection of items from the vending profile

**Console Commands**
* Console commands run via in-game console require the player running them has admin privileges. Console commands can also be run via rcon
* rustedit - Show all available console commands
* rustedit.apc.status - Show the current status of custom APCs
* rustedit.apc.killall - Kill all custom APCs
* rustedit.apc.respawn - Respawn all dead custom APCs
* rustedit.io.reset - Reset IO connections to what is stored in the map file
* rustedit.vending.restockall - Re-stock all map Vending Machines with a random selection of items from the vending profile
* rustedit.resource.respawnall - Force spawn all resources pending respawn
* rustedit.resource.info - Display a count of all map resources and their status
* rustedit.loot.respawnall - Force spawn all loot containers pending respawn
* rustedit.loot.info - Display a count of all map loot containers and their status
* rustedit.junkpile.respawnall - Force spawn all junk piles pending respawn
* rustedit.junkpile.info - Display a count of all map junk piles and their status

**Hooks**
* (void)RustEdit_NpcSpawned(BasePlayer) - Called when a NPC is spawned via a NPC spawner
