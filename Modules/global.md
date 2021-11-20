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

Unit: Miliseconds
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

Unit: Miliseconds
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
