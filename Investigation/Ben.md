# Question 1 - 4
Can easily be identified by analysising the raw data of the email. 

# Question 5
Unzip the attachment the file is disguised as a PDF; if you show the extension, you'll notice the file is actually exe. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/98f2cef3-de0c-40cc-8118-2eb5f4f02264)

Load the PDF file into CyberChef, and start skimming the content until you find "W.a.i.t.F.o.r.E.x.i.t." the mutex will be in curly brackets after this.

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/1f0dece6-b655-47cf-b02f-49a56e6c57b9)
Note: you need to remove the "." when submitting the answer. 


# Question 6
Move the file to the Noriben directory. Noriben is a sandbox that is designed to run malware and perform analysis. 

Run Norbien.py this will start system internals Procmon and run the unzipped application; after the application runs, press "CRTL C" in the terminal to stop Norbien. Norbien will create a txt file for you to review. 

In the registry Activity section of the txt, you'll find two odd executable names
- Explorer.exe
- Microsoft Corporation.exe

Copy their file path into the answer, Note: the file path starts with C:\


# Question 7
Note the extubale names from the previous question


# Question 8
Well, the application is running. Run the NETSTAT command in a terminal, review the results, and look for an out-of-place IP with SYN_SENT
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/21d96307-0864-4662-9d38-c0ea8e9710e4)
