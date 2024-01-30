# Win Event Logs
4663 - high number of files being deleted
4724 - Password Reset
4704 & 4717 - Change Usesr rights assignments
1102 - Security log cleared
529 - failed logon
624 - new user created
4624 - User successfully logged on
4625 - ASccount failed to log on
4672 - Special Logon, admin logs onto the system. 


# Splunk filters
Searches the botsv1 database, earliest will start at the 0 entry. 
```
index="botsv1" earliest=0
```

# Fields
Selected fields 
- Are the most important

Interesting Fields
- Have values in at least 20% of the search results
- a: next to a value notes a string value
- #: next to a value notes numeral


Source - option to see where the data we're dealing with is coming form, this is good way to filter log sources Ex. just Winevent logs. 
Source Type - the type of data we have. 
