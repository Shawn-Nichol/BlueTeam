# Sending Email Address
This where the email has come from. 

# Subject line
THe subject line  is useful artifact for both searching for other associated emails by using it as a search term in our email gateway security product, or for blocking incoming emails that use the same subject line. 

# Recipient Email Addresses
Identify which mailboxes have received this phishing email, so we can inform them not to interact with it. TO identify recipients check  the email gateway, and search for emails coming from the sending address and including the subject line we have observed. 

# Sending Server IP and Reverse DNS
Know the address of the server that has sent the email, this will help Identify if the email has been spoofed. Once the IP has been collected you can prefrom a reverse DNS search on it using online tools like Reverse IP lookup. 

# Reply to Address
The email address that will receive any replies to the orignal email. This value can be different then the sending address. 

# Date and Time
Recording the date and time all you to search for a period of time on either side of the observed time could allow for other emails to be identied that are a part of the same attack. 


# File Artifacts
**Attachment Name**
Knowing the uniquiness of the name could allow EDR platforms to block it. 

**SHA256 Value**
Can be used to provided more insite on the file. 

# Web Artifacts
**Full URLs**
Copy the URL, don't type it as this could lead to mistakes. 

**Root Domain**
Root domain can help show if the site has been created for malicious activity, or if it is a legitimate site that has been compromised. 

# Get File Hash
Powershell
```
get-filehash - algroithm sha1 .\file.exe; repat for MD1
```
