Description: is a PS script that was created by SANS to aid with the investigation and triage of Windows Event Logs. This tool can work with exported log files and live system to analyze. 

Can Identify the following attacks
- User Creation
- Users being added to groups
- Password guessing
- Password spraying
- Bloodhound offensive tool usage
- Obfuscated commands
- PS used to download remote files.
- Suspicious service creation
- MimiKatz used to dump LSASS.exe for credentail collection.
- and more.

# How to run
CD to the DeepBlue folder in powershell, when running the it for the first time you might come across an error.
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/119498dc-0f55-4ce5-89f6-3fb41fe4cdcd)

Disable this by changing the Execution Policy applied to the user. 
```
Set-ExecutionPolicy Bypass -Scope CurrentUser
```

Run the command again
```
./DeepBlue.ps1 ../Log1.evtx
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/2d4a517e-88af-4d40-b108-ea9decfd8f3c)

# Local analysis
```
./DeepBlue.ps1 -log security
./DeepBlue.ps1 -log system
```

