# Core

```
"name": "value"
```
Module Name referenced by the en.properties file and "flippedFrom" string. In-Game displays this name in red when no language value is applied.
***
```
"flippedFrom": "value"
```
Creates horizontally flipped variation of referenced "name".
***
```
"remove": true
```
Removes the specified "name" from the game.
***
```
"deriveFrom": "value"
```
Creates a replica of referenced "name". 
***
```
"patch": true
```
Marks that this module will only partially overwrite any file with the same "name", intead of completely overwriting it.
***
```
"categories": [ "value" ]
```
In-Game Editor Module Category. Setting this value blank will make the module valid without appearing in-game.

Can occupy multiple, or none.

Values: `BASIC` `STRUCTURAL` `LIFT` `PROPULSION` `RESOURCES` `COMMAND_AND_CREW` `WEAPONS` `TROOPS` `AIRCRAFT`
***
```
"required": "value"
```
Required technology, city, or charge bonus to build the module in Single Player.

See `Bonus/bonuses.json` for list of bonuses.
***
```
"providesBonus": "value"
```
When placed, gives the craft the specified bonus. Typically used to buff a craft stats by placing a module, using modded bonuses.

See `Bonus/bonuses.json` for list of bonuses.
***
```
"w": "value"
"h": "value"
```
Width and Height of the module.

Unit: Tiles
***
```
"isExplosive": true,
"isSail": true,
"isWeapon": true,
"isGun": true,
"isCannon": true,
"isRam": true
```
Specifies the module's property for AI logic.
***
```
"countsAsActiveCrew": true
```
Specifies the module acts as an active crew member, capable of performing module tasks without troops occupying the module, 
allowing interior vision of the module, and preventing defeat of the craft under certain conditions.
***
```
"instantlyDestroyed": true
```
Instantly removes the Module from the battle on destruction, allowing for animated or simplified death sequences from other connected Modules. 
Most often used on Monster Modules.
