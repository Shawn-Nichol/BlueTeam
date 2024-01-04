# Provide header Artifacts
- Sending Email Adddress
- Reply-to Address
- Date Sent
- Sending Server IP
- Reverse DNS of Sending Server IP
- Recipients
- Subject Line

Any Relevant URls (Defanged)

Emails with Atachments
- File names + extensions
- Hashes

# Email Body Content
Attach the email file directly to the report ".eml" or ".msg" format. Plus a brief descriptoin of the emaill and a screenshot, saving other analysts the hassle of downloading and opening the email file in the client. 




# Analysis Process
This is the largest part of your report, and will cover the analysis you completed to assesss the risk of any malicious artifacts such as attachments or URLs. You will include the tools used, and the results that they have provided. This can include visualization tools, reputation check resutlts, as well as manual investigation methods. 


# Defensive Measures Taken
There are three main types of actions
- Email artifact blocking (subject line, sending address, sending server IP)
- Web artifact blocking (URL, domain, IP)
- File artifact blocking (file name, file hash)

Two paths to complete these actions
- Analysts that are able to directly conduct defensive measures themselves
- Analysts that must request defensive measures to be taken by senior analysts or other departments, and need to provide sufficient justification.

# Sanitizing Artifacts
Defang URLS and IP address so another analysts doesn't mistakenly click link or open a file. 


# 
