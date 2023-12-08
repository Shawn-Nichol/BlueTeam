Note this challenge includes live malware; I've created a dirty VM on my virtual box and have disabled network access and copy on the VM.

OSINT
https://owasp.org/www-community/vulnerabilities/follina
https://www.reversinglabs.com/blog/threat-analysis-follina-exploit-powers-live-off-the-land-attacks



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

# Question 9
This can be found on multiple sites. 
CVE-2022-30190






