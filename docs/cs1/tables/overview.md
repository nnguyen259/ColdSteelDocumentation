# Tables Overview

## General Structure
``` java
short       entry_num
List<Entry> entries
```

`entry_num` shows the number of entries the table file has. Although the number of entries in entry_num can be different from the actual amount of entries, it is encouraged to keep these two in sync to allow for easier access with program later.

## Entry
``` java
String      entry_title
short       entry_length
EntryBody   entry_body
```

Every Entry starts with an `entry_title`, which is followed immediately by an `entry_length`, which shows how long the `entry_body` is. As with `entry_num` earlier, `entry_length` can mismatch with the actual body length. However, by keeping them in sync, future program can make access to these files a lot easier.