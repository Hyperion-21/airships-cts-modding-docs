# Tether/Harpoon

```
"tetherSpec": {
    "color": { "r": value, "g": value, "b": value}
```
The color of the rope, in decimal RGB. 

Harpoon Gun uses 217, 203, 177.
***

```
"tetherSpec": {
    "maxRange": value
```
Distance from the module the tether can reach.

Unit: Pixels
***

```
"tetherSpec": {
    "tearForce": value
```
The amount of force required to break the tether.

Unit: Unknown.
***

```
"tetherSpec": {
    "minLength": value
```
The minimum length of a tether, before it stops pulling.

Unit: Pixels
***

```
"tetherSpec": {
    "shrinkSpeed": value
```
The speed the tether retracts.

Unit: Unknown
***

```
"tetherSpec": {
    "k": value
```
The kinematic strength of the tether. Higher values increases the force the tether exerts on itself and its target.

At 0, the tether does nothing. Any value above 0.1 is not recommended.

Harpoon Gun uses 0.02
***

```
"tetherSpec": {
    "anchorX": value,
    "anchorY": value
```
The location on the module to attach the tether to.

Unit: Tiles
***

```
"tetherSpec": {
    "width": value
```
The width of the rope.

Unit: Pixels
***

```
"tetherSpec": {
    "ripSound": "value",
    "ripParticle": "value"
```
The sound and particle, created when the tether is broken.

Harpoon Gun uses sound `rip` and particle `rope`.