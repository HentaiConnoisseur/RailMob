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

* ARMOR
  * Armor bonus of a Custom Monster.
  
* ARMORTOUGHNESS
  * Armor durability bonus of a Custom Monster.
  
* ATTACKDAMAGE
  * Attack damage of a Custom Monster.
  
* FLYINGSPEED (parrots only)
  * Flying speed of a Custom Monster.
  
* FOLLOWRANGE
  * Range at which a Custom Monster will follow others.
  
* KNOCKBACKRESISTANCE
  * Resistance of a Custom Monster to knockback.
  
* MAXHEALTH
  * Maximum health of a Custom Monster.
  
* MOVEMENTSPEED
  * Movement speed of a Custom Monster.
  
* HORSEJUMPSTRENGTH (horse only)
  * Strength with which a Custom Monster will jump.
  
* ZOMBIESPAWNREINFORCEMENTS (zombie only)
  * Chance of a Custom Monster to spawn reinforcements.
</p>
</details>

to change the Minecraft Attribute on a Custom Monster

#### BaseValue (*)
* Input Type: Double
* The Attribute's base value on the Custom Monster.
#### AddBukkitDefaultValue
* Input Type: Boolean
* If set to false, the default value for this Attribute will not be added on to the BaseValue

### GenericInflict'X'Attribute

Note: This even works for creeper explosions, and entity projectiles!

<details><summary>Replace 'X' with any of the following (case-insensitive)</summary>
<p>

* ABSORPTION	
  * Increases the maximum health of an entity with health that cannot be regenerated, but is refilled every 30 seconds.
* BAD_OMEN	
  * oof.
* BLINDNESS	
  * Blinds an entity.
* CONDUIT_POWER	
  * Effects granted by a nearby conduit.
* CONFUSION	
  * Warps vision on the client.
* DAMAGE_RESISTANCE	
  * Decreases damage dealt to an entity.
* DOLPHINS_GRACE	
  * Squee'ek uh'k kk'kkkk squeek eee'eek.
* FAST_DIGGING	
  * Increases dig speed.
* FIRE_RESISTANCE	
  * Stops fire damage.
* GLOWING	
  * Outlines the entity so that it can be seen from afar.
* HARM	
  * Hurts an entity.
* HEAL	
  * Heals an entity.
* HEALTH_BOOST	
  * Increases the maximum health of an entity.
* HERO_OF_THE_VILLAGE	
  * \o/.
* HUNGER	
  * Increases hunger.
* INCREASE_DAMAGE	
  * Increases damage dealt.
* INVISIBILITY	
  * Grants invisibility.
* JUMP	
  * Increases jump height.
* LEVITATION	
  * Causes the entity to float into the air.
* LUCK	
  * Loot table luck.
* NIGHT_VISION	
  * Allows an entity to see in the dark.
* POISON	
  * Deals damage to an entity over time.
* REGENERATION	
  * Regenerates health.
* SATURATION	
  * Increases the food level of an entity each tick.
* SLOW	
  * Decreases movement speed.
* SLOW_DIGGING	
  * Decreases dig speed.
* SLOW_FALLING	
  * Slows entity fall rate.
* SPEED	
  * Increases movement speed.
* UNLUCK	
  * Loot table unluck.
* WATER_BREATHING	
  * Allows breathing underwater.
* WEAKNESS	
  * Decreases damage dealt by an entity.
* WITHER	
  * Deals damage to an entity over time and gives the health to the shooter.
* FIRE
  * Inflicts fire
</p>
</details>

to have that effect apply on the entity

#### BaseDuration (*)
* Input Type: Long
* How long the effect will last on the attacked entity in ticks.
#### BaseAmplifier (*) (Applies to all but 'FIRE')
* Input Type: Integer
* The level of the effect.

### Generic'X'DamageReductionAttribute

<details><summary>Replace 'X' with any of the following (case-insensitive)</summary>
<p>

* BLOCK_EXPLOSION	
  * Damage caused by being in the area when a block explodes.
* CONTACT	
  * Damage caused when an entity contacts a block such as a Cactus.
* CRAMMING	
  * Damage caused when an entity is colliding with too many entities due to the maxEntityCramming game rule.
* CUSTOM	
  * Custom damage.
* DRAGON_BREATH	
  * Damage caused by a dragon breathing fire.
* DROWNING	
  * Damage caused by running out of air while in water
* DRYOUT	
  * Damage caused when an entity that should be in water is not.
* ENTITY_ATTACK	
  * Damage caused when an entity attacks another entity.
* ENTITY_EXPLOSION	
  * Damage caused by being in the area when an entity, such as a Creeper, explodes.
* ENTITY_SWEEP_ATTACK	
  * Damage caused when an entity attacks another entity in a sweep attack.
* FALL	
  * Damage caused when an entity falls a distance greater than 3 blocks
* FALLING_BLOCK	
  * Damage caused by being hit by a falling block which deals damage
* FIRE	
  * Damage caused by direct exposure to fire
* FIRE_TICK	
  * Damage caused due to burns caused by fire
* FLY_INTO_WALL	
  * Damage caused when an entity runs into a wall.
* HOT_FLOOR	
  * Damage caused when an entity steps on Material.MAGMA_BLOCK.
* LAVA	
  * Damage caused by direct exposure to lava
* LIGHTNING	
  * Damage caused by being struck by lightning
* MAGIC	
  * Damage caused by being hit by a damage potion or spell
* MELTING	
  * Damage caused due to a snowman melting
* POISON	
  * Damage caused due to an ongoing poison effect
* PROJECTILE	
  * Damage caused when attacked by a projectile.
* STARVATION	
  * Damage caused by starving due to having an empty hunger bar
* SUFFOCATION	
  * Damage caused by being put in a block
* SUICIDE	
  * Damage caused by committing suicide using the command "/kill"
* THORNS	
  * Damage caused in retaliation to another attack by the Thorns enchantment.
* VOID	
  * Damage caused by falling into the void
* WITHER	
  * Damage caused by Wither potion effect
</p>
</details>

to reduce the damage of that specific cause.

#### Reduction (*)
* Damage Reduction (currentDamage * Reduction) where 0 Reduction is 100% and 1 is 0%

### GenericEquipment'X'Attribute

<details><summary>Replace 'X' with any of the following (case-insensitive)</summary>
<p>

* HELMET
  * The Custom Monster's helmet
* CHESTPLATE
  * The Custom Monster's Chestplate
* LEGGINGS
  * The Custom Monster's Leggings
* BOOTS
  * The Custom Monster's Boots
* MAINHAND
  * The Custom Monster's Mainhand
* OFFHAND
  * The Custom Monster's Offhand
</p>
</details>

to set the Custom Monster's equipment piece

## DropChance (*)
* Input Type: Double
* The chance at which this equipment piece will drop. Where 0 is 0% and 1 is 100%
## RegistryItem
* Input Type: String
* The input value must match an ItemStack in the ItemRegistry. To register an item, use /itemregistry or /ir in-game.
