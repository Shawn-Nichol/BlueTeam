# Question 1
Check Wireshark endpoints and arrange columns based on the list. 
192.168.1.120


# Question 2
Interfaces

# Question 3
Cyber Kill Chain: The first step is reconnaissance. 
Filter wire shark with the following "frame contains Nmap"

Nmap, Post /sdk HTTP/1.1

# Question 4
192.168.90.1

# Question 5
arp scan

# Question 6
192.168.90.5

# Question 7
8009, 8080

# Question 8
Stream one of the 8080 captures, and you can analyze the content. From the stream, you can see that port is used to access a web page. 
HTTP

# Question 9
Wireshark filters
- tcp.stream eq 1390
- frame contains admin (frame 23259)

The content shows info shows login, drilling to the HTML Form URL encode menu, you can find the user and password. 
http://192.168.90.5:8080/scadaBR/login.tm, admin:admin



# Question 10
In frame 23259, look for the next request frame
23262
