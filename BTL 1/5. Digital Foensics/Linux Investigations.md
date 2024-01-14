/etc/passwd is used to keep track of every registered user that has access to the system

etc/shadow file is readable only by the root account to prevent standard users from grabbing the contents and then using a tool such as hashcat or John the Ripper to brute force perform a dictionary attack or use Rainbow tables to crack the hashes and reveal the plain text passwords. 

/var/lib/dpkg/status. This file includes a list of all installed software packages. 

