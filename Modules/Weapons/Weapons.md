# WIP FILE IGNORE THIS

hardness
The damage of the physical Module in a collision scenario; intended for ramming.

maxRange
Maximum Range in pixels that the module must be from the target to fire the weapon.

minRange
Minimum Range in pixels that the module must be from the target to fire the weapon.

XRange
Range in pixels horizontally that the module must be from the target to fire the weapon.

UpRange
Max Range in pixels that the Shot can reach vertically upwards.

DownRange
Max Range in pixels that the Shot can reach vertically downwards.

shotSpeed
How fast the Shot travels its trajectory in Tiles per millisecond.

shotSpeedVariation
Variation of shotSpeed for each Shot fired in Tiles per millisecond.

reload
Time in milliseconds between shots.

clip
Number of Shots the Module can fire before needing a reload.

clipReloadTime
Time it takes to reload the weapon, in milliseconds.

inaccuracy
How inaccurate the Module is, before compensating "jitterMerge".

jitterMerge

numShots
Number of projectiles in a single Shot. Only seen in the Grapeshot module.

multiShotJitter
[incomplete - calculation] Jitter designed for "numShots". Only seen in the Grapeshot module. In percentage, 0.0 being extremely inaccurate and 1.0 always firing the same direction.
In decimal, ex. #.#

blastDmg
Blast Damage caused by the Modules Shots.

blastSplashRadius
Radius of the widened area of damage after a Shot hits the Target, in Pixels.
Only seen accompanying "blastDmg".

penDmg
Penetration Damage caused by the Modules Shots.

directDmg
Direct Damage dealt to the Target Module, without Armour penalties.

shootTroopsRange
[incomplete - calculation] Specifies the Module can Target Troops and at what range. (Assumed in Pixels - measurement needed)

fixedInaccuracyVsTroops
[incomplete - calculation] Fixed Inaccuracy against Troops. (Unknown if stacking with "innacuracy", unknown Value measurement)

recoilForce
[incomplete - calculation] Reverse Propulsion caused by firing the Shot, in negative Tile value.
In decimal; ex. #.#

impactForce

fireArc
Direction and arc the Module fires.

optimumRange
Distance from the Module that is optimal for the weapon, indicating how the AI should react to the Module.
In pixels.
