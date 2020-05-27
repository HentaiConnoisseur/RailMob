
# Possibilities

With RailMob, creating custom monsters is now possible. Custom monsters can have a plethora of things added to them.

A list of things that can be done with RailMob

### PathfindingGoals

PathfindingGoals control the AI behind entities. In this plugin, you can add, remove, and change existing PathfindingGoals on Custom Monsters.

For example, you can create an aggressive Sheep, a Creeper that doesn't explode, an Enderman that doesn't get mad when stared at, and more.

### Minecraft Attributes/Custom Attributes

In addition to having the ability to customize Minecraft Attributes, you can also further customize Custom Monsters by using Custom Attributes.

Minecraft Attributes are the ones listed on this page [Minecraft Attributes](https://minecraft.gamepedia.com/Attribute#Attributes_available_on_all_living_entities)

As for Custom Attributes, you can look here: {}

### Spawn Conditions

When an Entity spawns, it will attempt to find a suited Custom Monster by searching through the Spawn Conditions of each Custom Monster. If an Entity matches the conditions for a Custom Monster, it will become that Custom Monster.

a list of Spawn Conditions can be found here: {}

### Monster Leveling

All Custom Monsters have levels. The distance per level is configurable in the configuration, and by default, is set to 30.

The equation is as follows: DISTANCE_FROM_SPAWN / 30 (default value)

Monster Levels can be used to scale the values of Minecraft Attributes and Custom Attributes.

As an example, you can set a GenericMaxHealthAttribute (a Minecraft Attribute) on a Custom Monster to increase the entity's health by 1 for every Monster level.

An example image: 

In this image, the Mimic Creeper is a level 58, has half a heart of health (fixed), does 2.0 damage, and has 0.0 armor.
![Example Image](https://i.imgur.com/eXSUWRh.png)


