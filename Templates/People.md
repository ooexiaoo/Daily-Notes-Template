---
name: 
aliases: 
type:
  - Person
  - Family
  - Sister
date-met: 
location: 
cover: pfp
cssclasses:
  - cards
banner: https://w.wallhaven.cc/full/lm/wallhaven-lmqv3r.jpg
banner_icon: 🫂
---
# <% tp.file.title %>

> 
> **Links**
> [(X)]()
>
> **Relationships**
> -

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