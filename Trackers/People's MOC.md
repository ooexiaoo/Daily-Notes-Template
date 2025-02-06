```dataview
TABLE ("![|150](" + cover + ")") as Cover, date-met, location
FROM !"20 Templates"
WHERE contains(lower(type[0]),"person")
```