I'm using Ghidra to perform static analysis on the executable. 

# Question 1
Because this process starts early, I started going through the Decompiled first function 00401000, and found an API CreateProcessA, that is starting Notepad.exe. 


![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/d5693c8a-ea4a-4af8-9475-49ff6cd9550b)


notepad.exe, CreateProcessA

# Question 2 
Double-click the CreateProcessA to open API, start from 0 at the bottom, count two 4

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/bbb8e64e-0348-40f6-acab-0783b5a0e50d)

Google: dwCreationFlags
Select the following link: https://learn.microsoft.com/en-us/windows/win32/procthread/process-creation-flags
Now scroll down until you find the value 4

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/836c5be6-05d1-4a19-9910-4ef73f0a8cfb)

Create_Suspended

# Question 3
After some extensive search through the document, I noticed the PowerShell command was lower in Function 00401000, and that it was using base 64. Out of curiosity, I decoded this message, thinking it might be a clue to a later question. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b6f9a4a3-9ea8-425d-ba90-2162dc1e3235)

somec2.server


# Question 4
This information was obtained in the previous question when the PowerShell command was decoded. 
Invoke-WebRequest, c:\\Windows\\temp\exp.exe


# Question 5
Below the function, start looking for any that start with an NT. You'll eventually come across "NtUnmapViewOfSection" cross reference the NTUNmap to ensure a NTDLL is underneath it. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f9b81d8f-7d98-4df8-861c-3484ea4c945a)

NtUnmapViewOfSection



# Question 6
Near the very bottom of the function, there are three Thread APIs. The question ask to update and resume the Thread, so by process of elimination,
- update would be: SetThreadContext
- Resume would be ResumeThread

SetThreadContext, ResumeThread

# Question 7
Based on the name of the challenge and the information obtained throughout the challenge, we know it will be some sort of Process Injection. There are 15 options to choose from, T1055.
- 001. talks about injecting DLL  libraries into the process, this doesn't sound like what we're looking for.
- 002. Portable Executable injection, sounds pretty good along with WriteProcessMemory, then invoke CreateRemoteThread sounds like a winner to me. 



T1055.002
