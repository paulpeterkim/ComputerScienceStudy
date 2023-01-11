# **Internet Protocols**
## *What is internet?*
The internet is just a network between regions, intranet is opposite of internet and will be elaborated in different section. The *Internet* (proper noun) is a collection of **packet** switching full-duplex networks connected by **routers** following **TCP/IP protocol**.   
| Types of networks | Desc. |
| :---: | :---: |
| Circuit switching net. | Data is sent as single packet,that is, there is no division of data. |
| Packet switching net. | Data is divided into smaller segments calles **packets** with its metadata as *header*. Each packet may follow different route to destination, but there is sequence information in header which allows sorting of packets to decipherable data. | 
| Half-duplex net. | One way transmission from sender to receiver. |
| Full-duplex net. | Two way transmission between sender and receiver | 
| Local Area Network (LAN) | A network that connects computing devices in the same relative vicinity. | 
| Wide Area Networ (WAN) |  A network that is geographically boundless, and instead relies on DNS protocols and IP addresses. |
  
*More about LAN and WAN will be elaborated in another section.* Then what is TCP/IP protocol? These are Internet protocols.  
  
> Internet Protocols are a set of ***rules that governs the communication and exchange of data over the internet***. Both the sender and receiver should follow the same protocols in order to communicate the data. 
## *Working of internet protocol*  
The internet and many other data networks work by organizing data into small pieces called **packets**. Each data sent between two network devices are divided into smaller packets by underlying hardware and software. Each ***network protocol defines the rules for how its data packets must be organized in specific ways according to the protocols the network supports***. Each packet has header which contain metadata of the packet. 
## *Necessity of protocols*
Protocols are needed to **manage the flow control of data and access control** of the link being shared in the communication channel. We need to manage flow control of data because different networks, located different parts of the world, may have different data transfer rates, which will result in data loss. Also, if the access control is not managed, that is, the node whch will access a server at a particular instant of time is not managed, many computers simultaneously sending data will result in collision of transmitted data. This collision of data causes corruption and loss of data.  
## *Types of internet protocol*
| Types | Description |
| :---: | :---: | 
| [TCP/IP (Transmission Control Protocol/Internet Protocol)](TCP_IP.md) | ***A set of standard rules that allows different types of computers to communicate with each other.*** **IP** ensures that each computer connected to Internet has unique serial number called IP address. **TCP** specifies how data is exchanged over the Internet and how it should be broken into IP packets. It also makes sure that the packets have information about the source, the destination, and the sequence in which the message data should be re-assembled. It also checks if the message has been sent corretly to the specified destination. TCP is also known as a connection-oriented protocol. | 
| SMTP (Simple Mail Transfer Protocol) | Used when **sending and distributing outgoing e-mails**. SMTP uses the header of the mail to get the e-mail id of the receiver and enters the e-mail into the queue of outgoing mails. As soon as the e-mail is delivered to receiving e-mail id, the e-mail is removed from the queue. |
| PPP (Point to Point Protocol) | A communication protocol used to create **a direct connection between two communicating devices**. It defines rules using which two devices will authenticate with each other and exchange information with each other. ex. connecting two routers, connecting PC to ISP. |
| FTP (File Transfer Protocol) | **File transferring protocol**. Works on a client-server model. When a machine requests for file transfer from another machine, the FTP sets up a connection between the two and authenticates each other using their ID and Password. |
| SFTP (Secure File Transfer Protocol) | It is also known as ***SSH FTP***. Protocol of **file transfer over SSH (Secure Shell)**. SFTP acts as extension to SSH and encrypts data(and file) then sends them over a SSH data stream. It is used to remotely connect to other systems while executing commands from the command line. (Commands are encypted by SSH.) |
| HTTP (HyperText Transfer Protocol) | Used to **transfer hypertexts (such as HyperText Markup Language (HTML)) over the internet** and is defined by the World Wide Web (WWW) for information transfer. It defines how the information needs to be formatted and transmitted. It also defines the various actions the web browser should take in response to the calls made to access a particular web page. Whenever a user opens website using web browser, one is indirectly using HTTP as this is the protocol being used to share text, images, and other multimedia files over the WWW. |
| HTTPS (HyperText Transfer Protocol Secure) | An extension to HTTP, that is, secure version of HTTP. **Used for secure communication over a computer network with the SSL/TLS protocol for encryption and authentication**. |
| TELNET (Terminal Network) | A standard TCP/IP protocol **used for virtual terminal service given by ISO**. It enables one local machine to connect with another. The computer which is being connected is called a remote computer and which is connecting is called the local computer. TELNET operation **lets us display anything being performed on the remote computer in the local computer**. This operates on the client/server principle. The local computer uses the telnet client program whereas the remote computer uses the telnet server program. |
| POP3 (Post Office Protocol 3) | It has **two Message Access Agents (MAAs) when one is client MMA and another is server MAA** for accessing the messages from the mailbox. It helps us to **retrieve and manage e-mails from the mailbox on the receiver mail server to the receiver's computer**. This is implied between the receiver and receiver mail server. It can also be called as one way client server protocol. ***POP3 WORKS ON THE 2 PORTS I.E. PORT 110 AND PORT 995.*** |
| UDP (User Datagram Protocol) | A substitute communication protocol to TCP implemented primarily for creating loss-tolerating and low-latency linking between different applications. |
| Gopher | A collection of rules implemented for searching, retrieving as well as displaying documents from isolated sites. Gopher also works on the client/server principle. |
  
> Note: Hypertext is a texts file of the special format that can contain links to other texts.
## *Some other protocols*
- Address Resolution Protocol (ARP)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Address_Resolution_Protocol)
- Dynamic Host Configuration Protocol (DHCP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)
- Internet Message Access Protocol (IMAP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol)
- [Session Initiaion Protocol (SIP)](SIP.md)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Session_Initiation_Protocol)
- Real-Time Transport Protocol (RTP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Real-time_Transport_Protocol)
- Resource Location Protocol (RLP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Radio_resource_location_services_protocol)
- Route Access Protocol (RAP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Routing_protocol)
- Layer Two Tunneling Protocol (L2TP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Layer_2_Tunneling_Protocol)
- Point to Point Tunneling Protocol (PPTP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Point-to-Point_Tunneling_Protocol)
- Simple Network Management Protocol (SNMP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol)
- Trivial File Transfer Protocol (TFTP)&nbsp;&nbsp;&nbsp;&nbsp;[(To Wiki)](https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol)
  
[**To index**](../ComputerNetwork.md)  
[**To previous page**](URL.md)  
[**To next page**](TCP_IP.md)  