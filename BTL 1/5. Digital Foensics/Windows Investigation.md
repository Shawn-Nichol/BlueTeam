# LNK Files
C:\Users\$USER$\AppData\Roaming\Microsoft\Windows\Recent

Windows uses LNK files to link one file to another, which is how we can have application shortcuts that work as a redirector. When a shortcut is clicked, it will find the application wherever it resides in the files system and run the corresponding application. 

Use "Windows File Analyzer" to view these files in human-readable format. 

# Prefetch Files
Prefetch files can provide information about programs, including the application's name, the path to the executable file, when the program was last run, and when the program was created/installed. 

Found: c:\Windows\Prefetch

To view these files, use the Prefetch Explorer Command line, also known as PECmd.exe.

# Jump list
Jump list feature is able to find two different types of files: automaticDestination-ms and customDestination-ms. These files contain information about applications that are pinned to the taskbar, such as the file path, timestamps, and application identifiers. 

C:\Users\% USERNAME%\AppData\ Roaming\Microsoft\Windows\Recent\AutomaticDestinations
C:\Users\%USERNAME%\AppData\ Roaming\Microsoft\Windows\Recent\CustomDestinations

Analyze these files with "JumpList Explorer."

# Winlogon Artifacts
Event ID
- 4624 (Successful logon)
- 4672 (Special logon)
- 4625 (Failed Logon)
- 4634 (Logoff)

Windows event logs are stored at the following location
c:\Windows\System32\winevt\Logs



