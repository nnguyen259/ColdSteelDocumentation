# t_item.tbl
## EntryBody Structure
```
short   id
short   user_restriction
String  targeting_flags
short   category

byte    targetting_type
byte    targetting_range
byte    targettting_size

byte    effect1_id
short   effect1_data1
short   effect1_data2

byte    effect2_id
short   effect2_data1
short   effect2_data2

short   str
short   def
short   ats
short   adf
short   spd
short   acc
short   eva
short   mov
short   hp
short   ep

int     price
byte    stack_size
short   sort_id

short   quartz_unknown_bytes
short   unknow_bytes

String  name
String  description
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

### Stats

### Effects

### Unkowns

## Example