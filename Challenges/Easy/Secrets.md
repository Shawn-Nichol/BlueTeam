### String
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJmbGFnIjoiQlRMe180X0V5ZXN9IiwiaWF0Ijo5MDAwMDAwMCwibmFtZSI6IkdyZWF0RXhwIiwiYWRtaW4iOnRydWV9.jbkZHll_W17BOALT95JQ17glHBj9nY-oWhT1uiahtv8

It appears to be JSON Web Token (JWT). JWT are encoded strings that consist of three parts. 

### Header
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9
```
"alg":"HS256"
```

### Payload
eyJmbGFnIjoiQlRMe180X0V5ZXN9IiwiaWF0Ijo5MDAwMDAwMCwibmFtZSI6IkdyZWF0RXhwIiwiYWRtaW4iOnRydWV9
```
flag: BTLs_4_Eyes,
iat: 90_000_000, (timestamp)
name: GreatExp,
admin: true
```

### Signature
jbkZHll_W17BOALT95JQ17glHBj9nY-oWhT1uiahtv8

The signature is created by combining the "Header + Payload" + Secret


Dots are separate these parts. 



# Question 1
JWT

# Question 2

Header, Payload, Signature

# Question 3

# Question 4
Use hashcat to crack the brute force of the secret key. 
- Copy the JWT into a text file.
- Run Hashcat on the text file
```
hashcat jwt.txt -a 3 ?a?a -i --increment-min=2 --increment-max=10 --show
```
-a 3: specifies a brute-force attack
?a?a: This mask represents a two-character password where each character can be either lowercase or uppercase
-i: This flag instructs Hashcat to perform an incremental mode attack starting from the minimum length of 2 up to a max length of 10 characters. </br>

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/e4fe6977-c17f-41f5-905c-9fdb5d3669f8)


bT!0

# Question 5
Know too create a new JWT, Go to a site like "jwt.io" to edit the existing JWT. 

- Paste the original JWT into the encoded token box. 
- Edit the Payload so admin reads false
- Enter the signature found in question 4 in Verify Signature box, and deselect "secret base64 encoded"

![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/67b9a825-1c8e-4d59-a123-f9a77a4165de)

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJmbGFnIjoiQlRMe180X0V5ZXN9IiwiaWF0Ijo5MDAwMDAwMCwibmFtZSI6IkdyZWF0RXhwIiwiYWRtaW4iOmZhbHNlfQ.nMXNFvttCvtDcpswOQA8u_LpURwv6ZrCJ-ftIXegtX4

