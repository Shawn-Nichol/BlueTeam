Note this challenge includes live malware; I've created a dirty VM on my virtual box and have disabled network access and copy on the VM. The "any.run" website now requires a company email to register to prevent me from utilizing the tool; I was able to identify all the information need by utlizing native Kali tools and OSINT. 

OSINT
https://owasp.org/www-community/vulnerabilities/follina </br> 
https://www.reversinglabs.com/blog/threat-analysis-follina-exploit-powers-live-off-the-land-attacks  </br>
https://www.reversinglabs.com/blog/threat-analysis-follina-exploit-powers-live-off-the-land-attacks </br>

## Description
The Follina vulnerability represents a significant risk within Microsoft Office products. It enables remote code execution (RCE) attacks, demanding immediate attention as Microsoft has released security updates to address it. 

The vulnerability (CVE-2022-30190) affects the Microsoft Support Diagnostic Tool, a standard component of the company’s Windows operating system.

# Question 1
Run SHA1 against sample.doc
```
sha1sum sample doc
06727ffda60359236a8029e0b3e8a0fd11c23313
```


# Question 2
Enter SHA1 sum into virus's total
Office Open XML Document 


Question 3
again, use virus total; I went through all the links before finding the correct one.
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/b3e9f32a-c6d8-44ef-a3c5-6a780ff3a469)

https://www.xmlformats.com/office/word/2022/wordprocessingDrawing/RDF842l.html

Question 4
Virus total: in the bundle files, you'll notice one document with a rels on the end of it, you can remove the file path, as the question is only interested in the file name
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/76b5e9f1-cc96-48e2-90b8-5bd5c5864017)

document.xml.rels

# Question 4
THis can be found on the following blog
https://www.huntress.com/blog/microsoft-office-remote-code-execution-follina-msdt-bug

4096

# Question 5


# Question 6
 This information is available on the huntress blog
 
 msdt.exe

# Question 7
Event ID 4688 corresponds to a new process being created. 
ProcessName: Refers to the name of the newly created process. 
ParentProcessName: Refers to the name of the parent process that initiated the creation of the new process.

(ProcessName, ParentProcessName)
msdt.exe, WINWORD.exe

# Question 8
In virus total, go to the MITRE ATT&CK Tactics and Techniques. Click on the execution ID to navigate to the MITRE web page. 

T1059 matches the description of the malware on VirusTotal. 

T1059

# Question 9
This can be found on multiple sites. 
CVE-2022-30190






