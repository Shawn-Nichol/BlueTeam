This challanges gives you JSON file that can be analysis with NotePad++. 

# Question 1

Using Linux CLI, I used CAT and GREP to search through the sysmon log file. Not knowing where to start i started prefoming searchs on keys from the JSON file. 

```
cat sysmon* | grep "key" | sort | uniq
```
Keys tried
- OrignalFileName: retuned several binaries, all of which ended up being legitmate.
- ParentCommandLine: Had some potentaill supicous files, googling these file names didn't return anything supcious. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/1de81b99-ff0b-469b-b885-42b34446bc00)
- TargetFileName: returned to many restult, so I ignored this one.
- DestinationIp: Return one unique result. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/17ef5d0a-af73-44b7-ab24-008445d7f825)

I searched for the sysmon log file for the IP address, there are 395 results but looking at the first result we can see an IP address with an unusal port. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/3f000c95-e22f-4a2f-911a-9b2cafd26efd)



# Question 2
# Question 3
# Question 4
# Question 5
# Question 6
# Question 7
# Question 8
# Question 9
# Question 10
