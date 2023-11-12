# What is Steganorgaphy
The practice of concealing messages or information within other non-secret text or data. An example of this would be having a text file that contains secret information which is hidden inside an innocent image file. 

steghide command hide message
- steghide - Selects the tool
Embed - selects the mode we want
- cf - selects file we want to hide data in
- ef - selects the file we want to embed

steghide command to extract the message
- extract selects the mode we want to use
- sf - selects the steganography file for extraction. 

# Quiz

## Question
Embed the file 'secretmessage.txt' inside the cover file 'coverfile.jpg' and name the output stegofile 'hiddenmessage.jpg'. What is the full command you would use to do this?

```
steghide embed -cf coverfile.jpg -ef secretmessage.txt

```

kAN105KS
## Question
Flag 1 is hidden inside a text file in one of the steganography files. What is the value?
passphrase: christmasstree
File: pizza.jpg
```
steghide extract -sf pizza.jpg
```
Answer: kAN105KS



## Question
Flag 2 is hidden inside a text file in one of the steganography files. What is the value?
passphrase: darksky123
File: verypretty.jpg
```
steghide extract -sf verypretty.jpg
```
Answer: 001JDANL



## Question
Flag 3 is hidden inside a text file in one of the steganography files. What is the value?
passphrase: goldenwatch
File: car.jpeg
```
steghide extract -sf car.jpeg
```
Answer: 1LRBA9IU

