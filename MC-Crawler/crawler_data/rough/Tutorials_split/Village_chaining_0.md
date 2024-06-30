# Tutorials/Village chaining
Village chaining is the process by which one can move village centers abnormally close to, or within, each other. This is a process that is commonly used in making highly efficient and compact iron farms. It was first discovered in Java Edition 1.4.2, and has been used till Java Edition 1.13.2. The process was originally discovered and introduced to the majority by TangoTek.

## Contents
- 1 Classifications
	- 1.1 Non-Concentrical and Concentrical
		- 1.1.1 Comparing the non-concentrical version to the concentrical version
	- 1.2 Non-Resettable and Resettable
- 2 Game mechanics and mechanisms used in village chaining
	- 2.1 Village merging priority & Border extender
		- 2.1.1 Border extender
	- 2.2 Properties of the village center & Center anchor
		- 2.2.1 Center anchor
	- 2.3 One villager in multiple villages
	- 2.4 House detection mechanics & Layered chained village + Keeping doors detected + Undetecting a door
		- 2.4.1 Layered chained village + Keeping doors detected + Undetecting a door
	- 2.5 The downward preference

## Classifications
### Non-Concentrical and Concentrical
Non-concentrical chained villages are the first to be discovered. Their component villages' centers is usually arranged on a line and are not put in the same position.

On the other hand, concentrical chained villages are discovered much later. They have all component villages' centers in the exact same spot.

#### Comparing the non-concentrical version to the concentrical version
- Pros
	- Easier and simpler to create.
- Cons
	- Less space-efficient.
	- Require a whole lot moredoorplacing andbreakingif it is non-resettable, and a lot more doors if it's auto-resettable.
	- Require more villagers.

### Non-Resettable and Resettable
Because even the quickest reloading of chunks (usually done in autosaving, and affects most kind of chunk loaders) will basically wipe all villages data in those chunks and recalculate everything, chunks containing chained villages must never unload as long as the game is open, or else the whole thing will merge.

The solution to this is either putting the whole chained village in spawn chunk or its equivalent, then use a little trick to continue loading the chunks even when no player is in the same dimension as it (the non-resettable solution), or use redstone to rechain the village whenever the player needs (the resettable solution).

The resettable solution is primarily used when chunk permaloading cannot be achieved (for example in a Spigot server), or when the chaining process is so complex it cannot be done manually (such as in concentrical chained villages).

## Game mechanics and mechanisms used in village chaining
Note:
1. Before getting to the advanced, please visit the tutorial on village mechanics first to learn the basics.

2. Mechanisms discussed in this section are for Java Edition 1.8 and above only, however game mechanics discussion are for all versions that have villages.

3. To prevent itself from being unnecessarily long or wide, figures in this section use planks and fences to represent valid door positions and village radius, respectively. Side-view log represents a village center that contains a valid door, while top-view log represents a door-less center. The barrier icons just represent unimportant things. More important icons may overlay less important ones. The minimum village radius in those figures is 5 blocks and the merging range is radius + 5 blocks instead of 32 blocks and radius + 32 blocks like the real game.

### 
If all the chunks containing villages are not reloaded, village merging will only be considered when a villager detects new doors (technically only the bottom block of the door is counted). If there are multiple villages in range, only the most eligible village to merge with a door will get merged with it. All the other in-range villages are ignored. Thus, villages with overlapping boundaries are possible.

Before 1.8, the older a village is the more eligible it is to merge with a new village. Consequently, village chaining back then primarily used the merging range to prevent villages from merging initially. After 1.8, however, the nearer a village to a door the more eligible it is to merge with the door. If multiple villages have the same distance between their centers and a door, the door will prefer the older village more. This makes village chaining tougher, but also much more predictable, allowing a village to extend from a far spot to overlapping with a preexisting village. It also doesn't break chained villages from older versions as long as it is kept loaded, but old reset mechanisms no longer work.

#### Border extender
Initial State








































































































































































































































































The beginning of the 1st chaining cycle








































































































































































































































































The end of the 1st chaining cycle








































































































































































































































































2nd chaining cycle begins








































































































































































































































































2nd chaining cycle ends








































































































































































































































































3rd chaining cycle starts








































































































































































































































































3rd chaining cycle ends








































































































































































































































































4th chaining cycle begins








































































































































































































































































4th chaining cycle ends









































































































































































































































































The process of making village boundaries overlap, with the oak village getting closer and closer to the birch village each chaining cycle, until it cannot get any closer with this method. The oak village is created first, thus the game prefers it over the birch village. Note the rounding that shifted the center to the west. This is also almost exactly the same way TangoTek chained villages in his Iron Titan.

The village border extender is a valid house that, as the name suggests, extends the border of a village so that the center is closer to the center of another village. The extender should always be placed as close as possible to the other village, but must still be closer to the village that needs extension. After that, the further door(s) to the other village's center is removed, so that the extender becomes the center of the village, allowing it to use another extender to continue the process until it cannot get any closer with this method. After the extended village has reached that spot, more doors can be added to it & the other village so they both have enough doors to spawn iron golems.
