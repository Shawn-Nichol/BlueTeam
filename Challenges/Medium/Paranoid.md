# Question 1

Using aureport you can use the following command
```
aureport -if audit.log --auth 
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/0ac0fc1f-745b-4abd-a112-09415360ad5c)
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f8a55a5f-4797-401d-947c-81a099e13753)

btlo
# Question 2
You can see multiple attempts to access the system, so this looks like a brute force or a dictionary attack.
Brute Force
# Question 3
You'll see the IP address pop up multiple times in the previous search query. 

192.168.4.155 

# Question 4
Use the tty command to view keystrokes. 

```
aureport -if audit.log --tty
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/c7b7b3b3-f243-4080-86c6-62c824390765)


linpease

# Question 5
Looking at the result from the previous question, you can see another command called evil.tar.gz that was entered. When filtering the log, you can identify the PID that is associated with evil. 

```
aureport -if audit.log --tty
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/d7fc2c29-e3e9-4a14-a4b9-ce5f21d03428)

evil, 829992

# Question 6

Google "Binary executino to gain linux root CVE"
https://blog.aquasec.com/cve-2021-3156-sudo-vulnerability-allows-root-privileges

CVE-2021-3156 

# Question 7
Google CVE-2-21-3156, and NIST will describe the CVE. 

heap-based buffer overflow

# Question 8
Using the TTY flag that was used earlier, we can review the key commands after the last "whoami" and will see a cat command was entered to view a file before exiting. 
```
aureport -if audit.log --tty
```

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/62ac9d13-c36e-472a-a991-ce72ffe0a9cb)


