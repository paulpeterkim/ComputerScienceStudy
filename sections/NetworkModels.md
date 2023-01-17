# **Network Models**

The ***main aim*** of these layered architecture are to divide the design into smaller pieces. This divides unmanageably large tasks into smaller and manageable tasks. This modularity provides independence of layers, which makes it easier to understand, modify, test, and implement.  
  
Each lower layer adds its services to the higher layer to provide a full set of services to manage communications and run the applications. The number of layers, functions, contents of each layer will vary from network to network. However, the purpose of each layer is to provide the service from lower to a higher layer and hiding the details from the layers of how the services are implemented.  
  
The basic elements of layered architecture are:  
* **Service**: A set of actions that a layer provides to the higher layer.
* **Protocol**: A set of rules that a layer uses to exchange the information with peer entity. (How header is constructed.)
* **Interface**: A way through which the message is transferred from a one layer to another layer. That is, the data is passed through interface from upper to lower layer. A clean-cut interface makes it so that minimum information is shared amoing different layers and ensures that the implementation of one layer can be easily replaced by another implementation.   
  
In a layer *n* architecture, layer *n* on one machine will have a communication with the layer *n* on another machine and the rules used in a conversation are known as a *layer-n protocol*. In case of layered architecture, no data is transferred from *layer n* of one machine to *layer n* of another machine. Instead, ***each layer passes the data to the layer immediately just below it, until the lowest layer is reached***. ***Below layer 1 is the physical medium through which the actual communication takes place.*** 

> # [**TCP/IP Model**](TCP_IP.md)
---
> # [**OSI Model**](OSI.md)
---


[**To index**](../ComputerNetwork.md)  
[**To previous page**](URL.md)  
[**To next page**](InternetProtocols.md) 