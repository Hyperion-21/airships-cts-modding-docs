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
"w": value
"h": value
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
***

# Appearance

```
"appearance": {
    "src": "value"
```
The name of the `SpritesheetBundle` to use as a spritesheet.
***

```
"appearance": {
    "x": value,
    "y": value,
    "w": value,
    "h": value
```
The area on the spritesheet to pull textures from.

Unit: Tiles
***

```
"appearance": {
    "interval": value
```
When `frames` is present, is the time between frames.

Unit: Milliseconds
***

```
"appearance": {
    "frames": [
        { "x": value, "y": value, "w": value, "h": value },
        { "x": value, "y": ...
```
Animates the module, going from top to bottom, then looping. Each frame defines the area on the spritesheet to pull textures from.

Unit: Tiles
***

```
"externalAppearance": {
    "x": value, "y": value,
        "appearance": { "src": "value", "x": value, "y": value, "h": value }
```
Exterior graphics of the module. `x` and `y` represent the position on the module to place the `appearance`.

There is also `damagedExternalAppearances` and `destroyedExternalAppearance`.

Unit: Tiles
***

```
"windows": [
    { "x": value, "y": value, "w": value, "h": value },
    { "x": value, "y": ...
```
Places windows on the module.

Unit: Tiles
***

```
"hasGenericDestructionFragments": false
```
Removes generics explosive fragments that appear when a module is damaged/destroyed. Often used with with `damagedExternalAppearances` and `destroyedExternalAppearance`.
***

```
"hitParticle": "value"
```
The particle the module creates when hit.

See `ParticleType/` for list of particles.
***

```
"destructionLength": value
```
Duration of a modules destruction, before being removed from battle.

Unit: Milliseconds
***

```
"destructionParticle": "value"
```
Particle(s) created when the module is destroyed.
***

```
"destructionParticleDensity": value
```
Particle density of `destructionParticle` value.
***

### Incomplete, needs testing:
```
"fragmentsSpeedMult": value,
"fragmentsFireMult": value,
"fragmentsDensity": value
```
***

# Structure

```
"frontOnly": true,
"backOnly": true,
"topOnly": true,
"bottomOnly": true
```
The module cannot have another module intersect with any other module in the specified direction.
***

```
"frontOnlyList": [ value ],
"backOnlyList": [ value ],
"topOnlyList": [ value ],
"bottomOnlyList": [ value ]
```
The module cannot have another module intersect with any other module in the specified direction, but only on the listed values.

Starts from the top-left corner.
***

```
"upDoors": [ value ],
"leftDoors": [ value ],
"rightDoors": [ value ]
```
Specifies which edges of the module have doors. 

Starts from the top-left corner.

Note that there is no `bottomDoors` string.
***

```
"canOccupy": [
    { "x": value, "y": value },
    { "x": value, "y": ...
```
Determines which tiles crew can occupy.

Starts from the top-left corner.
***

# Resource

```
"external": true
```
Specifies if the module cannot be protected by armor. Removes all armor effects, including graphics.
***

```
"armorType": "value"
```
Forced/Built-In armor Type for the module. String is often used with monsters and hatches, where the armor is invisible or subjective.
***

```
"hp": value
```
The module's total hit-points; before adjacency, bonuses and armor.
***

```
"explodeHP": value
```
HP required before the module chances explosion; before adjacency, bonuses and armor.
***

```
"explodeDmg": value
```
Blast damage inflicted by the module to surrounding modules when destroyed. Does not affect other vehicles.

Equation provided by Zarkonnen:

![Untitled](https://user-images.githubusercontent.com/69665635/142716046-936b21b8-9951-4e6a-a46a-87ede051e5f6.png)
***

```
"fireHP": value
```
HP required to chance engulfing the module in fire.
***

```
"destroyedHP": value
```
HP required before the module is destroyed. Often used for monsters, where this value indicates a specific HP.
***

```
"collisionDamageReceivedMult": value
```
Damage multiplier against the module on collision with another object.
***

```
"destroyEntireShipOnDestruction": true
```
Destroys the entire craft on destruction of the module.
***

```
"moveDelay": value
```
Time it takes for personnel to travel through the module. For most modules, this is 800.
***

```
"weight": value
```
Weight of the module.

Equation unknown.
***

```
"cost": value
```
Cost of the module. This does not factor in armor.
***

```
"coal": value
```
How much coal the module holds.
***

```
"coalReload": value
```
Time before the module needs to be re-supplied with coal.

Unit: Milliseconds
***

```
"command": value
```
How much command the module generates. Higher means faster commands.

Equation provided by Zarkonnen:

![image](https://user-images.githubusercontent.com/69665635/142716537-8016a315-1e68-42a3-a2a9-5d74f2de722c.png)
***

```
"lift": value
"propulsion": value
```
How much lift/propulsion the module generates.

Equations unknown.
***

```
"supplyProvided": value,
"ammo": value,
"water": value
```
How much supply/ammo/water the module generates.
***

```
"structuralStressAmount": value
```
Structural Integrity the module adds or removes; can be a negative number, lessening the structural integrity penalty.
***

```
"sickbay": value
```
How many personel that can heal in the module at any given time.
***

```
"shipHPBonus": value
```
How much bonus HP the module provides to attached modules.
***

```
"adjacencyBonusStrength": value
```
Additional HP provided through adjacency with another module.
***

```
"accuracyBonus": value
```
Accuracy bonus the Module provides, against deviation.
***

```
"preventsBoarding": true
```
Prevents boarding of the craft, until the module is destroyed.
***

```
"crew": value
```
Number of sailors required for the module to function.
***

```
"recommendedCrew": value
```
Recommended number of sailors for the module to function properly. For example; an additional sailor to deliver ammunition or coal.
***

```
"optionalCrew": value
```
Number of sailors populating the module if no other higher priority module exists.
***

```
"hangarPositions": [
    { "x": value, "y": value },
    { "x": value, "y": ...
```
Positions troops take within the module. Most often seen on aircraft modules.
***

```
"fixedGuards": value
```
Number of guards required to protect the module.
***

```
"recommendedGuards": value
```
Number of guards recommended to protect the module.
***

```
"maintenanceCost" value
```
Maintenance cost of the module, applies against income in single player.
***

```
"quartersType": "value"
```
Troops the module houses.

Values: `sailor` `soldier` `marine` `grenadier` `guard` `arachnid` `pirate` `pirate_raider` `air_hussar` `triplane` `bomber` `biplane` `air_dragoon` `guardian_sprite` `wolf_spider` `black_widow_spider` `mech_spider` `susp_bee` `clockwork_wasp`
***

```
"quarters": value
```
Number of personnel `quartersType` generates.
