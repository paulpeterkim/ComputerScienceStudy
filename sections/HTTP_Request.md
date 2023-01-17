# **HTTP Request Methods**
> The Hypertext Transfer Protocol (HTTP) is a family of stateless, application-level, request/response protocols that share a generic interface, extensible semantics, and self-descriptive messages to enable flexible interaction with network-based hypertext information systems.  
  
> HTTP defines a set of **request methods** to indicate the desired action to be performed for a given resource. Although they can also be nouns, these request methods are sometimes referred to as *HTTP verbs*. Each of them implements a different semantic, but some common features are shared by a group of them: e.g. **a request method can be safe, idempotent, or cacheable**.
  
| HTTP Request Method | Description |
| :---: | :---: |
| GET | Requests a representation of the specified resource. Used for only retrieving the data. Defined to be SAFE. |
| HEAD | Asks for a response identical to GET, but without response body. Defined to be SAFE. | 
| POST | Submits an entity to the specified resource, often causing a change in state or side effects on the server. |
| PUT | Replaces all current representations of the target resource with the request payload. |
| DELETE | Deletes the specified resource. |
| CONNECT | Establishes a tunnel to the server identified by the target resource. |
| OPTIONS | Describes the communication options for the target resource. Defined to be SAFE. |
| TRACE | Performs a message loop-back test along the path to the target resource. Defined to be SAFE. |
| PATCH | Applies partial modifications to a resource. |
  
> [**GO TO HTTP Documentation**](https://httpwg.org/specs/)  
>   
> [**GO TO HTTP Semantics**](https://httpwg.org/specs/rfc9110.html)

[**To index**](../ComputerNetwork.md)  
[**To previous page**](TCP_IP.md)  
[**To next page**](../ComputerNetwork.md) 