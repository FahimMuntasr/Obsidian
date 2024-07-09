# IP Addresses

IP addresses are usually a 32bit binary number represented in decimal form, which is assigned to each device connected to the internet. IP addresses are used to specify your origin and identity. 

IP addresses with a 32bit/4byte length are of the 'IPv4' type 
As there are only 32 bits, the total number of possible combinations are ; $2^{32}=4,294,967,296$

IP addresses with a 128bit/6byte length are of the 'IPv6' type
As there are only 128 bits, the total number of possible combinations are ; $2^{128}=3.402823*10^{38}$ 

IP addresses are of two types ; Private and Public
Private IP addresses usually start with 192.168.xxx.xxx;

Private IP addresses on a same network send their traffic through a single public IP address, this reduces the number of unique addresses needed. This is done using Network Address Translation (NAT).

`IPv4 and IPv6 addresses are layer 3 protocols.`
# MAC Addresses

Every single electronic device with networking capabilities has a unique Media Access Control (MAC) Address. This address reveals information about the physical device and its manufacturer.  

`MAC Addresses are layer 2 protocols.`
# TCP, UDP, and the Three-Way Handshake
TCP : Transmission control protocol
UDP: User datagram protocol
Three-Way Handshake;
- A `SYN` packet is sent, this requests a connection with the destination.
- If the destination is online and ready, a `[SYN,ACK]` packet is sent letting the user know that the destination is open and ready.
- After this the user sends an `ACK` packet which acknowledges the established connection.
# Common Ports and Protocols
TCP
- FTP (21)
- SSH (22)
- Telnet (23)
- SMTP (25)
- DNS (53)
- HTTP (80)
- HTTPS (443)
- POP3 (110)
- SMB (139+445)
- IMAP (143)
UDP
- DNS (53)
- DHCP (67,68)
- TFTP (69)
- SNMP (161)

# The Open Systems Intercommunication (OSI) Model

| Layer # | Name         | examples                |
| ------- | ------------ | ----------------------- |
| 1       | Physical     | data cables             |
| 2       | Data         | Switches, MAC addresses |
| 3       | Network      | IP addresses, routing   |
| 4       | Transport    | TCP/UDP                 |
| 5       | Session      | session management      |
| 6       | Presentation | PNG, JPEG, MOV          |
| 7       | Application  | HTTP, SMTP              |

# Subnetting  

| CIDR           | Subnet          | Hosts | Network     | Broadcast     |
| -------------- | --------------- | ----- | ----------- | ------------- |
| 192.168.0.0/22 | 255.255.252.0   | 1022  | 192.168.0.0 | 192.168.3.255 |
| 192.168.1.0/26 | 255.255.255.192 | 62    | 192.168.1.0 | 192.168.1.63  |
| 192.168.1.0/27 | 255.255.255.224 | 30    | 192.168.1.0 | 192.168.1.31  |
