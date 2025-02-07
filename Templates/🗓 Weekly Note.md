---
cssclasses:
  - cards
banner: "https://w.wallhaven.cc/full/d6/wallhaven-d6r3mm.jpg"
banner_y: 0.4375
banner_icon:
banner_icon: 📌
---
Tags:: #Weekly_Notes
**Previous Week -** [[<% tp.date.now("YYYY-[W]WW", +1) %>]]
**Next Week -** [[<% tp.date.now("YYYY-[W]WW", +7) %>]]

## Days of the Week
[[<% moment(tp.file.title).startOf('isoweek').add(-1, 'day').format("YYYY-MM-DD") %>|Sun]] | [[<% moment(tp.file.title).startOf('isoweek').add(0, 'day').format("YYYY-MM-DD") %>|Mon]] | [[<% moment(tp.file.title).startOf('isoweek').add(1, 'day').format("YYYY-MM-DD") %>|Tue]] | [[<% moment(tp.file.title).startOf('isoweek').add(2, 'day').format("YYYY-MM-DD") %>|Wed]] | [[<% moment(tp.file.title).startOf('isoweek').add(3, 'day').format("YYYY-MM-DD") %>|Thu]] | [[<% moment(tp.file.title).startOf('isoweek').add(4, 'day').format("YYYY-MM-DD") %>|Fri]] | [[<% moment(tp.file.title).startOf('isoweek').add(5, 'day').format("YYYY-MM-DD") %>|Sat]]

## Weekly Review
```dataview
TABLE log as "log"
FROM "Logs/📓 Daily Notes"
WHERE file.day >= date(<% tp.date.now("YYYY-MM-DD", 0 ) %>) AND file.day <= date(<% tp.date.now("YYYY-MM-DD", 6 ) %>)
SORT file.day ASC
```
## Toggl
```toggl
SUMMARY FROM <% tp.date.now("YYYY-MM-DD", 0 ) %> TO <% tp.date.now("YYYY-MM-DD", 6) %>
```
## Tasks This Week
> ```todoist
> name: "Today & Overdue "
> filter: "due after: <% tp.date.now("YYYY-MM-DD", 0 ) %> & due before: <% tp.date.now("YYYY-MM-DD", 7) %> & #inbox"
> sorting:
>    - dateAdded
>    - priority
> show:
>    - due
>    - date
>    - description
>    - project
>    - labels
> ```

- [ ] 

## Weekly Log
log:: #on/WeeklyLog