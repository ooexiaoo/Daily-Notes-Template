---
name: Elon Musk
aliases:
  - Pro Memester
type:
  - Person
  - Friend
date-met: 2025-02-01
location: Texas
cover: https://pbs.twimg.com/profile_images/1874558173962481664/8HSTqIlD_400x400.jpg
cssclasses:
  - cards
banner: https://w.wallhaven.cc/full/j5/wallhaven-j5lqzq.jpg
banner_icon: 🫂
---
# Elon Musk

> 
> **Links**
> [(X)](https://x.com/elonmusk)
>
> **Relationships**
> - Good old friend, with the same dream of going to Mars 1 day.

> `="![LinkedinCover|250](" + this.cover + ")"`

```dataview
TABLE
rows.Details as "Details"
Where contains(log, this.file.name)
FLATTEN log as Details
WHERE contains(Details, this.file.name)
GROUP BY file.link as Source
SORT rows.file.day desc
```