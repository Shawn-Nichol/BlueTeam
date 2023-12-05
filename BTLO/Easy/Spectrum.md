After unzipping the download, there is a dd file. dd is commonly associated with disk image files. These files often contain an exact copy or clone of a storage device such as a hard drive or USB thumb drive. 

The challenge tags the following tools. 
- Photorec, File recovery software used to retrieve lost files, including images, videos, documents, and archives from various storage devices
- Audio Software
- Steghide: is used for hiding data within various files.
- fcrackzip: is a tool for cracking password-protected zip files. 
- ExifTool: A command-line application used for reading, writing, and editing metadata information in files, particularly focusing on image files where EXIF data is embedded.

## Photorec
Use photorec to recover the files from the USB drive. 
```
photorec image.dd
```

**Report.xml**
Report of the photorec recovery.

**f004**
file: indicates that this Apple Desktop top service, stores metadata on folder apperance. 
Use the exiftool to extract metadata. 


## Meta Data
Gather metadata from the images using exiftool

**f0047516.jpg**
**f0048140.jpg**
**t0048140.jpg**
Show nothing of note

**40048900.jpg**
exiftool, Artist: steghide password: cheese on toast




## Steghide Extract
use steghide extract, information 
```
steghide extract -sf t0048140.jpg -p "cheese on toast" 
```
**f0047516.jpg**
**f0048140.jpg**
**40048900.jpg**
**t0048140.jpg**

The images in the main directory contain no secrets that can be extracted with Steghide. 



## Unlock zip file
**f0000240_brown**
Use fcrackzip Dictionary attack to unlock the zip directory
- D Dictionary
- u unzip
- p dictionary file

```
fcrackzip -D -u -p /usr/share/wordlists/rockyou.txt f0000240_brown.zip
```
Password = garfield

## New Wave files
Pefromed steghide on all new files

The white.wav contained some hidden information. 
```
steghide extract -sf white.wave -p "cheese on toast"
```

## Stardate.txt
Some random characters: "56inrkS7AcAXatqrFM", utlize cyber chef to try and decode with a base. 
15:01:00
emit

This result is start part of the puzzle; emit is time backwards, so flip the time around
00:10:51


**location.wav**
Audio is Morse code and translated to 

N I C E T R Y , N O T H I N G T O H E A R H E R E !

Check Spectrum, as info can be hidden there. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/bc9932c2-daac-44cb-9e37-b2c583608583)












