TCMPDump is a command-line tool, that can be used to capture newtork traffic and view and analyze PCAP capture files. TCP Dump has the benefit of not needing GUI access to a host in order to use it - this property is very useful when you have remote shell access, eg during a penetration test, and need to get an idea of the network traffic. Additionally, in some ways, TCPDump provides even more granular analysis and filtering capabilities, with the ability to have the output piped to other commands. 

TCMPDump may seem daunting to some people who are used to GUI-based toools and have graphical guidance from the tool. Alothough there are quite a large amount of command parameters that TCP Dump supports, only a limitied range of them needs to be learned for basic usage. You can see the available options with tcpdump- h, or read the manual with man tcpdump. 

# Cappturing traffic
You can specify an interface to capture from, apply traffic filtering and save the capture to a .pcap file. To start a capture with defaul settings, simply teyp the command tcpdump

To view the list of available interfaces that TCPDump can capture traffic on, use tcpdump -D. To start captruing on a specific interface, use tcpdump -i interface, e.g. tcpdump -i en0

You can also apply filters by using command-line options. To filter by source or destination host, use tcpdump src ip-address or tcpdump dsdt ip-address. To filter by port, add the port parameter and the port number, such as tcpdump dst port 25. To filter by protocol add the protocol name, such as tcpdump ftp. Also, just like wireshark, logical operators such as and & or can be used to chain terms. Lastly, to make TCPDump quit after capturing x number of packets, use the -c no option

# Analyzing PCAPs
To read a saved capture file with default settings, use tcpdump -r filename. Fore a more verbose output, the -v, -vv or -vvv options can be used, with each one increasing in verbosity. 

In the first line of each TCP packet, IP header inforamtion is displayed, inclduing the TTL, flags, Layer 4 protocol, length and gragmentation offset. The second line of each TCP packet, you can see the source IP address and port, the destination IP address and port, the TCP flag, checksum, sequence and acknowledgement numbers, window size, any options and header length. 

Specifying TCP flags
TO match all packets with a singl especified TCP flag, add the tcp[tcpflags] ==tcp-ack/tcp-syn/tcp-fin/tcp-push/tcp-urg/tcp-rst

Specifying packet header byts

You can specify any byt inthe packet header by using its index. FOr example, let's suppose that we want to display only ICMP Echo Request packets. We know that echo request have an ICMP type of 8. Since the type field in an ICMP header is th first byte. of the iCMP header shoul d hbave a value of 8. from this , we can constructo our expression as icmp[0] == 8. The same  applies for other protocol headersand values, such as ip[8] for TTL. 

Note taht you can sometimes replace the byte index with the name of the field that you are specifying. for example icmp[0] could be replaced with icmp[icmpttype]

