# **Uniform Resource Locator (URL) (A.K.A web address)**
> A reference to a web resource that ***specifies its location on a computer network and a mechanism for retrieving it***. It is a ***specific type of Uniform resource Identifier (URI).*** Its most common use is to reference web pages (HTTP) but are also used for file transfer (FTP), email (mailto), database access (JDBC), and many other applications. 
  
The format **combines the pre-existing system of domain names with file path syntax**, where slashes are used to separate directory and filenames. 
Every HTTP URL conforms to the syntax of a generic URI.   
  
An Internationalized Resource Identifier (IRI) is a form of URL that includes Unicode characters. All modern browsers support IRIs. The parts of the URL requiring special treatment for different alphabets are the domain name and path. 
1. The domain name in the IRI is known as an Internationalized Domain Name (IDN). (Explained above.)
2. The URL path name can also be specified by the user in the local writing system. If not already encoded, it is converted to UTF-8, and any characters not part of the basic URL character set are escaped as hexadecimal using percent-encoding. The target computer decodes the address and displays the page.
  
[**To index**](../ComputerNetwork.md)  
[**To previous page**](URI.md)  
[**To next page**](InternetProtocols.md)  