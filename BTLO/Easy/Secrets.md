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

# Question 5
