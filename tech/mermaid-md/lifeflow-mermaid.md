#### Document Lifecycle Flowchart

```flow
st=>start: Open Document
editing=>operation: Make edits
sv=>operation: Save, Sign, Commit
cpr=>operation: create PR
sigs=>condition: Enough Sigs?
pr=>condition: Part of PR?
e=>end: Merge changes

st->editing->sv->pr(yes, bottom)->sigs(yes, bottom)->e
pr(no)->cpr(right)->editing
sigs(no)->editing
```
