# Start Splunk
open terminal
- sudo systemctl start Splunkd

Open Firefox
- 127.0.0.1:8000

# Splunk filters
Searches the botsv1 database; earliest will start at the 0 entry. 
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


# FIlters
Source IP
```
search src="10.10.10.50"
```

Search or Destination IP
```
search src="10.10.10.50" or dst="10.10.10.50"
```
wild card
```
search src="10.10.10.50" dst="10.10.10.*"
search pass* AND fail*
```


# Search commands
Sort
sort the events returned by the search, 

sort time by ascending
```
| sort time asc
```
Limit the return results.
```
| sort limit=2 time asc
```


Stats
Provides statistics about the results
```
| stats count by srcip
| sort count desc
```

Table 
create a custom table of the data we want to display and hide everything else

```
| table date, time, srcip, dstport, action, msg
```

Uniq/Dedup

used to retrieve unique values from the search
```
| table srcip | uniq
```
de-duplicate results
```
| table action | dedup action
```
