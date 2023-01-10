> # **Grid Computing**
> The use of widely distributed computer resources to reach a common goal. A computing grid can be thought of as a distributed system with non-interactive workloads that involve many files.  
>  
> Grid computing is distinguished from conventional high-performance computing systems such as cluster computing in that grid computers have **each node set to perform a different task/application**. Grid computers also tend to be more heterogeneous and geographically dispersed (thus not physically coupled) than cluster computers. Although a single grid can be dedicated to a particular application, commonly a grid is used for a variety of purposes. Grids are often constructed with general-purpose grid middleware software libraries. Grid sizes can be quite large. For certain applications, distributed or grid computing can be seen as a special type of parallel computing that relies on complete computers (with onboard CPUs, storage, power supplies, network interfaces, etc.) connected to a computer network (private or public) by a conventional network interface, such as Ethernet.  
>  
>  The primary **performance disadvantage** is that the various processors and local storage areas do not have high-speed connections. This arrangement is thus well-suited to applications in which multiple parallel computations can take place independently, without the need to communicate intermediate results between processors. The high-end scalability of geographically dispersed grids is generally favorable, due to the low need for connectivity between nodes relative to the capacity of the public Internet.
>  
  
> # **Computer Cluster**
> A **set of computers** that work together so that they can be viewed as a single system. Unlike grid computers, computer clusters have **each node set to perform the same task**, controlled and scheduled by software.  
>  
> The components of a cluster are usually connected to each other through fast local area networks, with each node (computer used as a server) running its own instance of an operating system. In most circumstances, all of the nodes use the same hardware and the same operating system. (In some setups, different OS and harwaress can be used.)
>  
>  The basic concept of the cluster computing is
> ```
> more computing power and better reliability by orchestrating a number of low-cost commercial off-the-shelf computers
> ```
> The activities of the computing nodes are orchestrated by "clustering middleware", a software layer that sits atop the nodes and allows the users to treat the cluster as by and large one cohesive computing unit, e.g. via a single system image concept.
> ## *Benefits*
> Clusters are primarily designed with performance in mind, but installations are based on many other factors. **Fault tolerance** (*the ability for a system to continue working with a malfunctioning node*) allows for ***scalability***, and in high-performance situations, ***low frequency of maintenance routines***, ***resource consolidation*** (e.g. RAID), and ***centralized management***. Advantages include enabling data recovery in the event of a disaster and providing parallel data processing and high processing capacity.
>  
> In terms of scalability, clusters provide this in their ability to add nodes horizontally. This means that more computers may be added to the cluster, to improve its performance, redundancy and fault tolerance. This can be an inexpensive solution for a higher performing cluster compared to scaling up a single node in the cluster. This property of computer clusters can allow for larger computational loads to be executed by a larger number of lower performing computers.
>  
> When adding a new node to a cluster, reliability increases because the entire cluster does not need to be taken down. A single node can be taken down for maintenance, while the rest of the cluster takes on the load of that individual node.
>  
> If you have a large number of computers clustered together, this lends itself to the use of distributed file systems and RAID, both of which can increase the reliability and speed of a cluster.