```dataview
TABLE
Class as "Class",
Date as "Date",
Due-Date as "Due Date",
Tagged-Concepts as "Tags"
FROM #class-work WHERE Date != "{{date}}" AND Status != "Done"
SORT Due-Date asc
```

