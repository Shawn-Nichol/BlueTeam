AFter unziping the download there is a dd file. dd is commonly associated with disk image files. THese files often contain an exact copyo or clone of a stroage device such as a harddrive, USB thumb drive. 

The challange tags the following tools. 
- Photorec, File recovery software yused to retrieve lost files including images, videos, documents, and archives from various storage devices
- Audio Software
- Steghide: is used for hiding data within various files.
- fcrackzip: is a tool for crackign password protected zip files. 
- exiftool: A command-line application used for reading, writing and editing metadata information in files, particularly focusing on images files wehre EXIF data is embedded.

Use photorec to recover the files from the USB drive. 
```
photorec image.dd
```

**Report.xml**
Report of the photorec recover.

**f004**
file: indicate s that this Apple Desktop top service, stores meta data on folders apperance. 
Use the exiftool to extract meta data. 

```
ExifTool Version Number         : 12.67
File Name                       : f0047500.DS_Store
Directory                       : .
File Size                       : 8.2 kB
File Modification Date/Time     : 2023:12:03 22:13:20-07:00
File Access Date/Time           : 2023:12:03 22:16:53-07:00
File Inode Change Date/Time     : 2023:12:03 22:13:20-07:00
File Permissions                : -rw-r--r--
Error                           : Unknown file type

```



**jpg**
The 4 jpg pictures are from london. 

**f0000240_brown**
Use fcrackzip to unlock the zip folder. 
- b bruteforce
- u unzip
- c character usage


# Notes for future
Look at the meta data of the jpg. 

fcrack Brute ran for 15 minutes nothing came up try rockyou.txt file. 












