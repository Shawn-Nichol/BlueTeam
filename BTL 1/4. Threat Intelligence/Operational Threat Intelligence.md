 # Precursors
 Threat Precursors are elements of the incident identification and response process that allow both an attacker and a security researcher professionals to determine the existence of flaws and or vulnerabilities within a system. 

*Issues with precursors*
Precursors can help with the security scheme of an organization, but they have a disadvantage in terms of identification. The vast majority of attacks do not have identifiable or detectable precursors. 


 *Types of Precursors*
One of the most effective ways to obtain information about a network is through scanning. Using tools such as Nmap, Netcat, and Nessus, both a researcher and an attacker can learn about the services and vulnerabilites that exist on a system. A lot of information can be gained from performing host discovery, port scanning, and vulnerability scanning activities, such as which ports or services are running and responding on a system, what operating system is installed on the system, and what applications and versions of applications are present. 

# IOC
IOC examples
- Email Address: Mailboxes that have been acting maliciously, such as sending emails containing malicious URLs, attachments or attempting social engineer

- IP Address: IPS have acted maliciously, such as performing unauthorized port or vulnerability scans hosting malicious content or websites, or have been linked to malicious actor infrastructure such as C2. WhoIS lookups can also be conducted to gain more information, such as who owns the IP, where it is geographically based, hostname, and occasionally contact details.

- Domain Names: Sites that have been acting maliciously, such as hosting malware, phishing sites, or other malicious content.

- File Hashes: We can easily share intelligence about malware or other malicious files, often by referring to them by their unique hash values.

*IOC Formats*
STIX and TAXII are common methods of sharing threat intelligence, such as indicators of compromise. These values alone don't mean a lot, but with STIX, we can share information in a structured format, providing a lot more than just lists of IOCs. 

*STIX*
Structured Threat Information eXpression was developed by MITRE and the OASIS Cyber Threat Intelligence Technical Committee as a standard language for sharing threat information. STIX is designed to work with or without TAXII, it is also designed to share IOCs and the following:
- Motivations
- Abilities
- Capabilities
- Response

*TAXII*
Trusted Automated eXchanged of Intelligence Information defines how cyber threat information can be shared by using services and message exchanges. Designed to handle STIX information, this platform is run on a server and allows the sharing of information between specified groups or provides a public threat stream


# ATT&CK Framework
ATT&CK is a knowledge base and model for cyber adversary behavior, reflecting the various phases of an adversary's attack lifecycle and the platforms they are known to target. Since its introduction in 2013, it has become one of the most respected and referenced resources for cybersecurity  professionals. 


# Cyber Kill Chain
It was Developed by Locked and Martin in 2011, and it is an intelligent Drive Defense model for the identification and prevention of cyber-attacks, specifically ones that can be classified as APT

CKC is split into seven different stages; all seven stages need to be completed for an attack to be considered successful. 

*1 Reconnaissance*
Attackers: Malicious actors will conduct research on the target organization typically using both active and passive reconnaissance methods such as domain record lookups, public IP range port, and vulnerability scanning, scouting out employees on social media. 

Defenders: Activity conducted by the attackers at this stage will come in the form of precursors, such as IPs that are performing port or vulnerability scanning, employees being approached by individuals that they do not know, and employees potentially receiving connection friend requests. 

*2 Weaponization*
Attacker: create their backdoor instead of purchasing commodity malware and host this file on a domain they own. They then write a macro within an MS Word doc that connects to the attacker-owned domain and downloads the malware to the system where the file was opened. 

Defenders: It is extremely hard for the security team to detect this stage, as it is not happening within their environment therefore, they have no visibility of what happens outside the organization. Typically, defenses should be employed such as anti-virus, email security, and system hardening. 

*3 Delivery*
Attacker: crafted a spear-phishing email using information gathered on the target from OSINT. The email contains an MS Office doc with a malicious macro that will run malware in the context of the currently signed-in user. 

Defender: The security team should have email defenses in place, such as attachment sandboxing, which should be able to detect any malicious attachments, such as immediately malicious binaries or malicious Word documents or PDFs

*4 Exploitation*
Attacker: Malicious actors have identified a vulnerability that, if exploited, can provide them with higher privileges than the currently compromised account has, providing them with more access and the ability to perform more actions. 

Defenders: The security team can prepare for this stage by hardening systems and performing vulnerability management processes to identify and remediate vulnerabilities that are both internal and externally present. 

