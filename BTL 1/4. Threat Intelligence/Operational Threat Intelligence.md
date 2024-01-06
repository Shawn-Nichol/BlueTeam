 # Precursors
 Threat Precursors are elements of the incident identification and response process that allow both an attacker and a security researcher of professional to determine the existence of flaws and or vulnerailites within a system. 

 **Issues with precursors**
 Precursors can help with the security scheme of an orgnaization, but they have a disavatage in terms of identification. THe vast majority of attacks do not have identifable or detectable precursors. 


 *Types of Precursors*
One of the most effective way to obtain information about a network iss through scanning. Using tools such as Nmap, Netcat, Nessus, both a researcher and an attacker can learn about the services and vulnerabilites that exist on a system. A lot of information can be gained from perfroming host discovery, port scanning, and vulnerability scanning activites, such as which ports or services ar running and responding on a system, what operating system is installed on the system, and what applications anad versions of applications are prsent. 

# IOC
IOC examples
- Email Address: Mailboxes that have been acting maliciosly, such as sending emails contaaining malicious URLS, attachemtns or attempting social engineer

- IP Address: IPS ahve acted maliciously, such as perfroming unauthorized port or vulnerability scans hosting malicious content or websites, or have been linked to malicious actor infrastructure such as C2. WhoIS lookups can also be conducted to gain more information, such as who owns the IP, where its geographically based, hostname and occasionally contnact details.

- Domain Names: Sites that have been acting maliciously, such as hsoting malware, phishing sites, or other malicious content.

- File Hashes: We can easily share intelligence about malware or other malicious files, often by referring to them by their unique hash values.

*IOC Formats*
STIX and TAXII are common methods of sharing threat intelligence, such as indicators of compromise. These values alon don't mean a lot, but with STIX we can share infomration in a structured format, providing a lot more than just lists of IOCs. 

*STIX*
Structured Threat INformatino eXpression, was developed by MITRE and the OASIS cyber Threat INtelligence Technical Committee as a standard language for sharing threat information. STIX is designed to work with or without TAXII, it is also designed to share IOCs adn the following:
- Motivations
- Abilities
- Capabilities
- Response

*TAXII*
Trusted Automated eXchanged of Intelligence Information, defines how cyber threat informamtion can be shared by using services and message exchanges. Designed to handle STIX information, this platform is run on a server and allows the sharing of information between specified groups or provides a public threat stream


# ATT&CK Framework
ATT&CK is knowledge base and model for cyber adversary behavior, reflecting the various phases of an adversary's attack lifecycle and the platforms they are known to target. Since it was introduced in 2013, it has become the one of the most respected and referenced resources for cyber security  professionals. 


# Cyber Kill Chain
Was Developed by Locked and martin in 2011and it is an intellgience Drive Defense model for the identificatino ad prevention of cyber-attacks, specifically ones that can be classified as APT

CKC is split into 7 different stages, all 7 stages need to be completed in order for an attack to be consider successful. 

*1 Reconnaissance*
Attackers: Malicious actors wil ldoncut research on the target organization typically using both active and passive reconnaissance methods such as domain record lookups, public IP range port, and vulnerability scanning, scouting out employees on social media. 

Defenders: Activity condcuted by the attackersr at this stage will come in the form of precursors, such as IPs that are perfroming port or vulnerability scanning, employees being approached by individuals that they do not know and employees potentially receivving connection friend requests. 

*2 Weaponization*
Attacker: create their own backdoor instead of purchasing commodity malware, and host this file on a domain they own. They then write a macro within a MS word doc that connects to the attacker-owned domain and downloads the malware to the system where the file was opened. 

Defenders: It is extremly hard for security team to detect this stage, as it is not happening within their environment therefore they have no visibility of what happens outside the organization. Typically defenses should be employed such as anti-virus, email security, and system hardening. 

*3 Deleviry*
Attacker: crafted a spear-phishing email using informatino gathered on the target from OSINT. The email contains a MS Office doc with malicious macro that will run malware in the context of the currently signed-in user. 

Defender: The security team should have email defenses in place such as attachment sandboxing which should be able to detect any maliciouws attachments such as immediately malicious binaries or malicious word ddocuemtns or PDFs

*4 Exploitation*
Attacker: Malicious actors have identified a vulnerability, that if exploited, can provide them with higher privileges than the current compromised acccount has, providing them with more access and ability to perfrom more actions. 

Defenders: The security team can prepare for this stage by hardening systems and perfroming vulnerability management processes to identify and remeidiate vulnerabilties that are both internal and externally paresent. 

*5 Installation*
Attackers: installs a backdoor and deploys persistence tactics and techniques to ensure that they can keep a foothold within the infected system, allowing continous access

Defender: The security team can deploy EDR software agents to potentially infected hosts to allow for the detection, investigation,and eradication of malicious presence. 

*6 Command and Control*
Attacker: The malicous actor installs malware that opens a channel between the malicous actor and remote machine, allowing them to send commands to the malware and attempt to gain the ability complete step 7, actions on objectives. 

Defender: the defenders last step to fully stop the threat, prevention of command execution is key. 

*7 Action on Objectives*
Attacker: was successful in their attack and has obtained keyboard access, they are nbow able to attempt to complete any objectives they have. 

Defenders: The defneder must detect this stage as quickly as possible to prevent further damage and minimiZe the time theat the attacker can complete tehire objectives. 







