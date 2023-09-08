```dataview
TABLE
Class as "Class",
Due-Date as "Due Date",
Tagged-Concepts as "Tags"
FROM #class-work WHERE Due-Date != "{{date}}" AND Status != "Done"
SORT Due-Date asc
```

