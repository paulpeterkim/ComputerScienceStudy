> # **Hosting**
>> Store (a website or other data) on a server or other computer so that it can be accessed over the internet.  
>> Hosting is basically the computer, a network infrastructure, that keeps my website available across the internet.  
>   
> | Types | Description | Characteristics |
> | :---: | :---: | :---: |
> | Shared Hosting | My website will be stored on the same server as multiple other websites. | All domains share the same server resources (Ex. RAM, CPU). |
> | Virtual Private Server (VPS) Hosting | Each website is hosted within its own space on the server. | Shares a physical server with other users but not resources. |
> | Dedicated Server Hosting | The server is exclusively rented. | Full root and admin access. |
> | Cloud Hosting | Many computers working together, running applications using combined computing resources. | Works via a network. Can employ as many resources as they need without having to build and maintain their own computing infrastructure. Resources that are being used are spread across several servers. |
> | Managed Hosting | Hosting companies provide technical services such as hardware and software setup and configuration, maintenance, hardware replacement, technical support, patching, updating and monitoring. | I don't have to manage server, it is managed by the provider. |
> | Colocation | ‘Co-locate' server equipment by renting space in a colocation center. | The center will provide the power, bandwidth, IP address and cooling systems that your server requires. Space is rented out in racks and cabinets. |
> | Reseller Hosting | Web hosting business model in which a Web hosting provider allows some or all of their Web hosting services to be sold by an individual or third party organization. | Enables an organization to act as a Web hosting provider without the need to build, operate and manage a Web hosting infrastructure. |
> ## *Migration*
> Transferring to new web hosting provider.
  

> # **IP Address**
>> **IP Address** : A unique address that identifies a device on the internet or a local network. It stands for "Internet Protocol." It is string of four numbers separated by periods. (***Thus, 32 bits.***) IP addresses are not random it is allocated by IANA(or InterNIC) (both are divisions of the ICANN).
> | Types | Explanation | Examples | 
> | :---: | :---: | :---: |
> | Comsumer IP addresses | Every individual or business with an internet service plan has this IP addresses, private IP address and public IP address | 
> | Private IP addresses | Every device that connects to your internet network has a private IP address. Router generates private IP addresses that are unique identifiers for each device that differentiate them on the network. | IP address of your computer, phone, and other electronics that is connected to your router. | 
> | Public IP addresses | A public IP address is the primary address associated with your whole network. Each device with its unique private IP addresses is included within the 'main' public IP address. | IP address of your router. | 
> | Public IP addresses (Dynamic) | Changes automatically and regularly. Usually ISP changes its customer's IP address for cost savings. | IP address of router that has IP address provided by ISP. |
> | Public IP addresses (Static) |  IP address remains consistant. | IP address of Sogang University. |
> 
> For wep hosting there is two types of IP addresses.
> | Types of WHIP | Explanation | 
> | :---: | :---: |
> | Shared IP addresses | Websites that rely on shared hosting plans from web hosting providers have this IP address. |
> | Dedicated IP addresses | Some web hosting plans (such as *Dedicated Server Hosting*) will give you this IP addresss. This can make obtaining an SSL certificate easier and allows you to run your own File Transfer Protocol (FTP) server. |
> 
> **There are 5 classes of TCP/IP networks**  
> IP address of class A~C are composed of 1) Network Part and 2) Host Part.  
> 1) Network part is assigned by InterNIC or IANA.  
> 2) Host part is assigned by the owner of the network.  
> 
> **Subnet mask tells which bits are used for network part. For bytes where subnet mask is 0, corresponding byte can only have range 1-254.**
> 
> | Class | Network Part of IP Address | Host Part of IP Address | Subnet masking | Application |
> | :---: | :---: | :---: | :---: | :---: |
> | A | First **8 bits**. (First byte.) First byte has range of **0-127**. (First bit of first byte is always 1.) | Remaining **24 bits**. (Remaining 3 bytes.) | 255.0.0.0 | Large number of hosts. | 
> | B | First **16 bits**. (First 2 bytes.) First byte has range of **128-191**. (First bit of first byte is always 1, and the second bit is 0.)| Remaining **16 bits**. (Remaining 2 bytes.) | 255.255.0.0 | Usually an organization. (ex. Sogang Univ.) | 
> | C | First **24 bits**. (First 3 bytes.) First byte has range of **192-223**. (First two bits of first byte are always 1, and the third bit is 0.)| Remaining **8 bits**. (Remaining 1 byte.) | 255.255.255.0 | Used for LAN (Local Area Network) | 
> | D | First byte has range of **224 to 239**. (First three bits of first byte are always 1, and the fourth bit is 0.) | - | NA | Reserved for multi-tasking. | 
> | E | First byte has range of **240 to 254**. (First four bits of first byte are always 1, and the fifth bit is 0.) | - | NA | Reserved for research and development purposes. |  
> 

