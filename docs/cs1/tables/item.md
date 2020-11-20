# t_item.tbl
## Overview
t_item.tbl contains information for every item in the game.

## EntryBody Structure
```
short       id
short       user_restriction
String      behaviour_flags
short       category

byte        targetting_type
byte        targetting_range
byte        targettting_size

Effect[2]   effects

short[10]   stats

int         price
byte        stack_size
short       sort_id

short       quartz_unknown_bytes
short       unknow_bytes

String      name
String      description
```
## EntryBody Details
### ID, Category, Restriction, and Misc...
* **ID**: The item's unique identification in the game. Each item will have one and they are unique.
* **Sort ID**: The ordering of items in inventory tabs. Lower Sort ID will be higher in the inventory.
* **Category**: Determine the inventory tab the item is in.
* **Restriction**: Determine who can use the item.
* **Price**: The cost of the item when buying in shops as well as the sell price, which is half the price.
* **Stack Size**: How many copies of an item can be carried in the inventory at the same time.


### Targetting
* Targetting Type: How the target is selected.
* Targetting Range: How far from the player that a target can be selected.
* Targetting Size: The size of the area of effect when the item is used.

### Stats
Stats are added to the items in the following order: STR, DEF, ATS, ADF, SPD, ACC, EVA, MOV, HP, EP.

### Effects
```
byte    effect_id
short   data1
short   data2
```
* Effect ID: Influence the effect the item will have. There are limitations on which effect is possible possibly depends on the item's category.
* Effect Data: Each effect can have 0-2 additional data attached to it. Some data are optional, while some are not.

List of Effect ID and Data will be coming in the future.

### Unkowns
* Behaviour Flag: Affect how the item behave in and out of battle. The exact behaviour is still unknown.
* Quartz Specific Bytes: Only quartz have value, but still unsure what they mean.
* Unknown Bytes: Right before the item name. Not sure what they represent.

## Example