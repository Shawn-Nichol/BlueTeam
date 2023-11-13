# Router
A router is a network device that forwards data based on a logical address. In the case of TCP/IP networks, the router would forward data based on the IP addresses of systems. If you're on your home network and want to visit Google.com your request will go to the router (DNS will convert the domain name Google.com into the IP address), and your request will be sent over the internet to google.com web server IP. 

# Hub
A hub is a network device that connects all devices on a LAN. When a system sends data to the hub on one port, the hub will broadcast these to all other attached devices. Hubs can be referred to as dumb devices because they do not understand who is the intended recipient of the data that has been received, so it sends it to all devices. Although the data will eventually reach the intended system, it generates unnecessary traffic and can also allow attackers to steal data. If an attacker is connected to a hub, whenever any connected host sends data, it will be sent to every other host, including the attacker's machine. 

# Switch
A switch  works as a smart version of a hub because it actually understands where to send data instead of sending it to everyone; it achieves this by using MAC addresses as unique identifiers for recipients of incoming data, so it can send it to the right system. In this diagram below, if the Desktop Computer wants to print a document, it would send the request, which would reach the Network Switch, which will know to send it to the printer as the desktop computer will include the MAC address in the request (which is gained by using Address Resolution Protocol or ARP).

# Bridge 
A network bridge device connects separate networks to make them into one larger network. This is different than a router, which allows networks to be connected but work independently. In the OSI model, bridgin works at layer 2, the Data Link Layer. 

# Firewall
A firewall is a network device that provides fundamental network security by monitoring incoming and outgoing traffic and determining whether to allow or block it, based on rules. Firewalls can come in software form or hardware form as physical devices that are plugged into the network infrastructure. This allows us to create private networks, where only intended communication can come in or out. 



