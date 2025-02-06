---
banner: "https://w.wallhaven.cc/full/d6/wallhaven-d6r2qo.jpg"
banner_icon: 📍
banner_y: 0.1525
cssclasses:
  - cards
---
Tags:: #Monthly_Notes 
**<% tp.date.now("YYYY-MM-DD HH:mm:ss") %>**

[[<% moment(tp.file.title, 'YYYY-MM').subtract(1, 'months').format('YYYY-MM') %>]] | [[<% moment(tp.file.title, 'YYYY-MM').add(1, 'months').format('YYYY-MM') %>]]

> [!rainbow] Weeks of the Month
> [[<%tp.date.now("gggg-[W]ww", "P-3W")%>|1st Week]]
> [[<%tp.date.now("gggg-[W]ww", "P-2W")%>|2nd Week]]
> [[<%tp.date.now("gggg-[W]ww", "P-1W")%>|3rd Week]]
> [[<%tp.date.now("gggg-[W]ww")%>|4th Week]]

```dataview
TABLE log
FROM #on/WeeklyLog
WHERE regexmatch("2025-W\\d{1,2}", file.name)
SORT file.name asc
```
## Toggl
```toggl
SUMMARY FROM 2024-12-01 TO 2024-12-31
```
## 3 Positives From The Month
- 
- 
- 

## 3 Things You Can Improve About Yourself By Next Month
- 
- 
- 

## Highlights Of The Month
* 

## What Did You Achieve This Month?
* 

## Goals For Next Month
- 
- 
- 

log:: #on/MonthlyLog