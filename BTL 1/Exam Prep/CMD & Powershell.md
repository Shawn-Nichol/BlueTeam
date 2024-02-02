# CMD

```
ipconfig /all
```

Check running tasks
```
tasklist
```

Display running processes and the assciated binary file that was executed to crreate it
```
wmic process get description, executablepath
```

Print a list of all system users to a terminal
```
net user
```

list all users that are in the administrators group. 
```
net localgroup administrators
net localgroup "Remote Desktop Users"
```

list all services and detailed information about each one
```
sc query | more
```

will list open ports on a system,
```
netstat -ab
```


# Powershell
Similar to ipconfig, to get network-=related information from the system
```
Get-NetIPConfiguration
Get-NetIPAddress
```

List all local users on the system
```
Get-LocalUser
```

Get specific details about a user
```
Get-LocalUser -Name BTLO | select *
```

IDnetify running services on the system. Out-GridView tells PS to show the results in a window. 
```
Get-Service | Where Status -eq "Running" | Out-GridView
```

Group running processes by their priorty value.  This provides process name, the process ID (PID) and other infomration. 
```
Get-Process | Format-Table -View priority
```
We can collect specific information from a service by including the name in the command
```
Get-Process -ID cmd | Select *
```

Get a list of scheudled tasks 
```
Get-ScheduledTask
Get-ScheduledTask -TaskName "TaskName" |  Select *
```


