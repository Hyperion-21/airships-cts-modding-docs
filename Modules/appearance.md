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
