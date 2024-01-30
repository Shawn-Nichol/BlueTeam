# IP Address
Either source or destination
```
ip.addr == x.x.x.x
```

Source
```
ip.src == x.x.x.x
```

Destination
```
ip.dst == x.x.x.x
```

Menu Statistics endpoints will provide you with list of all the IP address and how many times it was hit. 

Subnet
```
ip.addr == 192.168.1.0/24
```

Port filtering
```
tcp.port == 80
```

Multple Ports
```
tcp.port == 80, or tcp.port == 443, or tcp.port == 8000, or tcp.port == 8001, tcp.port == 8002, or tcp.port == 8003, or tcp.port == 80
tcp.port in {80,443,8000..8005}
```

# Statistics conversations
Right click the conversation and you can set the filter. 


you can combine protocols
```
tcp and dns
```

# Strings
Case senstive
```
ip contains "London"
```
Case insensitve 
```
ip matches "London"
```

```
eth matches "London"
```