> # **Domain name and DNS (Domain Name System)**
>   
>> **For simplicity, it gives your IP address simple and easy to remember names.** You can have more than one domain name per IP address (and vice versa). In fact, this is what makes *shared hosting* work, since shared hosting hosts multiple web sites with a single machine. (Of course, HTTP requires hostname as part of request so that the host can determine which web site to show. This is elaborated in section *Internet Protocols*.)  
>   
> A **distinct subset** of the internet with addresses sharing a common suffix or under the control of a particular organization or individual.
> In other words, **a string that identifies** a realm of administrative autonomy, authority, or control (ex. SIP, Domain Keys in e-mail systems, and URI.) within the Internet is a domain name. It is used in various networking contexts and for application-specific naming and addressing purposes. It is often used to identify services provided through the Internet; that is, it **identifies a network domain, an IP resource, or a server computer**. Individuals will mostly use domain names to identify network domains. This abstraction allows any resources to be moved to a different physical location in the address topology of the network, both globally and locally.  
>   
> Then, what is network domain? **Network domain** is an administrative grouping of multiple private computer networks or local hosts within the same infrastructure. As mentioned earlier, domains can be identified using a domain name; domains which need to be accessible from the public Internet can be assigned a globally unique name within the Domain Name System (DNS).  It is common practice to use **Domain controller**.
>   
> **Domain controller** is a server computer that **responds to security authentication** within a computer network domain, that is, it authenticates users and stores user account information while enforcing security policy of the domain. It is a network server that is responsible for allowing host access to domain resources. They are typically deployed as a cluster to ensure high-availability and maximixze reliablilty.  
>   
> So how are domain names formed? They are formed by the rules and procedures of the ***Domain Name System (DNS)***. Structure of DNS is as follows.   
> 1. **Domain name space**  
>     * Consists of a tree of domain names.
>         - ***The domain name itself consists of the label, concatenated with the name of its parent node on the right, separated by a dot.***
>         <br><p align="center"><img src="DNS_schema.svg" alt="Making Domain Name" style="width:50%;"/></p>
>     * Each node(or leaf) of the tree has a *label* and zero or more *resource record (RR)*, which holds information associated with the domain name. 
>     * The tree sub-ivides into *zones* beginning at the DNS root zones. They are managed by a **name server**.  
>         <br><p align="center"><img src="Domain_name_space.svg" alt="Schema of Domain Name Space" style="width:50%;"/></p>
>         - DNS zone may consit as many domain and sub domains as the zone manager chooses.  
>         - DNS can be partitioned according to the *class* (which is like an array of parallel namespace tree).  
>         - Administrative responsibility for any zone may be divided by creating additional zones. Authority over the new zone is said to be *delegated* to a designated name server. The parent zone ceases to be authoritative for the new zone.
> 2. **Domain name syntax, internationalization** 
>     * The definitive descriptions of the rules for forming domain names. (Look for RFC 1035, RFC 1123, RFC 2181, and RFC 5892)
>     * The right-most label conveys the top-level domain (TLD). (ex. .com, .net, .org, .edu {These are also called 'generic TLD or gTLD'}])
>     * The right-most label may also conveys the country code top-level domain(ccTLD). (ex. .kr)
>     * IANA also ***reserves*** a set of special domain names. ***(ex. example, local, localhost, and test)***
>     * The hierarchy of domains descends from right to left. Each label to the left specifies a subdivision, or subdomain of the domain to the right. (Second Level Domain = SLD)
>         - These are usually administered by a *domain name registrar* who sell its its services to the public.
>         - This means a tree with sub domains as root is delegated to them. 
>     * This tree of subdivisions may have up to 127 levels, each with distinct label.
>     * Each label may contain 0-63 octets(characters). 
>         - The null label (of the zero length) is reserved for the root zone.
>         - The full domain name may not exceed the length of 253 characters in its textual representation.
>     * ***Hostname*** is a domain name that has at least one associated IP address. Usually TLDs are not hostnames, but if a ccTLD has an IP address, it can be a hostname.
>     * ICANN approved the Internationalizing Domain Names in Applications (IDNA) system. Thus, we can map Unicode strings into valid DNS character set using Punycode.
> 3. **Name servers**
>     * The Domain Name System is maintained by a *distributed database system*, which uses the client–server model. ***The nodes of this batabase are the name servers.***
>     * Each domain has at least one authoritative DNS server that publishes information about that domain and the name servers of any domains subordinate to it. 
>     * *Authoritative name server*
>         - A name server that only gives answers to DNS queries from data that have been configured by an original source.
>         - An authoritative name server can either be a primary server or a secondary server. 
>             1. A primary server is a server that stores the original copies of all zone records.
>             2. A secondary server uses a special automatic updating mechanism in the DNS protocol in communication with its primary to maintain an identical copy of the primary records.
>         - Every DNS zone must be assigned a set of authoritative name servers. 
>   
> ## *Domain name Registration*
> * Administrative contact: A registrant usually designates an administrative contact to manage the domain name.
>     - usually has the highest level of control over a domain.
>     - installs additional contact information for technical and billing functions.
> * Technical contact: The technical contact manages the name servers of a domain name.
    - assures conformance of the configurations of the domain name with the requirements of the domain registry
    - maintains the domain zone records
    - provides continuous functionality of the name servers (that leads to the accessibility of the domain name)
