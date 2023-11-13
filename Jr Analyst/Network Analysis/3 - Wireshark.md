# Wireshark
Promiscuous mode allows Wireshark to capture packets that are received on an interface but not actually addressed to the host, for example, frames transmitted on a wireless network with different MAC addresses. This allows Wireshark to capture other hosts' traffic and have a broader picture of the network. 


Viewing Capture statistics
Wireshark collects different statistics about the traffic in the capture file - such as the percentage proportions of protocols, the amount of bytes transmitted to different hosts, and the IP addresses of all the hosts that have appeared in the same capture. They are helpful in certain scenarios, such as finding potential exfiltration vectors and identifying the exfiltrating host based on network usage. 


Protocol Hierarchy
The protocol hierarchy window displays the percentages of packets or bytes in a protocol conversation against the entire traffic. The protocols are organized in layers from Layer 2 to Layer 7

Conversations
The conversations window also provides a wealth of information on the traffic, including which hosts communicated to which hosts, on which ports, and a total of how many bytes and packets were in the conversation. This window is great for identifying the different MAC or IP addresses that a host has communicated with and the volume of traffic between them. 

Similar to the protocol hierarchy windows, the Conversations window can be very helpful in investigating data exfiltration attempts, as it can identify the attacker by IP address. If a host has been transmitting many packets and bytes to an unidentified IP address without receiving many packets in return, an exfiltration could have been occurring. 

Endpoints
Lastly, the Endpoints window shows all of the different hosts that appear in the capture and the amount of packets/bytes they sent and received. This window is useful in sorting hosts by their network activity, by either transmission or receiving volume, or by both. 

If a host has been receiving much more traffic than they have been transmitting, the host is probably downloading a large file. On the other hand, if the host has been transmitting more than they have been receiving, the host is probably uploading files or backing up to remote storage, such as the cloud. 
