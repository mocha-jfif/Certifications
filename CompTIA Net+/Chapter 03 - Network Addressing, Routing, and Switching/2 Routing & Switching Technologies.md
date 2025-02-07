# The Default Gateway
- <mark style="background: #BBFABBA6;">The router's IP address</mark>
- <mark style="background: #BBFABBA6;">Packets are forwarded to the destination network through the gateway.</mark>

# Routing Tables
- <mark style="background: #BBFABBA6;">A chart that helps determine the best possible path for data to travel.</mark>
- The routing table has:
	- <mark style="background: #BBFABBA6;">Network destination:</mark> the host IP address
	- <mark style="background: #BBFABBA6;">Netmask:</mark> the subnet mask value for the destination parameter
	- <mark style="background: #BBFABBA6;">Gateway:</mark> where the IP address is sent
	- <mark style="background: #BBFABBA6;">Interface:</mark> address of the interface that is used to send the packet to the destination.
	- <mark style="background: #BBFABBA6;">Metric:</mark> Measurement of directness of a route; the lower the metric, the faster the route.

# Static Routing
- Routes and route information are manually added into routing tables.
- <mark style="background: #BBFABBA6;">The route add command adds a static route to the routing table. The -p flag makes the static route persistent.</mark>

# Default Route
- <mark style="background: #BBFABBA6;">One static route is defined as the default route to be used if no other route is known.</mark>
- All packets with unknown destination addresses are sent to the default route.
- Used in dynamic routing.

# Switching Methods
- <mark style="background: #BBFABBA6;">To allow entities to communicate, communication paths move the information from one location to another and back. This is referred to as switching.</mark> Two methods: packet and circuit.

## <font color="#c3d69b">Packet Switching</font>
- Messages are broken into smaller pieces called packets.
	- Each packet has an assigned source, destination, and intermediate node address.
	- All of this is required because packets don't always used the same route. (Independent routing)
- The sending device is responsible for choosing the best path.
	- The path may change in transit and the packets may come out of order. The receiving device waits until all packets arrive, then reconstructs them based on each packet's sequence number.
- Two methods:
	- Virtual-circuit packet switching:
		- Logical connection is established between the source and destination device. It remains active until all packets are sent, or devices go offline.
	- Datagram packet switching:
		- Packets are independently sent so they are individually addressed. This way, packets avoid high traffic routes. Primarily used on the internet.

## <font color="#c3d69b">Circuit Switching</font>
- Requires a dedicated physical connection between the sender and receiver.
- When communication is done, the connection is terminated.
- Reliable, but burdensome.

# Dynamic Routing
- Routers use special routing protocols to communicate.
- They pass information about themselves to other routers so they can build routing tables.
- <mark style="background: #BBFABBA6;">Distance-vector router communications:</mark> Each router on the network communicates all the routes it knows to the routers to which its directly attached.
	- The routers use these updates to update their routing tables.
	- These updates are sent automatically every 30-60 seconds, depending on the routing protocol.
	- [[convergence]]
- <mark style="background: #BBFABBA6;">Link-state protocol:</mark> Builds a map of the entire network, then holds it in memory.
	- Routers send LSAs that contain information about networks to which they connect. These are sent to all routers on the network.
- Most popular routing protocols:
	- <mark style="background: #BBFABBA6;">Border Gateway Protocol (BGP):</mark>
		- Hybrid of distance-vector and link-state.
		- Can be used between gateway hosts on the internet.
			- Communicates using TCP.
			- Supports the use of autonomous system numbers (ASNs), which are globally unique numbers used by connected groups of IP networks that share the same routing policy.
	- <mark style="background: #BBFABBA6;">EIGRP:</mark>
		- Enables routers to exchange information more efficiently by using neighbor routing information and query these tables to find the best route.
			- Uses Diffusing Update Algorithm (DUAL) to determine the best route to destination.
	- <mark style="background: #BBFABBA6;">Open Shortest Path First (OSPF):</mark>
		- A link-state routing protocol on the shortest path first algorithm.
			- Each router using OSPF sends a list of its neighbors to other routers on the network, then the routers can determine the network design and shortest travel path.
- <mark style="background: #BBFABBA6;">Communication between distance-vector routers is called hops.</mark>
	- Tracert in Windows is used to see how many hops a packet takes to reach a destination (traceroute on Mac and Linux)
		- IPv6 version is tracert -6, traceroute 6, and traceroute -6. 
- <mark style="background: #BBFABBA6;">Routing loops:</mark>
	- Can occur on networks with slow convergence.
	- Occurs when the routing tables on the routers are slow to update and a redundant communication cycle is created between routers. Two strategies to combat this:
		- <mark style="background: #BBFABBA6;">Split horizon:</mark> 
			- Prevents the router from advertising a route back to the other router from which it was learned.
		- <mark style="background: #BBFABBA6;">Poison reverse:</mark>
			- Dictates that the route is advertised back on the interface from which it was learned, but it has a hop count of infinity, which tells the node that the route is unreachable.
