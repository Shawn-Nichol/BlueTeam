# Question
What is the phrase on line 8 of the first text file you come across?

use command head
```
└─$ head asda*
1 ..'.'.;.
2'###.#.#\
3/'#./#/#/#'
4;;==-\...1
5'\']\[===1111
6\[11\;l.]'1]'\
71;];];\[1]1...
there's a snake in my boot
9
10
```

Answer: there's a snake in my boot

# Question
How many images are in the /Home/PersonalFiles/Photos/ directory?

```
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Photos]
└─$ ls
betterdays.jpg  happyfamily.jpg  pexels-photo-457882.jpeg
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Photos]
└─$ file betterdays*
betterdays.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 100x100, segment length 16, progressive, precision 8, 460x300, components 3
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Photos]
└─$ file happyfamily.jpg
happyfamily.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 96x96, segment length 16, comment: "CREATOR: gd-jpeg v1.0 (using IJG JPEG v62), quality = 85", progressive, precision 8, 450x300, components 3
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Photos]
└─$ file pexels*        
pexels-photo-457882.jpeg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, progressive, precision 8, 500x333, components 3
                                                                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Photos]
└─$ 

```
Answer: 3

# Question
There are two files with incorrect extensions, what are their filenames? (Without the file extensions)

doggo, pancakerecipe.txt


# Question
One of these incorrect extension files hides a message, what is it?

SIERRA ECHO CHARLIE ROMEO ECHO TANGO

# Quesiton
There is a text file with the string “bankdetails” as part of the filename. What is the full filename?

Answer:  11_09_2019_statement_bankdetails.txt 

# Question
What is the flag value inside the text file within the hidden directory?

```
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Work Stuff]
└─$ ls -a
 .   ..   11_09_2019_statement_bankdetails.txt  'Meeting Notes'   .Private
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/…/SBT_Linux_CLI-2/Home/PersonalFiles/Work Stuff]
└─$ cd .Private    
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/…/Home/PersonalFiles/Work Stuff/.Private]
└─$ ls   
readme.txt
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/…/Home/PersonalFiles/Work Stuff/.Private]
└─$ strings readme.txt    
106019BAL0S0A1

```

106019BAL0S0A1







