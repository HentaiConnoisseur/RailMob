Note: 1 second = 20 ticks.

Values tagged with a * have a child Value which is added on top of their parent value. Child values are named after their parent values but with an 'IncreasePerLevel' text added on top. A few examples below:

BaseDamage becomes BaseDamageIncreasePerLevel for its child
BaseMaxFuseTicks becomes BaseMaxFuseTicksIncreasePerLevel for its child

and so on. The 'Input Type' remains the same for its child.

These 'IncreasePerLevel' child Values scale with the Custom Monsters level. (child Value * Custom Monster Level)


## ForeverBurningAttribute

When applied, the Custom Monster will constantly be on fire, even when it's raining or in water.

This Attribute has no customizable values.

##  DamagedByWaterAttribute

When applied, the Custom Monster will be damaged when in water.

#### BaseDamage (*)
* Input Type: Double
* The base amount of damage this Custom Monster will take in water
## ZombieModificationAttribute

Applies to: Zombie, Drowned, Husk, PigZombie, ZombieVillager

When applied, the input values will be changed on the Custom Monster.

#### ConversionTimeValue (*)
* Input Type: Double
* The amount of ticks until this Custom Monster will be converted to a Drowned as a result of being underwater
## CreeperModificationAttribute

Applies to: Creeper

When applied, the input values will be changed on the Custom Monster.

#### BaseMaxFuseTicks (*)
* Input Type: Integer
* The maximum fuse ticks for this Custom Monster, where the maximum ticks is the amount of time in which a creeper is allowed to be in the primed state before exploding
#### BaseExplosionRadius (*)
* Input Type: Integer
* Set the explosion radius in which this Custom Monster's explosion will affect
#### IsPowered
* Input Type: Boolean
* Sets whether this creeper is powered or not
### FireAuraAttribute

When applied, the Custom Monster will produce fire in a set radius, that removes on a fixed duration.

#### RemovalTime (*)
* Input Type: long
* The time in milliseconds in which the produced fire removes in
#### RadiusX (*)
* Input Type: integer
* The x radius of the produced fire
#### RadiuxZ (*)
* Input Type: integer
* The z radius of the produced fire
#### SpawnChance (*)
* Input Type: double
* Each produced fire block will check this chance, and if it passes, the fire will spawn, else nothing will happen. This allows for a more random fire pattern.
### Generic'X'Attribute



<details><summary>Replace 'X' with any of the following (case-insensitive)</summary>
<p>

ARMOR	
Armor bonus of an Entity.<p>
ARMORTOUGHNESS	
Armor durability bonus of an Entity.
ATTACKDAMAGE	
Attack damage of an Entity.
ATTACKSPEED	
Attack speed of an Entity.
FLYINGSPEED	
Flying speed of an Entity.
FOLLOWRANGE	
Range at which an Entity will follow others.
KNOCKBACKRESISTANCE	
Resistance of an Entity to knockback.
LUCK	
Luck bonus of an Entity.
MAXHEALTH	
Maximum health of an Entity.
MOVEMENTSPEED	
Movement speed of an Entity.
HORSEJUMPSTRENGTH	
Strength with which a horse will jump.
ZOMBIESPAWNREINFORCEMENTS	
Chance of a zombie to spawn reinforcements.

</p>
</details>
