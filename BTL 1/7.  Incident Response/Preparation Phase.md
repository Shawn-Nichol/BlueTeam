# Incident Response Plans
IRPS are typically split into the following categories
- Preparation
- IDentification
- Containment
- Eradication
- Recovery
- Lessons Learned


# Preparation
- Developing Reponse plans for different incident types and running simulated scenarios to evaluate how the incident response team responds, training them for the real thing.

- Esnure that all resources needed by the incident response team are approved and ready to use, such as laptops, notepbooks, software tools, forensic equipment, training, and the ability to abandon normal responsibilites when an incident occcurs.

- Continually train and evaluate the perfromance of incident response team memebers to ensure they are capable of completing their duties defined in the response plans. for Security analysts this could be analyzing and collectin information about  the incident, for forensics analysts it could be acquistion and preservation of digital evidence.


# Identification
- When did the incident occur
- Who discovered it
- How did they discover it
- What systems or business units have been affected
- Does it affect the organizations ability to operate.
- What is the scope of the incident

Once an incident has been discovered, orgnizations may choose to assign two values to help with prioritization, especially if myultiple incidents occur simultaneously

- Critically level: How fast does the response need to be?
- Impact level: How long will the incident impact business operations?

# Containmnet
Disconnect compromised devices from the internet preventing remote access, don't powering off systems. Powering off systems could result of the lose of crucial evidence taht could be in volatile areas such as memory. 

# Eridacation
USe Frame works like ATT&CK to work backwards and potentially identify previous  steps of the attack. 
Defensive measures should be taken to ensure that this type of incicdent can't happen again by hardening systems applying patches, and empowering automated defenses such as NIPS and HIPS using indicators of compromise gathered throught the investigation. 

# Recovery
Returnbing business operation to normal by moving affected systems back to production environments now that they have been cleaned and hardened. 

# Lessons Learned
Once the investigation and response are complete, a meeting should be held that includes any stakeholder involved in the incident. The focus of this meeting should be to recap exactly what happened, specifically what went well and how could the respone have been improved. 


# Emails

SPF Sender Policy Framework
A SPF is a type of DNS record that can help prevent an email address from being forged. This record is established to identify the hostnames or IP addresses that are allowed to send emails to your custom domain. When having an SPF record specified on your domain helps prevent a malicious actor from spoofing your domain. The SPF text record contains three parts: the declaration of the record type, the IP addresses, and external domains that can be sent on your domain's behalf, and an enforcement rule. 


Domain Keys Identified Mail
DKIM is a method of email authentication that cryptographically verifies if an email has been sent by its trusted servers and hasn't been tampered with during transmission across the internet. The way that DKIM works is that when the mail server sends an encrypted hash of the email contents, it is generated using a private key, and then it adds this hash to the email header as a DKIM signature. The receiving server will be able to verify whether the email contents have not been tampered with by looking up the corresponding public key in the domain's DNS records once a new hash is verified whether the original and the newly generated hash match to ensure email message integrity. 

Domain-based Message Authentication, Reporting & Conformance
DMAC is an email authentication, policy, and reporting protocol. DMARC is built largely off of concepts taken from SPF and DKIM, but it adds several improvements to those protocols. This record type allows the domain owner to specify what should happen if emails fail both SPF and DKIM checks. There are three basic options that the mail server can take: none, quarantine, and reject. 


