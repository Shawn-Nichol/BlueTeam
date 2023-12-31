# Sender Policy Framework (SPF)
A SPF record is a type of DNS record that can help prevent an email address from being forged. This record is established to identify the hostnames or IP addresses that are allowed to send emails to your custom domain. Having a SPF record specified on your domain helps prevent a malicious actor from spoofing your domain. The SPF TXT record contains three parts
- Declaration: of the record type
- IP addresses
- External domains that can be sent on your domain's behalf.

# Domain Keys Identified Mail (DKIM)
DKIM is a method of email authentication that cryptographically verifies if an email has been sent by its trusted servers and hasn't been tampered with during transmission. DKIM works because when the mail server sends an email, an encrypted hash of the email contents is generated using a private key, and then it adds this hash to the email header as a DKIM signature. The receiving server will be able to verify whether the email contents have not been tampered with by  looking up the corresponding public key in the domain DNS records. Once the receiving mail server decrypts the email with the public key, it calculates a new hash and verifies whether the original and the newly generated hash match to ensure the integrity of the email message. 

# Domain-based Message Authentication, Reporting & Conformance(DMARC)
DMARC is an email authentication, policy, and reporting protocol. DMARC is built largely off of concepts taken from SPF and DKIM, but it adds several improvements to those protocols. This record type allows the domain owner to specify what should happen if emails fail both SPF and DKIM checks. There are three basic options that the mail server can take:
- None
- Quarantine
- Reject



# SPAM Filter
SPAM filters were created with the end user in mind. 

Types of SPAM filters
1) Gateway: One that sits behind an on-premises network firewall. These can often be utilized by larger enterprise organizations.
2) Hosted: Hosted in a cloud. This works similarly to the gateway spam filters but is able to update more quickly than some of the on-premises filters.
3) Desktop: are user-installed and are typically used in SOHO scenarios. One major drawback of these filters is that they can sometimes be categorized as Freeware.


# SPAM filter Classification
**Content Filters**
Uses information in the email header and body to determine whether the email is legitimate or spam. When looking at the header, the filter could cross-reference the header with published blacklists or known spamming networks and automatically classify it as SPAM. 

**Rule-Based Filters**
A rule-based filter allows for emails to be filtered based on predetermined criteria. 

**Bayesian Filters**
Bayesian filters have become one of the most intelligent types of spam filters that can be used. It uses machine learning to learn users' spam preferences. EX. When the user marks an email as spam, it can analyze the characteristics of that message and use that information to block similar messages from going to the inbox. 

These are the three most common filters. 


# Attachment Filtering
It's a good idea to block attachments outright; common file types that are used for malicious activity are: 
- exe
- vbs (Visual Basic)
- js
- iso (Optical Disk Image)
- bat
- ps/ps1 (Powershell)
- htm/html

Typically,  businesses will use and send the following file formats via email, which can also be used for malicious purposes
- zip
- doc
- pdf
- xls

Email gateway and email security tools will often allow for different actions to be taken once a certain attachment has been identified, such as scanning it for malicious indicators, blocking the email from being delivered, quaranting the email, stripping the attachment, alerting the email gateway administrator, sending an email to specific recipients about the activity or generating logs which can be ingested by a SIEM platform and used to generate an alert for security analysts. 


# Immediate Response Process
1) Retrieve an original copy of the phishing email


2) Gather artifacts from the phishing email


3) Inform the recipients that received the email
This helps reduce the chance of them opening and interacting with the email. The email would contain the following
- Date and Time the email was sent
- Subject line
- Clear instructions on what to do with the email
- Contact details if the recipient is unsure what to do. 

4) Investigate malicious artifacts to collect indicators of compromise that can be blocked to protect the organization


5) Take defensive measures
Are actions taken by the security team  to reduce the risk generated by the phishing attack? This could include blocking emails, web, and file-based artifacts. 

6) Complete the investigation report, documenting all of the above steps.

# BLocking email artifacts
Once the artifacts are collected and analyzed, you can take defensive measures to block incoming and outgoing emails that feature these artifacts. Email artifacts
- Email sender
If a large volume is being sent from the same sender, you can block the sender on the email gateway, preventing more emails from coming in. 

- Sender domain
the step up from blocking the sending address is to block the entire sending domain. When receiving emails from @outlook or @gmail, it's obviously not feasible to block these entire domains, as there is a large potential to block legitimate emails. 
  
- Sending server IP
This is a very serious block and is not conducted unless it is absolutely necessary. This will drop any emails coming from the specified IP.

- Subject line
Phishing attackers will typically use one subject line. Otherwise, the attackers need to keep modifying it, creating more work. 

# Blocking Web artifacts
**URL BLocks**
URL blocks are extremely specific and will only block URLs that have been provided. 

Sometimes, URLs are dynamically generated for specific recipients; therefore, a URL block  would only neutralize the threat for one recipient. 

You can block URLs directly at the beginning to make the block more effective. 

**Domain Blocks**
Domain blocks work to prevent access to an entire domain. If you want to block google.com, it will prevent any web requests from going to Google. 


## DNS BLackholing
Blackholing is the process of creating a fake DNS entry so that if an employee tries to access a malicious site, they will be sent to another site. 

## FIrewall
Blocking an IP can be easily countered by changing the IP. 

# Blocking file artifacts
There are two standard types of blocks we can take when defending against malicious files. 
- Hash Blocking
- File name blocking

**Hash blocking**
Using EDR to block files based on their hash values can be countered by adding dummy data. 

**Blocking Names**
Typically, this is not a good idea unless the file has a unique name, as this could block legitimate files. 








