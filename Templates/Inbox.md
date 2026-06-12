
```dataview  
TABLE without id  file.outlinks AS "OUTGOING",   file.inlinks AS "BACKLINKS"  WHERE file.name = this.file.name 
```

```dataview  
TABLE without id  dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as created,  dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "last modified"   WHERE file.name = this.file.name
```

#task/now %% now | next | waiting | someday %%

- [ ] {{title}}


# Links

# Description
