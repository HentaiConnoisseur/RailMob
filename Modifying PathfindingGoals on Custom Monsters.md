Adding/removing PathfindingGoals on Custom Monsters is simple once you get the hang of it.

When removing or adding a PathfindingGoal on a Custom Monster, you must first specify the type of the PathfindingGoal.

There are 2 goal types of PathfindingGoals.

To figure out the goal type of the PathfindingGoal that you wish to add or remove, scroll down to 'Current PathfindingGoals' section

# Types

## Target

Used to find a target

## Goal

Used to do things such as floating, looking at players, walking, etc. Anything not target related.

# Fields

When adding a PathfindingGoal, you have to specify every field that PathfindingGoal has.

When removing a PathfindingGoal, you can specify the fields to match to avoid removing the wrong PathfindingGoal.

Fields for all of the current PathfindingGoals can be found in the 'Current PathfindingGoals' section

Learn how to use Fields in the sections below.

# Removing PathfindingGoals

```yaml
Mobs:
   ExampleMonster:
      Name: example
      PathfindingGoals:
         0:
            Mapping: PathfinderGoalFloatMapping
            Type: remove
            GoalType: GOAL
```


The above config will remove the PathfindingGoal, PathfinderGoalFloat, from the ExampleMonster, removing its ability to float.

```yaml
Mobs:
   ExampleMonster:
      Name: example
      PathfindingGoals:
         0:
            Mapping: PathfinderGoalAvoidTarget
            Type: remove
            GoalType: GOAL
            Fields:
             AvoidEntity: Ocelot
```

The above config will remove the PathfindingGoal, PathfinderGoalAvoidTarget, from the ExampleMonster matching the input AvoidEntity field, making it no longer afraid of ocelots.

# Adding PathfindingGoals

Every field of the PathfindingGoal must be input when adding. That means if a PathfindingGoal has 3 fields, you need to input a value for every one of those fields.

When a PathfindingGoal has no fields, you don't need to specify any fields.

```yaml
Mobs:
   ExampleMonster:
      Name: example
      PathfindingGoals:
         0:
            Mapping: PathfinderGoalAvoidTarget
            Type: add
            GoalType: GOAL
            Fields:
             AvoidEntity: Ocelot
             AvoidDistanceCheck: 6
             WalkSpeedModifier: 1.5
             SprintSpeedModifier: 1
```

The above config will add the PathfindingGoal, PathfinderGoalAvoidTarget, to ExampleMonster, with the specified fields.

```yaml
Mobs:
   ExampleMonster:
      Name: example
      PathfindingGoals:
         0:
            Mapping: PathfinderGoalFloat
            Type: add
            GoalType: GOAL
```

The above config will add the PathfindingGoal, PathfinderGoalFloat, to ExampleMonster. Since PathfinderGoalFloat has no fields, none are specified.

# Current PathfindingGoals

# PathfinderGoalFloat

Causes the CustomMonster to float on water.

## Fields
* This PathfindingGoal has no fields.

# PathfinderGoalAvoidTarget

Causes the CustomMonster to avoid the specified entity.

## Fields

### AvoidEntity
* Input Type: String
* The type of Entity to avoid. For a list of entities, see https://hub.spigotmc.org/javadocs/spigot/org/bukkit/entity/EntityType.html
### AvoidDistanceCheck
* Input Type: float
* The minimum distance the AvoidEntity has to be to start avoiding.
### WalkSpeedModifier
* Input Type: double
* The temporary walk speed multiplier for this entity, during the avoiding state.
### SprintSpeedModifier
* Input Type: double
* The temporary sprint speed multiplier for this entity, during the avoiding state.
