# Router
- Creates larger networks by joining two network segments.
- Can route data from one network to another.
- Uses the destination IP address to forward packets.

# Switch
- Provides the connectivity points of an Ethernet network.
- Devices connect via twisted pair cabling, one-per-device.
- Collisions occur when two devices attempt to transmit at the same tie.
- Switches can operate in full-duplex because switches reduce the number of collisions.
- The method of switching dictates how the switch deals with the data it receives. Methods include:
	- [[Cut-through]]
	- [[Store-and-forward]]
	- [[Fragment-free]]

## Switch Cabling
- [[Medium-Dependent Interface Crossed]] (MDI-X)
- [[Medium-Dependent Interface]] (MDI)
	- If there is no MDI port, use the MDI-X with a crossover cable.
	- In a crossover cable, wires 1 & 3 and 2 & 6 are crossed.
- A multilayer switch can distribute incoming data to specific application servers and help distribute load.

# Firewall
- A networking device that controls access to an organization's network.
- Software firewalls are deployed through network operating systems.
- The last rule in the firewall access *should* be implicit deny.
- Uses inbound and outbound rules.
- Can protect internal networks from public networks, and can control access between specific network segments.

# Intrusion Detection System & Intrusion Prevention System
- IDS: Can detect the presence of an attack then log that information. Can also alert an admin to a potential threat.
- IPS: Device continually scans the network for inappropriate activity; can shut down potential threats.
- Several variations of IDS/IPS:
	- Behavior-based: Looks for variations in behavior to recognize potential threats.
	- Signature-based: MD-IDS / MD-IPS; evaluates attacks based on [[attack signatures]] and audit trails.
	- Network-based: N-IDS / N-IPS; examines all network traffic to and from network systems.
	- Host-based: H-IDS / H-IPS; anti-virus software.
- An IDS can detect malicious activity and send alerting messages, but it does **not** prevent attacks.
- An IPS protects hosts and prevents malicious attacks from the network layer up through the application layer.

# Load Balancer
- Holds and distributes data, maintains backups, secures network communications, etc.
- Load balancing: The workload is distributed among several devices
- Round-robin: Evenly distributing requests among servers
- Weighted round-robin: Allows admins to adjust the allocation of requests based on server capabilities or priorities.

# Proxy Server
- A server that sits between a client computer and the internet and looks at the webpage requests that the client sends.
- If the request is for the internet, it sends the request as if it made the request.
- When a caching proxy server answers a request for a web page, the server makes a copy of all or part of that page in its cache.
- Proxies can disallow website access done through an ACL.
- A reverse proxy resides near the web servers and responds to requests; often used for load balancing purposes.
- A proxy server can be used if users within a corporate network need to connect to the Internet but corporate network policy doesn't allow direct connections.

# Network Attached Storage
- NAS: Easier than SAN and uses TCP/IP
- Consists of one or more hard drives organized into logical storage volumes accessible over the network using NFS or SM?B.

# Storage-Area Networks
- SAN: A network of storage devices that can be accessed by multiple servers or computers, providing a shared pool of storage space. 

# iSCSI
- Logical Unit Numbers (LUNs) came from the SCSI world and carried over, acting as unique identifies for devices. Both NAS and SAN use "targets" that hold up to eight devices.
- Language of storage.

# Fiber Channel and FCoE
- Fiber channel: A technology that defines full gigabit per second data transfer over fiber-optic cable. Commonly used in SANs.
- Utilizes FCP.
- FCoE: Allows fiber channel to use 100 gigabit ethernet. This solves the problem of enterprises having to run parallel infrastructures for both LANs and SANs.

# Wireless Access Point
- WAP: A transceiver device used to create a WLAN.
- Additional WAPs are used to allow access to more wireless clients and expand the range of the wireless network.
- An AP/WAP can operate as a bridge connecting a standard wired network to wireless devices or as a router passing data transmissions from one AP to another.
- Can act as a switch, DHCP server, router, and firewall.

# Wireless LAN Controller
- Often used with remote office deployments for wireless authentication.
- When an AP boots, it authenticates with a controller before it can begin working as an AP.

# Applications / Content Delivery Network

## CDN
- A geographically distributed network of servers and data centers that work together to deliver multimedia web content. Typically involves:
	- [[Content replication]]
	- [[Request routing]]
	- [[Content delivery]]
	- [[Dynamic content acceleration]]
	- [[Load balancing and failover]]
	- [[Security]]

# Virtual Private Networks
- VPN: Encapsulates encrypted data inside another datagram that contains routing information.
- Point-to-Point Protocol (PPP): What the encrypted data is encapsulated in
- A VPN extends a LAN by establishing a remote connection using a public network.
- Components of the VPN Connection:
	- [[VPN client]]
	- [[VPN server]]
	- [[VPN headend]]
	- [[VPN concentrator]]
	- [[Access methood]]
	- [[VPN protocols]]
- VPNs support analog modems, ISDN, wireless connections, and dedicated broadband such as cable and DSL.
- Full-tunnel: All requests through the VPN are encrypted regardless of where the service is hosted, and it is not possible to access local network resources.
- Split-tunnel: All incoming requests are encrypted, but traffic going outside the client network does not go through the VPN server.

# SSL / TLS / DTLS
- TLS has replaced SSL for the most part.
- SSL VPN can be used to connect locations that would run into trouble with firewalls and NAT when used with IPSec.
	- It is known as an SSL VPN, whether or not TLS or SSL is used.
- DTLS is a derivation of SSL/TLS by OpenSSL aimed to increase reliability.

# Quality of Service
- QoS: The strategies used to manage and increase the flow of network traffic; enables admins to predict bandwidth use, monitor that use, and control it.
- Two categories of applications:
	- [[Latency sensitive]]
	- [[Latency insensitive]]

