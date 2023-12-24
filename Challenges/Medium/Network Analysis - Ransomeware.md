# Question 1
This took me forever to find. I was trying to use filters to find the result so you can obtain the information required by reviewing the Capture file properties in the statistic tab. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/e6319719-7a2b-42d9-b11e-fc3e4939721d)


32-bit Windows 7 Service Pack 1, Build 7601

# Question 2
In Wire Shark, use the following filter. 

```
http.request.method == "GET"
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/539ecdbf-d6ca-4d32-9317-865a0d208c27)


One result is returned. Viewing the HTTP information from the result, we can see the URI. </br>
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/f0f90dd3-292d-4d79-bce9-810e9506b386)


http://10.0.2.15:8000/safecrypt.exe
# Question 3

safecrypte.exe
# Question 4
Google the MD5 hash for safecrypte.exe

4A1D88603B1007825A9C6B36D1E5DE44
# Question 5
Review the detection tab on virus total; you'll see a Popular threat at the top. </br>

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/48e5d74e-c248-4252-9453-89f1a826519b)


Teslacrypt
# Question 6
The encryption type can be found in multiple places; the easiest one for me was the PNG file. 
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/d6d301ad-2780-40ac-991e-6e20e892075a)

RSA-4096
# Question 7
Information is avalable on virustotal. </br>

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/69e463af-96b6-46b0-af7a-3516782f3856)


dunyamuzelerimuzesi.com/
# Question 8
Use a Tesla Drcypting tool to open the document. 


BTLO-T3nd3r-Fl@g
