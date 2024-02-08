Suspects name Zerry

# Question 1
Open the Text file in the disk image folder. This file provides metadata about the disk image that was extracted with FTK. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/a607c886-c673-4f17-9ed2-a3b74bd08261)

Sector Count: 25,165,824
MD5 checksum: 5c4e94315039f890e839d6992aeb6c58


# Quesiton 2
Open Autopsy and check the following locations for communication programs
- Installed programs, but nothing is in this folder. 
- Web download: there is nothing of note in this folder.
- Web search shows a search for "Signal download." 

With a quick look in the Windows prefetch folder, we can see  the signal application has been run. 
```
c:\Windows\Prefetch
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b52418ce-788f-4cea-b5b2-a84f8040664f)

Details about the prefetch folder. </br>
https://www.geeksforgeeks.org/prefetch-files-in-windows/

A Google search for Signal Decryption should return this handy page from Bleeping Computers. This page provides details on where the encryption key and database are stored. 
- Encryption Key: %AppData%\Signal\config.json
- Database: %AppData%\Roaming\Signal\sql\db.sqlit
https://www.bleepingcomputer.com/news/security/signal-desktop-leaves-message-decryption-key-in-plain-sight/

The article states that Singal stores the encryption key in plain text in the %AppData%\Signal\config.json

Zarry Singal application encryption can be found here
Location	/img_Zerry.E01/vol_vol3/Users/ZerryD????/AppData/Roaming/Signal </br>

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/7c772527-8ff5-4e40-892c-54811d9e0ca8)

Extract the file to the desktop to pull the Encryption key. 
{  "key": "c2a0e8d6f0853449cfcf4b75176c277535b3677de1bb59186b32f0dc6ed69998"}

# Question 3
Extract the SQL database from the image. Using DB Browser, we can open the database with the encryption key. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/e3cf1a7a-2354-4270-bd48-7362389279b8)

Note: Select the Raw key, and start the key with 0x



Conversation, Browse table. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/6014d7be-a806-4258-894d-f0f0ec883e55)
Phonenumber: 13026482364 </br>
Profile name: ZerryThe🔥

# Question 4
table: Messages_FTS_content </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/6c176ffa-9641-4a9e-9bdc-95b959c1a1bd)

eekurk@baybabes.com

# Question 5
Based on the Signal conversation, Zerry sent his email to Tom at Sunday, January 17, 2021 6:20:06.140 AM GMT, Zerry then confirmed the download on Sunday, January 17, 2021 6:25:16.179 AM GMT. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/0fe509c6-d3e9-4065-9399-4969372e0dd6)

Email sent time
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/14db248f-b828-4299-9dc3-f9093478a7e0)

Epoch Time: 1610864406140
GMT Time: Sunday, January 17, 2021 6:20:06.140 AM

Attachment confirmed time
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f12926d9-58f5-4eb7-8b42-011b400364b7)

Epoch Time: 1610864716179
GMT Time: Sunday, January 17, 2021 6:25:16.179 AM
Going back into Autopsy we can see that Zerry accessed the following file on Sunday,  January 17, at 6:24:39 AM. 
 
File: ⏳📅.png </br>


![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/022db508-3094-4483-b17b-62efa523f960)

# Question 6 




