# t_mstqrt.tbl
## Overview
t_mstqrt contains the data on all Master Quartz in the game. It has three different types of entries:
* MasterQuartzBase: General data about the Master Quartz. 
* MasterQuartzData: Data for each Master Quartz level.
* MasterQuartzMemo: Master Quartz texts.

## MasterQuartzBase
### EntryBody Structure
```
short   item_id
short   sort_id
short   starting_level
```
### EntryBody Details
Each Master Quartz has an item representation in t_item.tbl and the `item_id` points to that item. They are also sorted by their `sort_id`, with smaller goes on top.

Finally, the starting level will determine how many entries of MasterQuartzBase there are, with the formula being:
```
(5 - starting_level) + 1
```

## MasterQuartzData
### EntryBody Structure
```
short       item_id
short       level

short[7]    stats
float[6]    effects_power

short[2]    arts_gain
short[9]    memo_ids
```

### EntryBody Details
`item_id` once again points to the item in t_item.tbl, while `level` depicts the level of the Master Quartz this entry represents.

`stats` are the bonus stats the Master Quartz gives. They are in the following order: HP, EP, STR, DEF, ATS, ADF, SPD.

`effects_power` determine how powerful the Master Quartz effects are. Note that we can only change the power, not the actual effects. -1 is used when no number is needed.

Each level of Master Quartz can give up to two arts. They use the same art id as in the t_magic.tbl. Otherwise, -1 is used.

Finally, `memo_ids`. They determine which text will be displayed for the Master Quartz. The nine memos are in three sets of three, with one set per effect. The first one is the title, and the other two are details. If there is no need for a text, -1 is used instead of the `memo_id`

The number of filled in `memo_ids` will determine how many MasterQuartzMemo there are.

## MasterQuartzMemo
### EntryBody Structure
```
short   item_id
short   memo_id
String  text
```

### EntryBody Details
`item_id` points to the item in t_item.tbl, while `memo_id` is the id of the text, which is referenced to in MasterQuartzData.

`text` is the content of the memo, and will be displayed in game.