*5 Installation*
Attackers: installs a backdoor and deploy persistence tactics and techniques to ensure that they can keep a foothold within the infected system, allowing continuous access

Defender: The security team can deploy EDR software agents to potentially infected hosts to allow for the detection, investigation, and eradication of malicious presence. 

*6 Command and Control*
Attacker: The malicious actor installs malware that opens a channel between the malicious actor and remote machine, allowing them to send commands to the malware and attempt to gain the ability to complete step 7, actions on objectives. 

Defender: the defender's last step to fully stop the threat, prevention of command execution is key. 

*7 Action on Objectives*
Attacker: was successful in their attack and has obtained keyboard access; they are not able to attempt to complete any objectives they have. 

Defenders: The defender must detect this stage as quickly as possible to prevent further damage and minimize the time that the attacker can complete their objectives. 


# Cyber Attribution
IS the determination of cause or origin of action. In cybersecurity, we are concerned about this when malicious actors are in play and determining who, what, or where a cyber breach or intrusion has occurred. Attribution is not solely focused on laying blame but on gathering information; a new user may inadvertently cause a system failure; this would be attributed to inexperience rather than a malicious act. 

*Machine Attribution*
Attributing malicious cyber activity to a machine or multiple machines would mean identifying the machines used in an attack. This usually requires examining things like the IP address, log files, what is happening in the network, who has logged in to the machine. 

*Human Attribution*
finding the identity of the person responsible for the activity. Technical forensics, which looks at data left behind, may not be able to help much further; credentials may point to one person, but that may not have been the person physically executing the attack. 

*Ultimately Responsible Attribution*
Attributing this malicious activity to the ultimately responsible party answers the question of who is to blame. Was the actor working alone and fully responsible or working on behalf of an organization or nation-state?


Key Indicators to Attribution
- Tradecraft: frequently used behaviors such as an attacker's techniques, tools, and procedures used to conduct cyber-attacks
- Infrastructure: The physical machines or networks used in the attack are often compromised by other means before an attack.
- Malware: Malware can be specific to a threat actor; it can be reused, or it can be modified quickly if a compromise is suspected to avoid attribution
- Intent: The intent behind the attack, the motivation, or reasoning.
- External sources: External reports from organizations like cyber security companies, media even students

*Cyber Attribution Techniques*
Investigators use many different tools and programs to reveal information about attacks. As an example, let's consider a US-based company that was attacked with malware. This was written in a non-native language, the Cyrillic alphabet. T


# Pyramid of pain
The pyramid of  pain is a viual representation of the amount of pain we can cause a malicious actor by denying them certain indicators, working to disrupt their operations. Starting at the bottom are the easiest indicators that an actor can change, and at the top is the hardest indicator to change, forcing adversaries to change their entire operations by understanding and defending against the techniques they use in attacks. 


*Layers Explained*
*Hash values *
Trivial amounts of pain related to hash values. They can provide the highest confidence indicators yet are vulnerable to modification by the attack or accidentally by the end-user. By the degree that these can change and how often, these would be the least useful indicators and provide a  minimal amount of frustration to an attacker. 

*IP Address*
Next is the IP addresses. Though having a unique address is beneficial, changing these with VPNs, TOR browsing, or open proxies to reassemble your attack from a different address is not uncommon. 

*Domain Names*
Can be changed but requires registration and hosting. Many DNS providers do not all have the same standards across the board in terms of legality and restrictions, which can make it fairly easy for an attacker to change domains. Though not as easy as IP addresses, these can be modified with a longer wait time. 

*Network/Host Artifacts*
Network and host artifacts start to provide more difficulty to the attacker once you begin implementing defenses against these tools and methods they are using. 
- Different domain names
- Different IP addresses
- Different hashes

Changing the logic in the malware is much harder than changing the IP address. Signaling out these indicators and stopping them it creates greater frustration and hurdles for the attackers. 


*Tools*
Tools are hard to change. Carpenters can use reliable saws for years. The same goes for adversaries attacking your network. Identifying one or more of the tools they are using to distribute attacks and halting their use puts a severe bend in their hose. This requires re-tooling, researching, or building another method to attack. This could also simply force them to move on. 

*TTPs*
Finally, we come to tactics, techniques, and procedures. These are not just tools, but these are behavior patterns. You learned their methods by profiling the behavior and responding accordingly, such as spearphishing with PDFs. These attackers are human and act in similar, producible patterns. Forcing them to change their behavior and methods is the most time-consuming defense against them. 
