# Challenge Brief
The SOC has received an anonymous report that a user is potentially exfiltrating data from the company. An image of the user’s hard drive has been taken, and you are responsible for analyzing the contents of a perfect copy to find any evidence of malicious activity. Using your newly developed skills, search through the folders and files using techniques to uncover 4 pieces of hidden information (each piece of evidence will contain the string {1 of 4} or similar). You will be tested on your ability to discover this information using all of the techniques taught in this course; Linux CLI navigation, identifying incorrect file extensions, identifying hidden files/folders, steganography, and password cracking.

# Useful Commands
ls -a (Allows us to identify files hidden using filenames beginning with “.” in the current directory)
cat/heads/strings (Allows us to potentially find hidden text strings in image and audio files, or read text files from the CLI)
fcrackzip (Allows us to crack password protected .zip files)
steghide (Allows us to retrieve files hidden in image and audio files)
file (Allows us to see what the true file-type of the file is, even if the extension has been changed to trick us)


unzip commands provide the following file structure
```
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip d516*               
Archive:  d516a04c5268783c085d5b86a56870ad64c51d42c8d6b8fcc4f58cd3bbf4f1c5dcdb2a3082cd44c1a1d07819dcde.zip
   creating: J Harrison Disk Image 10.09.2019/
   creating: J Harrison Disk Image 10.09.2019/Images/
  inflating: J Harrison Disk Image 10.09.2019/Images/laptop.jpg  
  inflating: J Harrison Disk Image 10.09.2019/Images/exploratory.jpg  
  inflating: J Harrison Disk Image 10.09.2019/Images/wireframe-design-guide.png  
  inflating: J Harrison Disk Image 10.09.2019/Images/website-stock-photo.jpg  
  inflating: J Harrison Disk Image 10.09.2019/Images/desk stock img.mp3  
  inflating: J Harrison Disk Image 10.09.2019/Images/office pic1.jpg  
  inflating: J Harrison Disk Image 10.09.2019/Images/drupal 8 logo Stacked CMYK 300.png  
  inflating: J Harrison Disk Image 10.09.2019/Images/office 2.jpg  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/
   creating: J Harrison Disk Image 10.09.2019/WebDev work/finished webpages/

  inflating: J Harrison Disk Image 10.09.2019/WebDev work/to do list  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/Links.txt  

  inflating: J Harrison Disk Image 10.09.2019/WebDev work/scan.xml  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/
 extracting: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/Power Free Website Template - Free-CSS.com.zip  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/to-do/
 extracting: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/to-do/.a0415ns.zip  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/img/
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/img/banner-bg.jpg  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/img/blog-post-1.jpg  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/js/
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/js/bootstrap.js  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/js/main.js  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/flexslider-icon.eot  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/flexslider-icon.ttf  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/fontawesome-webfont.ttf  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/fontawesome-webfont.svg  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/flexslider-icon.svg  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/FontAwesome.otf  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/fontawesome-webfont.woff  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/flexslider-icon.woff  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/fonts/fontawesome-webfont.eot  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/index.html  
   creating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/font-awesome.css  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/bootstrap.min.abc  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/templatemo_misc.css  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/bootstrap.min.css  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/animate.css  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/templatemo_style.css  
  inflating: J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/templatemo_508_power/css/owl-carousel.css  
 extracting: J Harrison Disk Image 10.09.2019/WebDev work/VERSION  

  inflating: J Harrison Disk Image 10.09.2019/WebDev work/WAF on OS Detection Nmap Scan.txt  
   creating: J Harrison Disk Image 10.09.2019/Payslips/

  inflating: J Harrison Disk Image 10.09.2019/Payslips/readme  

  creating: J Harrison Disk Image 10.09.2019/Saved Emails/
  inflating: J Harrison Disk Image 10.09.2019/Saved Emails/Website Update Report 01_10_2019.eml  
  inflating: J Harrison Disk Image 10.09.2019/Saved Emails/Form1.jpg  

   creating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/
   creating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 10/

  inflating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 10/posidon.xml  
  inflating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 10/tue  
   creating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 9/
  inflating: J Harrison Disk Image 10.09.2019/Weekly Meeting Notes/Week 9/Friday  

 extracting: J Harrison Disk Image 10.09.2019/.test  
```
# Root
```
ls -a 
```
shows a '.test' file

contents
```
this is a test
```


# Image folder 
'desk stock img.mp3' file extension has been altered; the file should be a jpeg.
```
mv 'desk stock'* desk.jpg
```
Using the password obtained from the Emails folder and steghide I was able to extract a password list from the laptop image.
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

# Payslips
A readme saying pay slips should emailed to personal address

# Saved Emails
Email file appears to be normal, reading the Form1.jpg file with strings command we can see an some critical information being shared. 
```
Simon, I have usernames and passwords for the VPN. Still on my work PC. Don't want to risk emailing them just yet. When I do, the file is a .jpg image + password for extraction is 
password
. Use steghide. Talk again soon

```


# Weekly Meeting

### Week 10
posidon file is a png that was converted to XML
```
mv posidon.xml posidon.png
```
The image contains a list of offices
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/9682114d-dc2f-40dc-9078-7ae6e09fb077)

The tue file contains nothing of note. 

### Week 9
Minutes from the meeting nothing of note. 


# WebDev work
scan file has an IP in it (10.10.10.35)

### unfinished webpages

#### Todo
There is unzip file that requires a password here. 
```
──(kali㉿kali)-[~/…/J Harrison Disk Image 10.09.2019/WebDev work/unfinished webpages/to-do]
└─$ fcrackzip -D -u -p /usr/share/wordlists/rockyou.txt .a0415ns.zip        


PASSWORD FOUND!!!!: pw == vendy13031988

```
List of Employees and their company information. 

