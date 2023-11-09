Digital forensics, also known as computer forensics, is a specialized field within the realm of forensic science that deals with the investigation, preservation, analysis, and presentation of digital evidence. That will be used in an investigation. 

The primary goal is to establish the authenticity and integrity of the evidence, enabling it to be admissible in court and, ultimately, to assist in solving cyber crimes, intellectual property theft, fraud, and other digital-related offenses. As technology evolves, digital forensics remains crucial in ensuring the integrity of digital evidence and upholding justice in the digital age. 

Digital Forensics, from a Security Operations perspective, is often associated with monitoring employees to maintain a high-security posture, aiding with incident response to reveal details of how a compromise occurred and any post-actions. 

# Types of digital forensics
These are the four main types of digital forensics used in cybersecurity. 

- Computer forensics: Identifying, collecting, and preserving evidence taken from desktops, laptops, and other computer systems and storage media to aid investigations or legal proceedings.
- Network Forensics: The monitoring, collection, and analysis of network activities such as visited websites and connected IPs, usually associated with incident response and intrusion detection.
- Memory Forensics: The Process of recovering evidence from the RAM of a running system
- Mobile Forensics: The process of recovering evidence from mobile phones, SIM cards, PDSAs, tablets, and other mobile devices.

# Benifits of Digital Forensics
Supporting Incident Response Capabilities
Having a better incident response capability can be achieved by having additional team members with strong technical backgrounds and skills that can help when responding to escalated security events. When dealing with an incident, it is important to correctly gather and preserve evidence so it can be  used for analysis, intelligence sharing, and potential prosecution. Digital Forensics analysts can be a great asset when it comes to analyzing malicious activities, from a malware infection to an insider threat, using their deep technical knowledge, analysis techniques, and monitoring capabilities. 


Legal Prosecution
Chain of Custody is a procedure for digital evidence to be submitted in court. If this evidence is not kept secure, accounted for, and unmodified at all times, it will not be valid and hold no weight in court. Forensics experts will be familiar with how to collect and handle evidence appropriately, keeping it secure. 

Monitoring Employees
Sometimes, employees need to be monitored closely due to suspicious or malicious behavior. This could include inappropriate internet browsing on work systems, breaches of an Acceptable Use Policy, downloading malicious or inappropriate files, or any other scenario that requires intervention from the security team. Forensics analysts will likely be trained to monitor for insider threats and covertly collect evidence, which the Human resources department can use as justification for firing an employee or handing over to law enforcement if the user's activity breaks any laws. 


# Associaiated Roles

### Tier 1 SOC Analyst
T1 Analysts will generally conduct initial investigations, mainly first-line incident response, and collect evidence to be added to an investigation case. This evidence is then used to justify taking defensive measures, such as blocking an IP, domain, or email sender. Here, an analyst will need to understand that these artifacts IPS, emails, and domains are considered evidence for the investigation.

### Tier 2/3 SOC Analyst
T2/T3 Analysts will typically handle escalated/more critical investigations that require more technical expertise or access to additional tools or sensors. Due to the nature of critical and higher-priority investigations, the related evidence is likely to be collected and handled under more strict conditions. 

### Malware Analyst
Within the security operations domain, Digital Forensics can also be used as a term to refer to the process of malware analysis. Taking a sample of malware and using different techniques to discover what its purpose is and how to detect it in the future by gathering IOCs. 

### Digital Forensics Analyst
Digital Forensics Analysts will work on high-profile investigations, escalated cases, employee monitoring, working with the security Incident Response Team, and other tasks that require trusted and highly technical individuals. 

### Insider threat Analyst
Security professionals that focus on detecting and monitoring insider threats will utilize their extensive digital forensics skills to ensure that no stone is left unturned and that any and all evidence against an individual is collected in the appropriate manner. 

### Threat Hunter
Threat Hunters are expert technical defenders that have a deep understanding of both offensive and defensive practices. To be able to effectively hunt these individuals need to truly understand how computers and networks work and also understand key artifacts that can be found and used as evidence of an intrusion

### Incident Responder
Incident responders are top-tier security analysts who typically possess skills across a wide range of blue-team disciplines, forensics being one of them. This allows them to conduct deeper, more in-depth investigations in order to understand how the system was compromised and the behavior of the device. 

An Incident Responder sometimes works closely with FOrensics Examiners, especially on tasks such as retrieving data from physical media such as laptops and phones and using specialist tools to process and analyze the data to find indicators of malicious activity. 


# Evidence Collection
### KAPE
Kape (Kroll Artifact Parser and Extractor) is a free and open-source digital forensics tool. Design to automate the collection and parsing of forensic artifacts from a computer's file system and memory. Kape can be deployed locally or on remote systems to quickly gather key data. This allows analysts to begin investigating while the lengthy process of taking a disk image is being conducted. KAPE can retrieve artifacts relating to browser usage, program execution, the filesystem logs, and much more. 

### FTK Imager
FTK Image is a massive tool that allows us to create hard drive images and memory images, which can be analyzed in other programs. It's also possible to import disk images into FTK, allowing us to navigate through the file system as if we were on a live device.

### Encase
Like FTK, EnCase is a suite of tools with a wide range of functionality for digital forensics and e-Desicvoery. EnCase can be used to take forensic images of computers, mobile phones, and IoT devices, which can then be analyzed to collect digital evidence. 

### Cellebrite
Cellebrite is a suite of tools designed primarily for mobile forensics, which allows easy acquisition of data from a mobile device so it can be processed in the tools covered in the section. 

#Evidence Analysis

### Autopsy
An autopsy is an open-source digital forensics tool that helps investigators analyze and extract evidence from various data sources, such as hard drives and mobile devices. It works by creating a forensic image of the target storage media and then running in-depth searches to quickly retrieve key information, such as recently used programs, deleted files, emails, visited websites, and much more. 

### Volatility
Volatility is a Python-based memory forensics framework that enables the analysis of memory dumps or memory images. It captures a snapshot of a computer's memory, allowing users to search for valuable information. This data aids in understanding the computer's past activities and uncovering potential evidence of malicious actions.

Volatility's versatility extends to analyzing memory from various operating systems, including Windows, Linux, and Mac OS, making it suitable for a wide range of scenarios. Moreover, it can recover deleted files that might be inaccessible through other means, enhancing its utility. 















