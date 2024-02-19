# LNK Files
The Windows OS uses LNK files to link one file to another, which is how we can have application shortcuts that work as a redirector. 

Meta data
- LNK created
- Modified
- last accessed
- File size

Location: C:\Users\$USER$\AppData\Roaming\Microsoft\Windows\Recent
Human readable application: Windows Analyzer https://www.mitec.cz/wfa.html

# Prefetch Files
Provide information about programs, including the application's name, the path to the executable file, when the program was last run, and when the program was created/installed. 

Location: C:\Windows\Prefetch
Human readable application: PEDmd.exe https://ericzimmerman.github.io/#!index.md

# Jump list
Jump list contains to types of files: automaticDestination-ms and customDestination-ms. These files contain information about applications that are pinned to the taskbar
- file path
- timestamp
- application identifiers (AppIDs)

Jump list location
- C:\Users\% USERNAME%\AppData\ Roaming\Microsoft\Windows\Recent\AutomaticDestinations
- C:\Users\%USERNAME%\AppData\ Roaming\Microsoft\Windows\Recent\CustomDestinations

Human readable program JumpList
https://ericzimmerman.github.io/#!index.md


