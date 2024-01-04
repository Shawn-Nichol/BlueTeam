# Provide header Artifacts
- Sending Email Addresses
- Reply-to Address
- Date Sent
- Sending Server IP
- Reverse DNS of Sending Server IP
- Recipients
- Subject Line

Any Relevant URls (Defanged)

Emails with Attachments
- File names + extensions
- Hashes

# Email Body Content
Attach the email file directly to the report ".eml" or ".msg" format. Plus, a brief description of the email and a screenshot saving other analysts the hassle of downloading and opening the email file in the client. 




# Analysis Process
This is the largest part of your report and will cover the analysis you completed to assess the risk of any malicious artifacts, such as attachments or URLs. You will include the tools used and the results that they have provided. This can include visualization tools, reputation check results, and manual investigation methods. 


# Defensive Measures Taken
There are three main types of actions
- Email artifact blocking (subject line, sending address, sending server IP)
- Web artifact blocking (URL, domain, IP)
- File artifact blocking (file name, file hash)

Two paths to complete these actions
- Analysts that are able to directly conduct defensive measures themselves
- Analysts who must request defensive measures to be taken by senior analysts or other departments need to provide sufficient justification.

# Sanitizing Artifacts
Defang URLS and IP addresses so other analysts don't mistakenly click links or open a file. 


# Practice report
BTL1 Phishing Analysis Domain - Report Writing Basic Template

=======================================
Section 1: Email Description and Artifacts Collected
=======================================
(Include a brief description of the email, and list any artifacts that have been retrieved, including email-based, web-based, and file-based if applicable)
This email was sent to 5 people in the company and tried to use social engineering to scare the recipients that their email account would be locked if they don't click on the link in the email.  

Sending Email Address:
emailsecalert1@gmail.com

Sending Server IP
209.85.222.173

Reverse DNS of Sending Server IP
mail-qk1-f173.google.com (Gmail)


Reply-to Address
emailsecalert1@gmail.com

Recipients
john.smith@dicksonunited.co.uk
alice.cooper@dicksonunited.co.uk
jacon.long@dicksonunited.co.uk
fred.johnson@dicksonunited.co.uk
pickle.rick@dicksonunited.co.uk

Date Sent
3:21 PM Monday 1st June 2020

Subject Line
Your Email Will be Locked! Act NOW!

======
Web Artifacts
======
Full URL (sanitized):
hxxps://outlook-security.emailsecalerts[.]net/index/2020/OWA.php?

Root Domain:
hxxps://emailsecalerts[.]net


=======================================
Section 2: Artifact Analysis
=======================================
(Include what actions have been taken to analyze email, file, and web-based artifacts, such as the tools and any results)
Email is themed to look like a security alert from Outlook, claiming the mailbox will be closed unless the recipients confirm their identity. Tells users to click a button. Using Outlook logos. 

A Reverse DNS search shows that the email has come from Gmail. 

URL2PNG shows that the full URL hosts an Outlook web access credential harvester. Requires email and password. 

VirusTotal shows this domain has been flagged for malicious/phishing activity. 

Checking the SIEM and EDR, no users have clicked on the link and created a network connection to the domain yet. 

Checking the email gateway shows no users have replied to the email. No other recipients than those stated above. 






=======================================
Section 3: Suggested Defensive Measures
=======================================
(Consider what actions we need to take to protect the organizations. Also, remember if blocking an artifact could have a negative consequence!)

The sender is using a Gmail address; the most appropriate action would be to block the specific mailbox to prevent any more incoming malicious emails from this sender. 


Request an email gateway block from the sending address "emailsecalert1@gmail.com"
The domain has been recognized as malicious, and there is no business justification for any  employees needing to access this site. VirusTotal recognizes this site as a credential harvester, the entire domain can be blocked on the web proxy, preventing employees from connecting to the site. 

Requesting a web proxy block for the domain "hxxps://emailseclerts[.]net