- Distance-vector protocols have three problems:
	- The periodic update system can slow updates down.
	- The periodic updates can generate large and unnecessary traffic.
	- Incorrect information can be propagated, creating loops.

# Route Selection
- [[Administrative Distance]]
	- Can be manually assigned or assigned by a routing protocol's algorithm.
	- The lower the better; 0-255.
	- Routes are prioritized based on administrative distance.
- <mark style="background: #BBFABBA6;">Prefix length (subnet mask / subnet prefix):</mark> When multiple routes exist for the same destination network, the router selects the rout with the longest prefix length; known as the longest prefix match algorithm.

# Address Translation
- Capable communication between networks with incompatible addressing schemes; can be achieved by translating IP addresses and/or port numbers in the IP headers of packets (usually a firewall or router does this)

## Network Address Translation
- <mark style="background: #BBFABBA6;">NAT:</mark>
	- Many computers can "hide" behind a single IP address.
	- Using NAT means that only one registered IP address is needed in the system's external interface, acting as the gateway between internal and external networks.
- NAT allows for any address scheme on the internal network for internal networks.
- You can statically map a specific internal IP address to a specific external one (one-to-one NAT method) so that the outgoing requests are always tagged with the same IP address.
- If you have a group of public IP addresses, you can have the NAT system assign addresses to devices on a first-come first-served basis.
- Tunneling can be used for transmitting packets of one type over another network.

## Port Address Translation
- <mark style="background: #BBFABBA6;">PAT:</mark>
	- All systems are translated to the same IP address, but with a different port number assignment.
- When packets come back into the private network, they are routed back to their destination with a table within PAT that tracks the public and private port numbers.
- PAT enables nodes on a LAN to communicate with the Internet without revealing their IP address. All outbound IP communications are translated to the router's external IP address. Replies come back to the router, which then translates them back into the private IP address of the original host for final delivery.

# First Hop Redundancy Protocol
- <mark style="background: #BBFABBA6;">FHRP:</mark>
	- Allows multiple routers to share a virtual IP address and MAC address, ensuring uninterrupted connectivity for hosts in the event of a router failure.
- Important features of FHRP:
	- <mark style="background: #BBFABBA6;">Virtual IP address:</mark>
		- This virtual IP address serves as the default gateway for hosts on the LAN.
		- If the primary router fails, another router in the FHRP group takes over the virtual IP address, ensuring uninterrupted connectivity for hosts without requiring manual reconfiguration.
	- <mark style="background: #BBFABBA6;">Virtual MAC address:</mark>
		- This virtual MAC address is associated with the virtual IP and is used by hosts on the LAN to resolve the layer 2 MAC address of the default gateway.
		- Another failover.
	- <mark style="background: #BBFABBA6;">Redundancy Protocols:</mark> 
		- HSRP, VRRP, GLBP
		- These define how routers in the group communicate, elect a primary router, and handle failover events.
	- <mark style="background: #BBFABBA6;">Router Election:</mark> 
		- Backup routers monitor the primary's status and take over if it becomes undesirable. 

# Sub-Interfaces
- <mark style="background: #BBFABBA6;">Logical interfaces that are configured on a physical interface of a network device, such as a router or a switch.</mark>
- Commonly used when a physical interface needs to be divided into multiple virtual interfaces to support multiple VLANs or multiple IP subnets.
- Each VLAN has its own configuration settings, such as IP address, VLAN membership, and encapsulation type.
- Each sub-interface is associated with a specific VLAN and can be configured to add VLAN tags to incoming and outgoing packets.

# Virtual Local-Area Networks
- <mark style="background: #BBFABBA6;">VLANs:</mark>
	- Significantly increases the network's performance capability.
	- Removes potential performance bottlenecks.
	- Can increase network security.
	- Can enable you to create multiple broadcast domains on a single switch. 
- <mark style="background: #BBFABBA6;">VLAN Trunking Protcol (VTP):</mark>
	- Used to reduce administration in the switched network.
	- You can put all switches in the same VTP domain and reduce the need to configure the same VLAN everywhere.
- <mark style="background: #BBFABBA6;">Tagging:</mark>
	- The port will send out a packet with a header that has a tag number that matches its VLAN tag number.
	- <mark style="background: #BBFABBA6;">On any given port, you can have just one untagged VLAN, and that will be the default port that the traffic will go to unless it is tagged to go elsewhere.</mark>
	- Used to identify packets as belonging to a particular VLAN.
	- <mark style="background: #BBFABBA6;">VLANs are used to segment a network into logical sub-networks, and each VLAN is assigned a unique VLAN tag.</mark>
	- If the VLAN tag is not configured correctly, the computer may not be able to access network resources.
- <mark style="background: #BBFABBA6;">Port binding:</mark>
	- How a port is bound; static, dynamic, or ephemeral.
