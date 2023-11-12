# Protectign a Zip file
By encrypting files with passwords,  individuals and organizations can safeguard confidential information from unauthorized access. This security measure ensures that potentially incriminating or sensitive data remains protected, preserving its integrity and chain of custody. 

However, from the digital forensics perspective, password-protected ZIP files present challenges, as investigators need to crack these passwords to access their contents and uncover potential evidence. 

Zip a file and set a password.
- Zip selects the tool
- encrypt - selection the function of the tool we want to use. Afterwards, we will need to provide a password to access the file
- Protected.zip - The name of the outputted Zip file
- text.txt the we want to compress.
```
zip --encrypt Potected.zip text.txt
```


# Brute-Force Attacks
Sometimes, investigators will encounter password-protected zipped archives or zipped malware during an investigation with no reference  to what the password could be. 

Zip cracking is vital in digital forensics for accessing encrypted evidence, uncovering hidden information, completing data pictures, and building strong legal cases. It allows investigators to retrieve password-protected files, revealing crucial evidence and supporting investigations in court. 

However, it must be conducted lawfully and ethically to ensure the integrity of the process and the admissibility of evidence. 

### Pros of using brute-force attack?
The obvious pro of using this method is that you will always get the password. Because you are trying every possible combination, you will eventually crack the password and gain access, but this comes with major downside. 

If you have information such as the length of the password, you will cut down the number of possibilities dramatically. This can be applied to other attacks such as cracking account credentials - if you know the password policy or requirements, you can reduce the number of possibilities significantly. 


### Cons of using Brute-force attacks?
The attack method takes time. A lot of time. If you started with AAAAA, the next guess would be AAAAB, and the next guess would be AAAAC. It's going to take a very long time to get the right password, and each additional character is going to add a lot more possibilities. 

Brutefore attack
- fcrackzip - Selecting the tool
- -b - Selecting the option for a brute-force attack
- BrutForceAttack.zip, the file we want to brute-force
- -u - This makes sure fcrackzip actually tries to unzip the file; without this, we won't actually get the right password
- -c - this is where we pick the characters we want to use in our dictionary attack. ex a represent lowercase letters, and 1 represents numbers 0-9
- -l - This where we state the length of the password we want to crack. 

```
fcrackzip -b BruteForceAttack.zip -u -c a1 -l 4
```

Cheat sheet
(https://manpages.ubuntu.com/manpages/trusty/man1/fcrackzip.1.html)https://manpages.ubuntu.com/manpages/trusty/man1/fcrackzip.1.html


# Dictionary Attacks
Dictionary attacks use wordlists, which are collections of thousands of passwords, each on their own separate line in a text document. These are fed into tools, which will attempt to use each password one after the other until it receives the correct password or runs out of entries to try. 

### Pros
This attack method can be really quick. At the end of the day, you're trying to find a password that a human has set, and humans are usually predictable. By trying known passwords, you're more likely to find the password than if you were cracking it using brute force due to the nature of the entries you are trying. 

### Cons
If the password you're looking for isn't in the  wordlist you're using, then you won't get into the entity you're trying to gain access to. You could leave your computer running for 3 days trying different wordlists, but if it's not in there, you will never gain access. 

Rockyou.txt wordlist is pre-installed on Kali computers.


Dictionary attack
- fcrackzip - Selecting the tool
- -D - selecting the option for a dictionary attack
- -u - This makes sure fcrackzip actually tries to unzip the file; without this we won't actually get the right password
- -p - Use strings as passwords
- /usr/share/wordlists/rockyou.txt - Location of password list
- DictionaryAttack.zip - the file you want to crack

```
fcrackzip -D -u -p /usr/share/wordlists/rockyou.txt
DictionaryAttack.zip
```

cheat sheet
https://manpages.ubuntu.com/manpages/trusty/man1/fcrackzip.1.html






