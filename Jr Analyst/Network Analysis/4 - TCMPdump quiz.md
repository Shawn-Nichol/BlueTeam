PCAP 4
# Question
How many UDP packets have been captured?
```
tcpdump -r SBT-PCAP4.pcap udp | wc -l
```
3200

# Question
How many TCP packets have both the SYN and ACK flags set?
```
tcpdump -r SBT-PCAP4.pcap 'tcp[tcpflags] & (tcp-syn|tcp-ack) == (tcp-syn|tcp-ack)' | wc -l
```
20


# Question
Which version of Chrome was used to connect to securityblue.team?
```
tcpdump -A -r SBT-PCAP4.pcap | grep -E "Chrome|securityblue.team"
```
Chrome/80.0.3987.87 

# Question
How many packets have a TTL value of 38?
 ```
tcpdump -r SBT-PCAP4.pcap 'ip[8] == 38' | wc -l
```
710

PCAP 5
# Question
What is the name of the PNG file on the webserver at 192.168.56.111?
```
tcpdump -A -r SBT-PCAP5.pcap | grep .png
```
proprietary.png

# Question
Which version of OpenSSH is running on the server?
```
tcpdump -vvv -r SBT-PCAP5.pcap | grep OpenSSH
```
OpenSSH-7.9p1

# Question
On which port is the .zip file being served?
```
tcpdump -A -n -l -r SBT-PCAP5.pcap | grep ".zip"
```
3016

# Question
When was a packet with a TCP checksum value of 53203 captured? (Format: xx:xx:xx.xxxxxx)
```
tcpdump -x -r SBT-PCAP5.pcap "tcp[16:2]=53203"  
```
06:04:46.207925
