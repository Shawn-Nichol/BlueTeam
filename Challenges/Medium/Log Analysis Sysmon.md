This challenge gives you sysmon log file that can be analyzed with NotePad++. 

# Question 1

Using Linux CLI, I used CAT and GREP to search through the sysmon log file. Not knowing where to start I started performing searches on keys of key/pairs from the sysmon file. 

```
cat sysmon* | grep "key" | sort | uniq
```
Keys tried
- OrignalFileName: I returned several binaries, all of which were legitimate.
- ParentCommandLine: There were some potentially suspicious files; googling these file names didn't return anything suspicious. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/1de81b99-ff0b-469b-b885-42b34446bc00)
- TargetFileName: It returned too many results, so I ignored this one.
- DestinationIp: Return one unique result. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/17ef5d0a-af73-44b7-ab24-008445d7f825)

I searched for the sysmon log file for the IP address. There are 395 results, but looking at the first result, we can see an IP address with an unusual port. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/3f000c95-e22f-4a2f-911a-9b2cafd26efd)

updater.hta

# Question 2
Use the same command to return results for Powershell
```
cat sysmon* | grep "powershell" | sort | uniq
```
There are a couple of results, most of which have encrypted data, but those can be ignored. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/0559490e-313b-4c12-8ec0-3ef08d84de64)

Invoke-Webrequest, 6969

# Question 3
My first thought is that the ZoneId=3 would be the answer here. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/347ff1e0-0b6c-47ee-8fb4-c7687e68c904)

Next, I started combing through the log and used "CRTL+F" to identify any events containing IP address 192.168.1.11. After reading a few of the responses, I realized there were over 300 matches, which would take too long. This is when it dawned on me that variables are typically set with an = sign, So I used the following Linux command
```
cat sysmon* | grep "=" | sort | uniq
```
The first result was the clue I was looking for, as it contained a set command and looked like it was applying a variable. </br> 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/02d7dc58-f677-4e82-b3d8-ce6708052446)

comspec=C:\\windows\\temp\\supply.exe"

# Question 4


# Question 5
# Question 6
# Question 7
# Question 8
# Question 9
# Question 10
