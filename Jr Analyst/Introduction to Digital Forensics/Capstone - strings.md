
Could this be one

```
┌──(kali㉿kali)-[~/Downloads/J Harrison Disk Image 10.09.2019/Payslips]
└─$ strings readme
Note to self, stop leaving payslips on my work PC. Just email them to personal address and print off at home

```
# String 2
```
──(kali㉿kali)-[~/Downloads/J Harrison Disk Image 10.09.2019/Images]
└─$ steghide extract -sf laptop*              
Enter passphrase: 
wrote extracted data to "passwords".
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Downloads/J Harrison Disk Image 10.09.2019/Images]
└─$ strings passwords           
{2/4}
a123456
vincent
Usuckballz1
spooky
```


# String 3
```
┌──(kali㉿kali)-[~/Downloads/J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 10]
└─$ file *
posidon.xml: PNG image data, 162 x 147, 8-bit/color RGB, non-interlaced
tue:         ASCII text

┌──(kali㉿kali)-[~/Downloads/J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 10]
└─$ mv posidon.xml posidon.png   
```




![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/dfde5b00-484c-481c-8289-6025d9d135ca)



# String 4
```
┌──(kali㉿kali)-[~/…/WebDev work/unfinished webpages/templatemo_508_power/css]
└─$ head boot*   
==> bootstrap.min.abc <==
/*!
 * Bootstrap v3.1.1 (http://getbootstrap.com)
 * Copyright 2011-2014 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */

/*! {Part 4 of 4}
 * This is in case Colin tries to screw me. I'll expose him.
 * Colin Andrews
 * 31 years old

```
