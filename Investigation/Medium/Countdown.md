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
Based on the Signal conversation, Zerry sent his email to Tom on Sunday, January 17, 2021, 6:20:06.140 AM GMT; Zerry then confirmed the download on Sunday, January 17, 2021, 6:25:16.179 AM GMT. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/0fe509c6-d3e9-4065-9399-4969372e0dd6)

Email sent time
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/14db248f-b828-4299-9dc3-f9093478a7e0)

Epoch Time: 1610864406140
GMT Time: Sunday, January 17, 2021 6:20:06.140 AM

Attachment confirmed time
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f12926d9-58f5-4eb7-8b42-011b400364b7)

Epoch Time: 1610864716179
GMT Time: Sunday, January 17, 2021 6:25:16.179 AM
Going back into Autopsy, we can see that Zerry accessed the following file on Sunday,  January 17, at 6:24:39 AM. 
 
File: ⏳📅.png </br>


![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/022db508-3094-4483-b17b-62efa523f960)

# Question 6 
The hint tells you to look at Thumbcache_256.db in the /img_Zerry.E01/vol_vol3/ZerryD💣🔥/AppData/Local/Microsoft/Windows/Explorer/. 

Export this file to the desktop top and use Thumbcache Viewer to open the db. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/82dd0d60-4f28-4768-acd3-0a467a8bce85)

Looking at the DB, we can see only two files that aren't 0 KB. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/330cb757-00e3-41f1-8de7-1f3bccb91297)

View the thumbnail for both images. We can see one has a date and clock on it, giving us the time of the attack. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/fbaabf9b-11c2-4550-bab8-b6ad0d097ca2)

Time: 1-02-2021 9:00 AM 

# Question 7
The Signal conversation says they discussed the location at their annual meeting in 2020. 
EPOC TIME: 1610907262384

The following TOR database provides browser information such as bookmarks. That could be used to identify an encryption/decryption method. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/d7ed92c9-6604-4738-85a0-9225fa6a82bd)

Export the places.SQLite database to the desktop so it can be viewed in DB Browser. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/ad3eb4da-5f68-4acb-a0cf-461ee8cb0569)

To get the coordinates, export the Microsoft StickeyNotes folder
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b37b65bd-d341-4f39-95f6-b0e17053f714)

Open the folder in DB Browser. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/34ed3211-0758-4201-9d91-a8f03397bb79)

Check the Notes table and select the first column. This data now needs to be decoded in cyberchef with Rot13. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b5aeabc4-a528-438e-8f4e-32bda20e5187)

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/0c6f1bee-b873-4ca4-bf5f-7e6085b3e136)

40 degrees 45 minutes 28.6776 seconds N, 73 degrees 59 minutes 7.944 seconds W