- <mark style="background: #BBFABBA6;">Port aggregation:</mark>
	- Combining multiple ports on a switch; auto, desirable, or on.
- <mark style="background: #BBFABBA6;">Link Aggregation Protocol (LACP):</mark>
	- A common aggregation protocol that enables multiple physical ports to be bound together. Most devices allow you to bind up to four, but some go up to eight.

## VLAN Membership
- Common methods to determine how VLAN membership is assigned:
	- <mark style="background: #BBFABBA6;">Protocol-based VLANs:</mark>
		- Computers are assigned to VLANs using the protocol in use and the layer 3 address.
		- This method enables a particular IP subnet to have its own VLAN.
		- The IP numbers are only used to determine membership, not to determine routing.
	- <mark style="background: #BBFABBA6;">Port-based VLANs:</mark>
		- Require that specific ports on a network switch be assigned to a VLAN.
	- <mark style="background: #BBFABBA6;">MAC Address-based VLANs:</mark> 
		- Assigns membership according to the workstation's MAC address.
		- Useful because the workstation can move anywhere without needing reconfigured.
- The primary reason for segmentation is to protect sensitive information from other hots or the rest of the network in general. 

## Switch Virtual Interface
- <mark style="background: #BBFABBA6;">SVI:</mark>
	- A virtual interface configured on a layer 2 switch to enable routing between VLANS.
- SVIs are used to route traffic between VLANs.
- <mark style="background: #BBFABBA6;">Each SVI represents a VLAN interface and is assigned an IP address and subnet mask.</mark>
- SVIs are usually configured using the switch's CLI.

## Interface Configuration and Switch Management
- There are other options that you can choose or tweak:
	- Tag vs Untag VLANs: Tagging should be used if you're trunking. The only VLAN that is not tagged in a trunk is the native VLAN.
	- Default VLAN: Mandatory and used for communication between switches.
	- Flow Control: Ethernet temporarily stops transmission of data to ensure zero packet loss when the network is congested.
	- <mark style="background: #BBFABBA6;">Port Mirroring:</mark> Used to monitor network traffic and monitor how well a switch works. It copies the traffic from all ports to a single port and disallows bidirectional traffic on that port. RSPAN and SPAN can be used.
	- Port Security: Allows an admin to configure switch ports so that only certain MAC addresses can use the port. Three main areas:
		- MAC limiting and filtering
		- 802.1x
		- Blocking unused ports.
	- <mark style="background: #BBFABBA6;">Authentication, Accounting, and Authorization (AAA):</mark> Often uses RADIUS, TACACS+, or Kerberos.
	- Usernames/Passwords: It is possible to configure local username/password auth without AAA, but not recommended.
	- Virtual Consoles and Terminals: Often a serial or parallel port, and it is possible for virtual ports to connect to physical ports. Configure a username/password for this.
	- <mark style="background: #BBFABBA6;">Jumbo Frames:</mark> Used to allow for very large ethernet frames. When a lot of data is sent at once, the number of packets is reduced, and the data sent is less processor intensive. Not all network devices and protocols support these.
	- Other: Speed, duplexing, IP addressing, and the default gateway.

## Voice VLAN
- A VLAN configuration typically used in VoIP to ensure efficient and secure transmission of voice traffic.
- Separates voice traffic and data traffic.

# Trunking
- <mark style="background: #BBFABBA6;">The use of multiple network cables or ports in parallel to increase the link speed beyond the limits of any one cable or port.</mark> Link aggregation is essentially the same thing.
- VLAN Trunking: Trunking to the VLAN, now common with routers, firewalls, VMWare hosts, and WAPs.

# Spanning Tree Protocol
- <mark style="background: #BBFABBA6;">STP: Designed to prevent switching loops</mark>
- <mark style="background: #BBFABBA6;">Spanning Tree Algorithm (STA): Enables a switch or bridge to work around hops in a network's topology.</mark>
- If network topology changes or if a switch/bridge port fails, STA creates a new spanning tree, notifies the other bridges, and routes around it.
- If a particular port has a problem, STP can block the port, disable the port, or forward data to another port. 
- STP uses bridge protocol data units (BPDUs) to identify the status of ports and bridges across the network.
- Redundant paths and potential loops can be avoided by:
	- <mark style="background: #BBFABBA6;">Blocking:</mark> A blocked port accepts BPDU messages, but doesn't forward them.
	- <mark style="background: #BBFABBA6;">Disabled:</mark> The port is offline and does not accept BPDU messages.
	- <mark style="background: #BBFABBA6;">Forwarding:</mark> The port is part of the active spanning tree topology and forwards BPDU messages to other switches.
	- Learning: Not part of the active topology, but can take over if another port fails. Receives BPDUs and identifies changes to the topology.
	- <mark style="background: #BBFABBA6;">Listening:</mark> Receives BPDU messages and monitors for changes to the network topology.


[[1 IPv4 Network Addressing|<- Prev Section]] | [[3 Network Services|Next Section ->]]
