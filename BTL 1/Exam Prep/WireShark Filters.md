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

Menu Statistics endpoints will list all the IP addresses and the size of communication data between points. 

Subnet
```
ip.addr == 192.168.1.0/24
```

Port filtering
```
tcp.port == 80
```

Multiple Ports
```
tcp.port == 80, or tcp.port == 443, or tcp.port == 8000, or tcp.port == 8001, tcp.port == 8002, or tcp.port == 8003, or tcp.port == 80
tcp.port in {80,443,8000..8005}
```

# Statistics conversations
Right-click the conversation, and you can set the filter. 


You can combine protocols.
```
tcp and dns
```

# Strings
Case senstive
```
ip contains "London"
```
Case insensitive 
```
ip matches "London"
```

```
eth matches "London"
```

# Filter out the noise
```
!(arp or stp or lldp or tcp.port{443})
```
From here, you can export the PCAP to a new file for easier analysis. 


# TCP Flags

```
TCP.analysis.flags
```
