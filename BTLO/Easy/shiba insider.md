Unzip the download file with 7z x file.zip

## file.zip
Obtain the password for the zip by running fcrack dictionary attack
```
fcrackzip -D -u -p /usr/share/wordlists/rockyou.txt file.zip
```
PASSWORD FOUND!!!!: pw == redforever


Unlock file.zip 


## Readme.txt
Shiba Dog has everything you need and decided that no more passwords will be needed 




## Insider.pcap
Wireshark stream results

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/32835828-7bc1-4220-b760-70b4af60290f)


There is a base64 encoded message "ZmFrZWJsdWU6cmVkZm9yZXZlcg==" which reads "fakeblue:redforever"

## ssdog1.jpeg
exiftool shows a couple of interesting lines. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/3cbf8d09-bc67-4fc5-bffa-cebba17c54a4)

After trying a couple of passwords, I recalled the README.txt file that said there were no passwords and ran steghide without entering a password to extract a new file, "idInsider.txt"

## Insider
0726ba878ea47de571777a

# Question 1
use your own password

# Question 2
redforever

# Question 3
No

# Question 4
Exiftool

# Question 5
Technique:Steganography

# Question 6
Steghide

# Question 7
0726ba878ea47de571777a

# Question 8
This answer is really tricky as the previous question gives you the user ID; after lots of digging and randomly entering the ID into different sites, someone mentioned looking up the ID on BTLO and entering the ID into the address bar. 
```
https://blueteamlabs.online/home/user/0726ba878ea47de571777a
```
This will take you bluetiger's profile