> * Billing contact: The party responsible for receiving billing invoices from the domain name registrar and paying applicable fees.
> * Name servers

> # **Uniform Resource Identifier (URI) (Superset of URL!!!)**
>> ***A unique sequence of characters*** that ***identifies*** a logical or physical resource used by web technologies. URIs may be used to identify anything, including real-world objects, concepts, or information resources. Some URIs provide a means of **locating and retrieving information resources on a network** (either on the Internet or on another private network, such as a computer filesystem or an Intranet); these are ***Uniform Resource Locators*** (URLs). Other URIs provide only a unique name, without a means of locating or retrieving the resource or information about it, these are Uniform Resource Names (URNs).  
> ```
> ─── URI 
>     ├── URL (locating and retrieving information)
>     └── URN (Only provide unique name) 
> ```
> URIs are used to identify anything described using the Resource Description Framework (RDF).  
> 
> ***A Uniform Resource Name (URN)*** is a URI that identifies a resource by name in a particular namespace. A URN may be used to talk about a resource without implying its location or how to access it. (ex. ISBN {or International Standard Book Number})  
>   
> ***A Uniform Resource Locator (URL)*** is explained in section *Uniform Resource Locator (URL) (A.K.A web address)*.  
> 
> ## *Syntax*
>> A URI has a scheme that refers to a specification for assigning identifiers within that scheme. As such, the URI syntax is **a federated and extensible naming system** wherein each scheme's specification may further restrict the syntax and semantics of identifiers using that scheme. The URI generic syntax is a superset of the syntax of all URI schemes.  
>   
> A URI is composed from an allowed set of ASCII characters consisting of **reserved characters** (*generic*: :, /, ?, #, [, ], and @; *scheme- or implementation-specific*: !, $, &, ', (, ), *, +, ,, ;, and =), **unreserved characters** (uppercase and lowercase letters, decimal digits, -, ., _, and ~), and **the character %**.  
>   
> Syntax components and subcomponents are separated by *delimiters* from the *reserved characters* (only from generic reserved characters for components) and define *identifying data* represented as unreserved characters, reserved characters that do not act as delimiters in the component and and subcomponent respectively, and percent-encodings when the corresponding character is outside the allowed set or is being used as a delimiter of, or within, the component. A percent-encoding of an identifying data octet is a sequence of three characters (consisting of the character % followed by the two hexadecimal digits representing that octet's numeric value) and is used for internationalization.  
>   
> The URI generic syntax consists of five components organized hierarchically in order of decreasing significance from left to right.  
> ```
> URI = scheme ":" ["//" authority] path ["?" query] ["#" fragment]
> ```
> A component is undefined if it has an associated delimiter and the delimiter does not appear in the URI; the scheme and path components are always defined. A component is empty if it has no characters; the scheme component is always non-empty.  
>   
> The authority component consists of subcomponents.
> ```
> authority = [userinfo "@"] host [":" port]
> ```
> <br><p align="center"><img src="URI_syntax_diagram.svg" alt="Diagram of URI Syntax" style="width:100%;"/></p>
> 
> The URI comprises:  
> * A non-empty **scheme** component followed by a colon (:), consisting of a sequence of characters beginning with a letter and followed by any combination of letters, digits, plus (+), period (.), or hyphen (-). 
>     - **Schemes** are case insensitive.
>     - Canocical form is lowercase and documents that specify schemes must do so with lowercase letters. 
>     - They should be registered with the IANA. (non-registered schemes are sometimes used.)
>     - Examples: http, https, ftp, mailto, file, data, irc, and etc...
> * An optional **authority** component preceded by two slashes (//), comprising:
>     - An optional **userinfo** subcomponent followed by an at symbol (@), that may consist of a user name and an optional password preceded by a colon (:).
>         + Use of the format username:password in the userinfo subcomponent is deprecated for security reasons. 
>     - A **host** subcomponent, consisting of either a registered name (including but not limited to a hostname) or an IP address. 
>         + IPv4 addresses must be in dot-decimal notation, and IPv6 addresses must be enclosed in brackets ([]).
>     - An optional **port** subcomponent preceded by a colon (:), consisting of decimal digits.
> * A **path** component, consisting of a sequence of path segments separated by a slash (/).
>     - A path is always defined for a URI, though the defined path may be empty (zero length). 
>     - A segment may also be empty, resulting in two consecutive slashes (//) in the path component. 
>     - A path component may resemble or map exactly to a file system path but does not always imply a relation to one.
>     - If an authority component is defined, then the path component must either be empty or begin with a slash (/). If an authority component is undefined, then the path cannot begin with an empty segment—that is, with two slashes (//).
>     - By convention, in **http** and **https** URIs, the last part of a path is named **pathinfo** and it is optional. 
>         + It is composed by zero or more path segments that do not refer to an existing physical resource name but to a logical part that has to be passed separately to the first part of the path (aka query part) that identifies an executable module or program managed by a web server.
> * An optional **query** component preceded by a question mark (?), consisting of a query string of non-hierarchical data. Its syntax is not well defined, but by convention is most often a sequence of attribute–value pairs separated by a delimiter (& and :).
>     - An http or https URI containing a pathinfo part without a query part may also be referred to as a 'clean URL' whose last part may be a 'slug'.
> * An optional **fragment** component preceded by a hash (#). 
>     - The fragment contains a fragment identifier providing direction to a secondary resource, such as a section heading in an article identified by the remainder of the URI. 
>     - When the primary resource is an HTML document, the fragment is often an id attribute of a specific element, and web browsers will scroll this element into view.
>   
> The scheme- or implementation-specific reserved character + may be used in the scheme, userinfo, host, path, query, and fragment, and the scheme- or implementation-specific reserved characters '!', '$', '&', ''', '(', ')', '*', ',', ';', and '=' may be used in the userinfo, host, path, query, and fragment. Additionally, the generic reserved character ':' may be used in the userinfo, path, query and fragment, the generic reserved characters '@' and '/' may be used in the path, query and fragment, and the generic reserved character '?' may be used in the query and fragment.
>   
## *Examples*
```URI
          userinfo       host      port
          ┌──┴───┐ ┌──────┴──────┐ ┌┴┐
  https://john.doe@www.example.com:123/forum/questions/?tag=networking&order=newest#top
  └─┬─┘   └───────────┬──────────────┘└───────┬───────┘ └───────────┬─────────────┘ └┬┘
  scheme          authority                  path                 query           fragment

  ldap://[2001:db8::7]/c=GB?objectClass?one
  └┬─┘   └─────┬─────┘└─┬─┘ └──────┬──────┘
  scheme   authority   path      query

  mailto:John.Doe@example.com
  └─┬──┘ └────┬─────────────┘
  scheme     path

  news:comp.infosystems.www.servers.unix
  └┬─┘ └─────────────┬─────────────────┘
  scheme            path

  tel:+1-816-555-1212
  └┬┘ └──────┬──────┘
  scheme    path

  telnet://192.0.2.16:80/
  └─┬──┘   └─────┬─────┘│
  scheme     authority  path

  urn:oasis:names:specification:docbook:dtd:xml:4.1.2
  └┬┘ └──────────────────────┬──────────────────────┘
  scheme                    path
```
> # **Uniform Resource Locator (URL) (A.K.A web address)**
>> A reference to a web resource that ***specifies its location on a computer network and a mechanism for retrieving it***. It is a ***specific type of Uniform resource Identifier (URI).*** Its most common use is to reference web pages (HTTP) but are also used for file transfer (FTP), email (mailto), database access (JDBC), and many other applications. 
>   
> The format **combines the pre-existing system of domain names with file path syntax**, where slashes are used to separate directory and filenames. 
> Every HTTP URL conforms to the syntax of a generic URI.   
>   
> An Internationalized Resource Identifier (IRI) is a form of URL that includes Unicode characters. All modern browsers support IRIs. The parts of the URL requiring special treatment for different alphabets are the domain name and path. 
> 1. The domain name in the IRI is known as an Internationalized Domain Name (IDN). (Explained above.)
> 2. The URL path name can also be specified by the user in the local writing system. If not already encoded, it is converted to UTF-8, and any characters not part of the basic URL character set are escaped as hexadecimal using percent-encoding. The target computer decodes the address and displays the page.
# **Internet Protocols**
