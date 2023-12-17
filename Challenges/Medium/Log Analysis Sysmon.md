This challenge gives you a sysmon log file that can be analyzed with NotePad++ and Linux CLI. 

# Question 1

Using Linux CLI, I used CAT and GREP to search through the sysmon log file. Not knowing where to start I started performing searches on keys of key/pairs from the sysmon file. 

```
cat sysmon* | grep "key" | sort | uniq
```
Keys tried
- OriginalFileName: I returned several binaries, all of which were legitimate.
- ParentCommandLine: There were some potentially suspicious files; googling these file names didn't return anything suspicious. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/1de81b99-ff0b-469b-b885-42b34446bc00)
- TargetFileName: Returned a lot of DLL, and don't think this is what we are after
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
What is a LOLBIN

LOLBIN stands for "Living Off the Land Binaries." These are legitimate, built-in executable files or binaries within an operating system that attackers leverage to carry out malicious activities. The term emphasizes using these trusted and often overlooked system binaries for nefarious purposes.

Use the "CTRL+F" to find events that contain "comspec=C:\\windows\\temp\\supply.exe", this will return two results. The two events have an OrignalFileNames of CMD.exe of FTP.exe. Note that "comspec" is in the ParentComandLine of the second event; this indicates that the second event called the LOLBIN. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/c448c4ee-7e38-4cf6-85f4-b462939b7a00)


ftp.exe
# Question 5
Start looking for events that ran after 2021-05-07 12:22:39.500 that contain supply.exe

This is the first event that contains supply.exe that runs after the time that includes a command. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/04a0cf38-b9be-4a9c-81da-21867fece083)



ipconfig
# Question 6
Earlier, I used the key TargetFilename, which returned a lot of dll, one that I thought was odd was python27.dll

python
# Question 7
We know that Invoke-WebRequest was used to pull files, so the list starts looking for these events. 
```
cat sysmon* | grep -i "Invoke-WebRequest" | sort | uniq
```
Note: you need to use the -i flag so the search isn't case-sensitive. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/31f09920-f0d9-4c90-a454-fab03546f5b9)

https://github.com/ohpe/juicy-potato/releases/download/v0.1/JuicyPotato.exe

# Question 8
Now that we have the application the attacker is using, "juicy.exe" (The application name was obtained from the Outfile of the Invoke-WebRequest). We can parse the sysmon log for that information. 

```
cat sysmon* | grep "juicy.exe" | sort | uniq
```

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/61c5d098-b5b8-4dc1-9dfe-bd95c1112f60)

9898
