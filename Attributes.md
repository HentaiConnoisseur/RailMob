Note: 1 second = 20 ticks.
Note: 

## ForeverBurningAttribute

When applied, the Custom Monster will constantly be on fire, even when it's raining or in water.

This Attribute has no customizable values.

##  DamagedByWaterAttribute

When applied, the Custom Monster will be damaged when in water.

#### BaseDamage
* Input Type: Double
* The base amount of damage this Custom Monster will take in water
#### DamageIncreasePerLevel
* Input Type: Double
* Increases per level by the input value then applies it to BaseMaxFuseTicks

## ZombieModificationAttribute

Applies to: Zombie, Drowned, Husk, PigZombie, ZombieVillager

When applied, the input values will be changed on the Custom Monster.

#### ConversionTimeValue
* Input Type: Double
* The amount of ticks until this Custom Monster will be converted to a Drowned as a result of being underwater
## CreeperModificationAttribute

Applies to: Creeper

When applied, the input values will be changed on the Custom Monster.

#### BaseMaxFuseTicks
* Input Type: Integer
* The maximum fuse ticks for this Custom Monster, where the maximum ticks is the amount of time in which a creeper is allowed to be in the primed state before exploding
#### MaxFuseTicksIncreasePerLevel
* Input Type: Integer
* Increases per level by the input value then applies it to BaseMaxFuseTicks
#### BaseExplosionRadius
* Input Type: Integer
* Set the explosion radius in which this Custom Monster's explosion will affect
#### ExplosionRadiusIncreasePerLevel
* Input Type: Integer
* Increases per level by the input value then applies it to BaseExplosionRadius
#### IsPowered
* Input Type: Boolean
* Sets whether this creeper is powered or not
### FireAuraAttribute

When applied, the Custom Monster will produce fire in a set radius, that removes on a fixed duration.

#### RemovalTime
* Input Type: long
* The time in milliseconds in which the produced fire removes in
#### RadiusX
* Input Type: integer
* The x radius of the produced fire
#### RadiuxZ
* Input Type: integer
* The z radius of the produced fire
#### SpawnChance
* Input Type: double
* Each produced fire block will check this chance, and if it passes, the fire will spawn, else nothing will happen. This allows for a more random fire pattern.
