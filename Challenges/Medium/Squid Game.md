# Question 1
I used Exiftool to review the file's metadata; nothing of note here. 

I tried numerous reverse image searches, all of which said the file size was too large. Knowing this image is used in squid games, I googled the Squid Game phone number, which ended up being the answer

86504006

# Question 2
Using Steghide, I was able to extract an additional file from the image. The password for Steghide is the phone number from the previous question. 

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/a335826b-a828-4d7f-bd20-d1e8a2389a75)


Dalgona.png

# Quesiton 3
I tried the following methods without any results. 
- exiftool
- strings
Next up was to use stegsolve to analyze the image. 

Stegsolve can downloaded with this command. 
wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar

Run stegsolve
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/ed03b47f-aaa3-4938-87d6-0b2bbcf741db)

Load the image and rotate through the analyze options. Gray bits will provide a readable text. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/ddb89b82-3e07-4ed4-b351-e0afa4aca0d3)


Red Pixel

# Question 4

