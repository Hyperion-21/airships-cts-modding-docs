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
How inaccurate the module is, before compensating `jitterMerge`.

Unit: "Standard deviation in tiles per pixel" (src: [zark modding guide](http://www.zarkonnen.com/airships/modding_guide))
***

```
"jitterMerge": value
```
How "precise" the weapon is. See image for an example. 0 means shots are completely random, 1 means shots are clustered.

![image](https://user-images.githubusercontent.com/69665635/142752839-9121201a-653d-46b4-bbd0-2c9f2deef87d.png)
*img credit: St. Olaf Collede*

Equation:

![image](https://user-images.githubusercontent.com/69665635/142753254-d9b81899-5e40-4941-b311-18a1e271375c.png)
![image](https://user-images.githubusercontent.com/69665635/142753288-d0ec8219-ffca-46c5-858d-2363776c4bea.png)

With bonuses being, for example, accuracy bonuses from modules, or fog (3x) and light/dark (2x).
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
