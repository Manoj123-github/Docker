# Docker Networking overview
Container networking refers to the ability for containers to connect to and communicate with each other, or to non-Docker workloads.
Networking allows containers to communicate with each other and with the host system. Containers run isolated from the host system and need a way to communicate with each other and with the host system.
By default, Docker provides two network drivers for you, the bridge and the overlay drivers.

**docker network ls**

<pre> NETWORK ID          NAME                DRIVER
      xxxxxxxxxxxx        none                null
      xxxxxxxxxxxx        host                host
      xxxxxxxxxxxx        bridge              bridge</pre>
# Types of Network Drivers

    **bridge:** If you build a container without specifying the kind of driver, the container will only be created in the bridge network, which is the default network. 
    **host:** Containers will not have any IP address they will be directly created in the system network which will remove isolation between the docker host and containers. 
    ** none:** IP addresses won’t be assigned to containers. These containments are not accessible to us from the outside or from any other container.
    **overlay:** overlay network will enable the connection between multiple Docker demons and make different Docker swarm services communicate with each other.
    **ipvlan:** Users have complete control over both IPv4 and IPv6 addressing by using the IPvlan driver.
    **macvlan:** macvlan driver makes it possible to assign MAC addresses to a container. 
