---
type: dailyNote
date: <% tp.file.title %>
banner: "https://w.wallhaven.cc/full/7p/wallhaven-7pkg9y.jpg"
banner_y: 0.36
banner_icon: 📆
banner_x: 0.5
---
# <% tp.file.title %>
Tags:: #Daily_Notes 

**Prev::** [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]]
**Next::** [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]]
**Parent::** [[<% tp.date.now("YYYY-MM", 0, tp.file.title, "YYYY-MM-DD") %>]], [[<% tp.date.now("YYYY-[W]ww", 0, tp.file.title, "YYYY-MM-DD") %>]]

---
[Google Calendar](https://calendar.google.com/calendar/u/0/r?pli=1) | [Todoist](https://app.todoist.com/app/today) | [Toggl](https://track.toggl.com/timer)

## 🖼️ Pictures
### <% tp.file.title %>

## Toggl
```toggl
SUMMARY <% tp.date.now("YYYY-MM-DD") %>
```
## Todoist
```todoist
filter: <% tp.date.now("YYYY-MM-DD") %> | overdue
sorting:
   - date
   - priority
```

## 🌇 Morning Review
> [! rainbow]+
> ### 🌞 Log Morning
> log-sleep-hours:: 
> log-wake-time:: 
> fasting:: 
> log:: #on/morningReview

## 👣Tracking
> [! log]
> ### 🍽️ Consumables
> log-water:: 
> log-tea:: 
> log-food:: 
> healthy-eating:: 
> 
> ### 🔧 Habits
> Exercise:: 
> Meditation:: 
> Reading:: 
> Supplement:: 

## 🌆 Evening Review
> [! moon]
> log:: #on/dayreview
> log-day-rating:: 1-10
> log:: 

## 🧩 Which Files I Created This Day
> [! data]
> ```dataview
> LIST
> WHERE file.cday = date(<% tp.file.title %>)
> SORT file.ctime desc

## 🛠️ Which Files Were Modified Last This Day
> [! data]
> ```dataview
> LIST
> WHERE file.mday = date(<% tp.file.title %>)
> SORT file.ctime desc

## 📓 Notes Surrounding This Day
> [!data]
> ```dataview
> list
> where date(this.file.ctime) - file.ctime <=dur(1week)
> sort file.name asc
> ```