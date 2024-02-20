# FTK Imager
- Run Capture Memory: to capture volatile memory.
- Run Create Disk Image: to capture the image of a disk. 

# Powershell - procdump
Procdump is a system administrator tool that is in the Sysinternals suite of tools from MS
```
.\procdump.exe -ma 1688
```

# KAPE 
Browser data acquisition

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f5821f11-5b04-4ecc-af7c-175bdcf5f1a3)

Select Browsers
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/9e7b52fe-1409-4b38-bb50-ff405ede9b48)

Execute

Storage location: 
- KAPE Browser Forensics\C\Users\JBeam\AppData\Local\Google\Chrome\User Data
- KAPE Browser Forensics\C\Users\JBeam\AppData\Roaming\Mozilla\Firefox\Profiles

# Browser History Capture (BHC)
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/a3920f9f-39a2-4c23-bd8d-6f79bb58c3c5)

Load capture in Browser History Viewer

# Recycle Bin

Navigate to the recycle bin in CMD
```
cd \$Recycle.Bin
```

Scan the directory with RBCmd.exe, this will save a CSV file to the desktop
```
C:\Users\BTLOTest\Desktop\Recycle-Bin-Analysis\Tools\RBCmd.exe -d . --csv C:\Users\BTLOTest\Desktop\
```

Application: https://github.com/EricZimmerman/RBCmd

Note
$R: Contains the true file contents of the recycled file.
$I: Files that start with $I and end in the same string as the $R counterpart contain the metadata for that specific file
