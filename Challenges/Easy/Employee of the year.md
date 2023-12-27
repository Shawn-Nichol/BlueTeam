Download file

There will be three files/dir

The output dir contains some information; you can find the first flag here. 


CLI TOols
- find doesn't return any results
    - find -name "flag"*
- ls -R can provide a layout of the file structure
- xdg-open will open the file with the attended program
- eog used to open images file.

photorec recoverfiles.dd (restores files). 

Parted can show some disk information

The strings command will show file formats for the flags. 

# Flag 1
This can be found by viewing the PNG file

# Flag 2
XML files are actually part of a DOCX file; open the Documetns.xml file in the Word folder. Scanning the XML, you see base64 encryption towards the end of the file. Convert this base64 for the flag. 

# Flag 3
Navigate to the PDF folder. When you open the file, the PDF reads you found the flag. Use a tool like pdfinfo in Poopler utils to review the metadata of the PDF file. The author is the flag; some of the characters are still in ASCII format; ask ChatGPT to convert these characters. 

Linux commands to download popular utils. 
```
sudo apt-get install popular-utils

check metadata of PDF
pdfinfo filename.pdf
```


