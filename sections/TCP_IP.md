# **TCP/IP (Transmission Control Protocol/Internet Protocol)**
  
> ***A set of standard rules that allows different types of computers to communicate with each other.*** **IP** ensures that each computer connected to Internet has unique serial number called IP address. **TCP** specifies how data is exchanged over the Internet and how it should be broken into **IP** packets. It also makes sure that the packets have information about the source, the destination, and the sequence in which the message data should be re-assembled. It also checks if the message has been sent corretly to the specified destination. TCP is also known as a connection-oriented protocol.
  
It is network model developed prior to [OSI model](OSI.md). It consists of 4 layers:  
1. Layer 4: Application Layer  
2. Layer 3: Transport Layer  
3. Layer 2: Internet Layer  
4. Layer 1: Network Access Layer (Data Link & Physical Layer)

Some authors compare TCP/IP with OSI model's 7 layers. Whilst doing that, they separated TCP/IP model's layer 1 into two different layers; data link layer and physical layer. Thus, in some reference, it is said that TCP/IP consists of 5 layers.  
> Layer 4 in TCP/IP Model is equivalent to *Application Layer, Presentation Layer, and Session Layer of OSI model* **combined**. Layer 1 in TCP/IP Model is equivalent to *Data Link and Physical Layer of OSI model* **combined**.
  
---  
## *Application Layer: Layer 4*
The application layer makes sure that **the data from the sending end is received in a format that is acceptable and supported** at the receiving end. It is responsible for handling high-level protocols, issues of representation. This layer **allows the user to interact** with the application. When one application layer protocol wants to communicate with another application layer, it **forwards its data to the transport layer** through socket.  
> Every application cannot be placed inside the application layer except **those who interact with the communication system**.
Protocols used in this layers are:
- [HTTP](InternetProtocols.md)
- [SNMP](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol)
- [SMTP](InternetProtocols.md)
- [DNS](DomainName_DNS.md)
- [TELNET](InternetProtocols.md)
- [FTP](InternetProtocols.md)
  
---
## *Transport Layer: Layer 3*
The transport layer is responsible for **the smooth transmission of data** from one end to the other. It is also responsible for **reliable connectivity, error recovery, and flow control** of the data. This is where TCP comes in. Thus this layer os sometimes called as TCP layer. (Sometimes UDP is used thus, UDP layer.)  
- TCP (Transmission Control Protocol):
    + It provides a full transport layer service to applications.
    + It creates **a virtual circuit between the sender and receiver**, and it is active for the duration of the transmission.
    + It **detects the error and retransmits the damaged frames**. Therefore, it ensures all the segments must be received and acknowledged before the transmission is considered to be completed and a virtual circuit is discarded.
    + At the sending end, TCP divides the whole message into smaller units known as segment, and each segment contains a sequence number which is required for reordering the frames to form an original message.
    + At the receiving end, TCP collects all the segments and reorders them based on sequence numbers.
- UDP (User Datagram Protocol):
    + It provides connectionless service and end-to-end delivery of transmission.
    + It **discovers the errors but does not specify them**, making them unreliable.
    + If UDP discovers error, ICMP reports existence of the error in the datagram to the sender.
    + There are four fields (Which are all 16 bits):
        * Source Port Address: The address of the application program that has created the message.
        * Desination Port Address: The address of the application program that receives the message.
        * Total length: The total number of bytes of the user datagram in bytes.
        * Checksum: A 16-bit field used in error detection.
    + UDP does not specify which packet is lost. UDP contains only checksum; it does not contain any ID of a data segment.
  
---  
## *Internet Layer: Layer 2*
This Internet layer **moves packets from source to destination** by connecting independent networks. This is where **IP** comes in. Thus this layer is cometimes called as IP layer. It is also called as **network layer**. Movement of packet is irrespective of the route they take.  
  
Responsibility of IP are:  
- [IP addressing](IPaddress.md)
- Host-to-host communication: Determines the path where the data is to be transmitted through. 
- Data encapsulation and formatting: It receives data from *transport layer* then encapsulates the data into **IP datagram**. This ensures that the data is sent and received securely.
- Fragmentation and reassembly: The limit imposed on the size of the IP datagram by *network access layer* is known as **Maximum Transmission Unit (MTU)**. If size of IP datagram is greater than the MTU, IP splits the datagram into smaller pieces. Fragmentation is carried out by the sender or intermediate router. At the receiver side, all the fragments are reassembled.
- Routing: When IP datagram is sent through local networks(LAN, MAN, WAN), it is known as **direct delivery**. When sender and receiver are on the distant networks, the datagram has to be sent indirectly. This is done by routing by devices called as routers.  
  
Some other protocols are:   
- ARP (Address Resolution Protocol):
    + A network layer protocol which is used to **find the physical address** from the IP address.
    + **ARP request** is when a sender wants to know the physical address of the device and broadcasts a request to the network. Every device attached to the network will accept the ARP request and process the request.
    + **ARP reply** is when the recipient recognize the IP address and sends back its physical address to the sender. Only the specified recipient sends back ARP reply to the sender's ARP request. The recipient adds the physical address to its cache memory and to the datagram header.
- ICMP (Internet Control Message Protocol):
    + A mechanism used by the hosts or routers to send notifications regarding **datagram problems** back to the sender.
    + A datagram travels from router-to-router until it reaches its destination. If a router is unable to route the data because of some unusual conditions such as disabled links, a device is on fire or network congestion, then the ICMP protocol is used to inform the sender that the datagram is undeliverable.
    + **ICMP test** is used to test whether the destination is reachable or not.
    + **ICMP reply** is used to check whether the destination device is responding or not.
    + ***The core responsibility of the ICMP protocol is to report the problems, not correct them. The responsibility of the correction lies with the sender.***
    + ICMP can send the messages only to the source, but not to the intermediate routers because the IP datagram carries the addresses of the source and destination but not of the intermediate routers that it is passed to.
---
## *Network Access Layer: Layer 1*
As mentioned earlier, some authors separate this layer into additional two layers; data link layer and physical layer. The network access layer sees how **a computer connects to a network, physically**. Thus, it is mainly reponsible for the transmission data between two devices on the same network. The functions carried out by this layer are **encapsulating the IP datagram into frames** transmitted by the network and mapping of IP addresses into physical addresses. Protocols used in this layer are:  
- Ethernet
- Token ring
- FDDI
- X.25
- Frame relay  
  
These are all protocols used in LAN.  
  
---
[**To index**](../ComputerNetwork.md)  
[**To previous page**](NetworkModels.md)  
[**To next page**](OSI.md)  