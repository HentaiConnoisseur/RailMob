Creating Custom Monsters is easy in RailMob.

Note: By retroactive, I mean changes are reflected in existing entities.
Note: Code-names and Custom Monsters are the same thing.

Custom Monsters go into the 'Mob' section of the Config.yml file located in the RailMob's data folder in the plugin folder of your server.

Any top-level section in the 'Mob' section is the Custom Monster's code-name. Any values/sections within that code-name apply to that Custom Monster only.

Code-names are important. In Railmob, a Custom Monster *is* solely identified from their code-name. Changing the code-name of an existing Custom Monster will cause any entities who identify by that code-name to revert to their original Minecraft state, for the most part. Certain things will not be reverted, such as PathfindingGoals and some Minecraft/Custom Attribute values.

A very basic Custom Monster with no PathfindingGoals and Attributes looks like this.

```yaml
Mobs:
 CustomEntity: // code-name (used to identify the monster in code)
  Name: 'Custom Entity' // actual in-game name
  ```

The 'Name' value is the entity's display name in-game. Color codes are supported. 

Note: The 'Name' value is retroactive.

Custom Monsters can have Spawn Conditions. All conditions must evaluate to true for an entity to become the Custom Monster.

Since the above entity has no conditions, all entities that spawn will become that Custom Monster.

The spawn conditions are as follows: SpawnChance (double), EntityType (string), MinLevel (integer), and MaxLevel (integer)

Here's an updated configuration with spawn conditions.

```yaml
MobsA:
   CustomEntity:
      Name: 'Custom Zombie' // new name
      SpawnConditions:
         SpawnChance: 0.5
         MinLevel: 0
         MaxLevel: 100
         EntityType: ZOMBIE
```

Note: Conditions are not retroactive. Once an entity meets the conditions for a Custom Monster, it will stay as that Custom Monster as long as the code-name remains the same.

With the above config, all zombies within level 0 to 100, have a 50% chance to become the Custom Monster, CustomEntity.

The Custom Monster, CustomEntity, still does nothing, and that's a shame. Let's add some Attributes to spice things up.

Attributes can be defined within a Custom Monster like so:

```yaml
MobsA:
   CustomZombie:
      Name: Potentially Strong Zombie // new name again!
      SpawnConditions:
         SpawnChance: 0.5
         MinLevel: 0
         MaxLevel: 100
         EntityType: ZOMBIE
      Attributes:
         0:
            Type: GenericMaxHealthAttribute
            BaseValue: 1
	    ValueIncreasePerLevel: 1
            AddBukkitDefaultValue: false
```

With the above config, all CustomZombie's will have a base health of BaseValue, and it increases per level by ValueIncreasePerLevel. The AddBukkitDefaultValue determines whether or not to add the entity's default health onto the BaseValue. In this case, we disable it because we do not want it.

The '0' top-level section in 'Attributes' can be anything as long as it's unique to the 'Attributes' section.

A list of Attributes can be found here: {}

Note: Most Attributes are retroactive.

TODO: PathfindingGoals
