# Weapons

```
"hardness": value
```
The damage of the physical module in a collision scenario; intended for ramming.
***

```
"maxRange": value,
"minRange": value
```
Maximum/minimum range that the module must be from the target to fire the weapon.

Unit: Pixels
***

```
"maxXRange": value,
"minXRange": value
```
Maximum/minimum range horizontally that the module must be from the target to fire the weapon.

Unit: Pixels
***

```
"maxUpRange": value,
"minUpRange": value
```
Maximum/minimum range upwards that the module must be from the target to fire the weapon.
***

```
"maxDownRange": value,
"minDownRange": value
```
Maximum/minimum range downwards that the module must be from the target to fire the weapon.
***

```
"shotSpeed": value
```
How fast the shot travels its trajectory.

Unit: Tiles per millisecond
***

```
"shotSpeedVariation": value
```
Variation of `shotSpeed` for each Shot fired.

Unit: Tiles per millisecond
***

```
"reload": value
```
Time between shots.

Unit: Millisecond
***

```
"clip": value
```
Number of shots the module can fire before needing a reload.
***

```
"clipReloadTime": value
```
Time it takes to reload the weapon.

Unit: Milliseconds
***

```
"inaccuracy": value
```
How inaccurate the module is, before compensating for `jitterMerge`.

Equation:

![image](https://user-images.githubusercontent.com/69665635/142779806-53eb0c9c-48cd-47fb-860d-248798ba9997.png)
![image](https://user-images.githubusercontent.com/69665635/142779816-481ab848-d078-448b-b2db-d503b98b5ae9.png)

With bonuses being, for example, accuracy bonuses from modules, or fog (3x) and light/dark (2x).

If `jitterMerge` is present, the equation will only apply to the first shot.

Unit (for `firstShot` and `target`): Pixels
***

```
"jitterMerge": value
```
How "precise" the weapon is. See image for an example. 0 means shots are completely random, 1 means shots are clustered.

![image](https://user-images.githubusercontent.com/69665635/142752839-9121201a-653d-46b4-bbd0-2c9f2deef87d.png)
*img credit: St. Olaf College*

Equation for `jitterMerge`'d shots:

![image](https://user-images.githubusercontent.com/69665635/142779879-bf3a1389-443e-466c-abc2-adab1c9d6789.png)
![image](https://user-images.githubusercontent.com/69665635/142779891-2bc9c077-f6a2-41ae-b1d3-d2155411675e.png)

With bonuses being, for example, accuracy bonuses from modules, or fog (3x) and light/dark (2x).

Unit (for `nextShot`, `previousShot`, `target`): Pixels
***

```
"numShots": value
```
Number of projectiles in a single shot.
***

```
"multiShotJitter": value
```
Jitter designed for `numShots`. Most likely the same calculation as `jitterMerge`.
***

```
"blastDmg": value
```
Blast damage caused by the module's shots.
***

```
"blastSplashRadius": value
```
Radius of the area of damage after a shot hits the target.

Unit: Pixels
***

```
"penDmg": value
```
Penetration damage caused by the module's shots.
***

```
"directDmg": value
```
Direct damage dealt to the target module's HP, completely ignoring armor.
***

```
"shootTroopsRange": value
```
Specifies the Module can Target Troops and at what range. 

(Assumed in Pixels - measurement needed)
***

```
"fixedInaccuracyVsTroops": value
```
Fixed Inaccuracy against Troops. 

(Unknown if stacking with "innacuracy", unknown value measurement)
***

```
"recoilForce": value
```
Reverse propulsion caused by firing the Shot, in negative tile value.
***

```
"impactForce": value
```
Propulsion exerted on target, when hit by the module's shot.
***

```
"fireArc": { "direction": "value", "degrees": value }
```
Direction and arc the module is allowed to fire in.

Values: `up` `down` `forwards` `backwards`
***

```
"optimumRange": value
```
Distance from the module that is optimal for the weapon, for AI purposes.

Unit: Pixels

# Tether/Harpoon

```
"tetherSpec": {
    "color": { "r": value, "g": value, "b": value}
```
The color of the rope, in decimal RGB. 

Harpoon Gun uses `217, 203, 177`.
***

```
"tetherSpec": {
    "maxRange": value
```
Distance from the module the tether can reach.

Harpoon Gun uses `800`.

Unit: Pixels
***

```
"tetherSpec": {
    "tearForce": value
```
The amount of force required to break the tether.

Harpoon Gun uses `1.5`.

Unit: Unknown.
***

```
"tetherSpec": {
    "minLength": value
```
The minimum length of a tether, before it stops pulling.

Harpoon Gun uses `100`.

Unit: Pixels
***

```
"tetherSpec": {
    "shrinkSpeed": value
```
The speed the tether retracts.

Harpoon Gun uses `0.05`.

Unit: Unknown
***

```
"tetherSpec": {
    "k": value
```
The kinematic strength of the tether. Higher values increases the force the tether exerts on itself and its target.

At 0, the tether does nothing. Any value above 0.1 is not recommended.

Harpoon Gun uses `0.02`.
***

```
"tetherSpec": {
    "anchorX": value,
    "anchorY": value
```
The graphical location on the module to attach the tether to.

Unit: Tiles
***

```
"tetherSpec": {
    "width": value
```
The graphical width of the rope.

Harpoon Gun uses `1`.

Unit: Pixels
***

```
"tetherSpec": {
    "ripSound": "value",
    "ripParticle": "value"
```
The sound and particle, created when the tether is broken.

Harpoon Gun uses sound `rip` and particle `rope`.