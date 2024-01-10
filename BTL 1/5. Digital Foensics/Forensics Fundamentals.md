# Order of Volatility

1. Registers & Cache
The contents of the CPU and registers are extremely volatile since they are constantly changing. An investigator needs to retrieve data from the cache and register immediately before that evidence is lost. 

2. Memory
The information located on Random Access memory can be lost if there is a power spike or if the system is disconnected from power. This is a fast, temporary type of memory in which programs, applications, and data are stored.

3. Disk
Once data is overwritten, it is impossible to recover it, and SSDs have the additional risk of Garbage Collection or TRIM deleting files that could be used as evidence.

4. Remote Logging and Monitoring data

The potential for remote logging and  monitoring data to change is much higher than data on a hard drive, but the information is not as vital. 

5. Physical COnfiguration, Network Topology, Archival Media
Here, we have items that are either not vital regarding the data or are volatile. The physical configuration and network topology are information that could help an investigation but will likely not have a tremendous impact. Finally, archived data will usually be located on a separate physical device, such as a USB or external hard drive.


# File Carving
It is the process of searching for files in a data stream and is used to carve deleted files from disk images so we can investigate files that a user has deleted, provided they haven't been overwritten. 


# Memory Analysis
Refers to the analysis of volatile data in a computer memory dump. 

# Memory Dump
a snapshot capture of computer memory data from a specific instant. A memory dump can contain valuable forensic data about the state of the system before an incident, such as a crash or security compromise, such as running processes, New York connections, and malware that doesn't take the form of files but instead resides purely in memory. 

# Pagefile
is used within Windows OS to store data from RAM when it becomes full. The pagefile.sys is a continuous file, so it can be read more quickly.

# Deleting Pagefile.sys
pagefile.sys is hidden from the normal Windows users by default, as it is a system that Windows identifies as important in the normal operation of the system. If the file is deleted fully then the system will not function correctly and is likely to become unstable, however, the system can be configured to store the pagefile.sys onto another hard drive. 
