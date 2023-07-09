# Docker Networking overview
Container networking refers to the ability for containers to connect to and communicate with each other, or to non-Docker workloads.
Networking allows containers to communicate with each other and with the host system. Containers run isolated from the host system and need a way to communicate with each other and with the host system.
By default, Docker provides two network drivers for you, the bridge and the overlay drivers.

docker network ls

NETWORK ID          NAME                DRIVER
xxxxxxxxxxxx        none                null
xxxxxxxxxxxx        host                host
xxxxxxxxxxxx        bridge              bridge
