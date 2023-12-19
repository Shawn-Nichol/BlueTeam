# Question 1
Here, you can use Linux CLI to count the number of "Failure Information" that occurred in the log file. 
```
cat BTLO_Bruteforce_Challenge.txt | grep "Failure Information" | wc -l 
```
3103

# Question 2
To identify the account that is being targeted, use the following command to print all user accounts listed in the log and compare the number of times the Account Name appeared to the number of failed events. 
```
cat BTLO_Brutefoce_Challenge.txt | grep "Account Name:" | sort | uniq -c
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/78e7d0e7-5962-4713-aa00-e33f153d2132)

administrator

# Question 3
This string can be found in the failed events. 

Unknown user name or bad password

# Question 4
The ID number can be located at the top of each event.  </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/670c1468-6c6c-4117-b985-8e08b4770270)

4625

# Question 5
The source IP can be located in the event. 

133.161.192.227
# Question 6
Use the IP address lookup site to identify the location of the IP address. 

Viet Nam

# Question 7
We can use roughly the same command we used throughout the challenge to identify the ports. 
```
cat BTLO_Brutefoce_Challenge.txt | grep "Source Port:" | sort | uniq
```
This will filter out duplicate Ports and organize them from highest to lowest, grabbing the lowest and highest ports. 

49162 -65534
