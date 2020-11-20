# t_magic.tbl
## Overview
t_magic contains the information on all commands, arts and crafts in battle.

## EntryBody Structure
```
short       id
short       character_restriction
String      targetting_flags

short       category
short       type
short       element

short       targetting_type
short       targetting_range
short       targetting_size

Effect[2]   effects

byte        cast_delay
byte        recovery_delay
short       cost
byte        unbalance_bonus
byte        level_learn

short       sort_id

String      name
String      description
```
## EntryBody Details
List details as needed.

## Example
Add example as needed.