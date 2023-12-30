# Reconnaissance Emails
Reconnaissance emails are used to get a response from the recipient. This doesn't mean that the user has to reply to the sender, as there are ways that malicious actors can tell if an email has been successfully delivered or even opened. 

## Tactics
**SPAM**
These emails do not use any tactics and are simply looking to see if an email error code, such as undeliverable, is sent back to the attacker. This allows the attacker to determine whether the mailbox is in use. 

**Social Engineering**
These emails will typically follow the format of either a spam recon email, a social engineering email, or a social engineering email but are combined with an invisible tracking pixel, which allows the attacker to see if an email client has viewed the email. While the other email types can determine if a mailbox is being used, using a tracking pixel can help the attacker understand how active the mailbox is. 

The malicious actor will add the tracking pixel using HTML code in the email body.  This code contains an external link to a pixel server. If the email recipient opens the email, the client or webmail provider will load the HTML code and send a message back to the server. 

Tracking pixel can obtain the following information
- OS
- Type of website or email used
- Client used
- Client's screen resolution
- Date and time the email was read
- IP address.

Recon emails are often observed daily by large organizations. They typically always make it through the  email gateway as they do not contain any malicious indicators, so they are not inherently malicious. 


## Credential Harvestor
Credential harvesters are the most common phishing emails, targeting human weaknesses to attempt to retrieve valid credentials, which can potentially be used to gain access to numerous services and accounts as a result of credential stuffing attacks. 

These emails tries to trick users by redirecting them to a legitimate-looking site and tries to get them to enter their credentials. 


- Imitates commonly used websites and services
- Entices the recipient to enter credentials into a fake login portal
- Uses social-engineering tactics, including creating a sense of urgency and using false authority.
- URLs may be completely random or attempt to copy the legitimate domain name of the organization they are masquerading as
- Often have small spelling or styling mistakes, which is extremely rare, with legitimate emails from big brands and organizations.

# Social Engineering
Social engineering is exploiting a human instead of a system, using psychological methods to get them to complete actions that they wouldn't normally do. 

Commonly used social engineering tactics in phishing emails
- Convincing the recipient to reply to an attacker's initial email
- Convincing the recipient to transfer money by posing as the CEO, CTO, CFO
- Convincing the recipient to provide the attackers with confidential or private information by posing as the data subject or someone in a higher position within the company.



# Vishing and Smishing
Targets users by voice or Text message. 


**Smishing**
is a kind of phishing attack where the attack vector is through a text message or SMS 

Victim: messages can be sent in bulk. 

Target: These attacks are after PII or banking or financial information. 

Ways to defend: User security awareness training and education, as well as being diligent in clicking links or completing actions sent from unknown phone numbers or impossible phone numbers. 

## Vishing
