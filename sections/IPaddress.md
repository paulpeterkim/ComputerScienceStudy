# **IP Address**
> **IP Address** : A unique address that identifies a device on the internet or a local network. It stands for "Internet Protocol." It is string of four numbers separated by periods. (***Thus, 32 bits.***) IP addresses are not random it is allocated by IANA(or InterNIC) (both are divisions of the ICANN).  
 
| Types | Explanation | Examples | 
| :---: | :---: | :---: |
| Comsumer IP addresses | Every individual or business with an internet service plan has this IP addresses, private IP address and public IP address | 
| Private IP addresses | Every device that connects to your internet network has a private IP address. Router generates private IP addresses that are unique identifiers for each device that differentiate them on the network. | IP address of your computer, phone, and other electronics that is connected to your router. | 
| Public IP addresses | A public IP address is the primary address associated with your whole network. Each device with its unique private IP addresses is included within the 'main' public IP address. | IP address of your router. | 
| Public IP addresses (Dynamic) | Changes automatically and regularly. Usually ISP changes its customer's IP address for cost savings. | IP address of router that has IP address provided by ISP. |
| Public IP addresses (Static) |  IP address remains consistant. | IP address of Sogang University. |
  
For wep hosting there is two types of IP addresses.
| Types of WHIP | Explanation | 
| :---: | :---: |
| Shared IP addresses | Websites that rely on shared hosting plans from web hosting providers have this IP address. |
| Dedicated IP addresses | Some web hosting plans (such as *Dedicated Server Hosting*) will give you this IP addresss. This can make obtaining an SSL certificate easier and allows you to run your own File Transfer Protocol (FTP) server. |
  
**There are 5 classes of TCP/IP networks**  
IP address of class A~C are composed of 1) Network Part and 2) Host Part.  
1) Network part is assigned by InterNIC or IANA.  
2) Host part is assigned by the owner of the network.  
  
**Subnet mask tells which bits are used for network part. For bytes where subnet mask is 0, corresponding byte can only have range 1-254.**
  
| Class | Network Part of IP Address | Host Part of IP Address | Subnet masking | Application |
| :---: | :---: | :---: | :---: | :---: |
| A | First **8 bits**. (First byte.) First byte has range of **0-127**. (First bit of first byte is always 1.) | Remaining **24 bits**. (Remaining 3 bytes.) | 255.0.0.0 | Large number of hosts. | 
| B | First **16 bits**. (First 2 bytes.) First byte has range of **128-191**. (First bit of first byte is always 1, and the second bit is 0.)| Remaining **16 bits**. (Remaining 2 bytes.) | 255.255.0.0 | Usually an organization. (ex. Sogang Univ.) | 
| C | First **24 bits**. (First 3 bytes.) First byte has range of **192-223**. (First two bits of first byte are always 1, and the third bit is 0.)| Remaining **8 bits**. (Remaining 1 byte.) | 255.255.255.0 | Used for LAN (Local Area Network) | 
| D | First byte has range of **224 to 239**. (First three bits of first byte are always 1, and the fourth bit is 0.) | - | NA | Reserved for multi-tasking. | 
| E | First byte has range of **240 to 254**. (First four bits of first byte are always 1, and the fifth bit is 0.) | - | NA | Reserved for research and development purposes. |  

[**To index**](../ComputerNetwork.md)  
[**To previous page**](Hosting.md)  
[**To next page**](DomainName_DNS.md)  