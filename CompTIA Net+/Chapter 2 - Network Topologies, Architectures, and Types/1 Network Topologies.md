- <mark style="background: #BBFABBA6;">Topology: Refers to a network's physical and logical layout</mark>.
	- Physical topology: Refers to the actual layout of the computer cables and other network devices.
	- Logical topology: Refers to the way in which the network appears to the devices that use it.
	- The diagrams are used to identify network components and how they are physically or logically connected.

# Star / Hub & Spoke
- All devices connect to a central device called a hub or switch.
- Each connected device requires a single cable to be connected to the hub or switch, creating a point-to-point connection. 
- <mark style="background: #BBFABBA6;">Advantages</mark>:
	- Easily expanded without disruption to the network.
	- Cable failure affects only a single endpoint.
	- Easy to troubleshoot and implement.
- <mark style="background: #FFB86CA6;">Disadvantages</mark>:
	- This topology requires more cable than others.
	- A central device is a single point of failure.
	- Additional network equipment is required to create the layout.

# Mesh
- Point-to-point connection between every device on a network.
- Each node is a relay, so if one cable fails, data has an alternative route.
- <mark style="background: #BBFABBA6;">Advantages</mark>:
	- Mesh provides redundant paths between LAN topologies.
	- Can be expanded without disruption to current users.
- <mark style="background: #FFB86CA6;">Disadvantages</mark>:
	- Requires more cable than other topologies.
	- Implementation is complicated.

# Hybrid Topology
- Also known as a "partial mesh." Combines multiple topologies.

# Point-to-Point
- Connection between **two** devices.

# Spine & Leaf
- Two-tier model promoted by Cisco for switches.
- The spine is the back bone of the network (trunk) and is responsible for interconnecting the leaf switches.
- Every leaf is connected to every spine.
- Path is randomly chosen so traffic load is evenly balanced between the top-tier switches.
- If one top-tier switch fails, there would only be a mild degradation in performance.
- Always crosses same number of devices.
- Uses SDN to route traffic.

# Three-Tier Hierarchical Model
- End user is effectively isolated from the database by the introduction of a middle-tier server.
- The three layers involved:
	- <mark style="background: #BBFABBA6;">Core Layer</mark>:
		- Backbone; switching and routing meet.
		- Incorporate internal firewall, strong equipment.
		- High throughput speeds.
	- <mark style="background: #BBFABBA6;">Distribution / Aggregation Layer</mark>:
		- Management takes place, DNs polices are managed, filtering, and routing.
		- Lower latency and larger MAC address table required because of the high volume of traffic.
	- <mark style="background: #BBFABBA6;">Access / Edge Layer</mark>:
		- Switches that allow end users and servers to connect to the enterprise are called access (or edge) switches.
		- May or may not be layer 3; minimizing cost-per-port and providing high port density.

>[!info] The core layer is the backbone, where the fastest routers and switches operate to manage separate networks. The distribution / aggregation layer is the boundary layer where ACLs and layer 3 switches operate to properly manage data between VLANs and subnetworks. The access / edge layer is where switches connect to ensure data is delivered to endpoints.

# Collapsed Core
- <mark style="background: #BBFABBA6;">Three-layer becomes two-layer; core and distribution layers are combined</mark>.
- Commonly seen in datacenters and enterprise networks.
- More simplicity, cost saving, more efficient communication, and scalability.
- Limited redundancy, scalability, constraints, and potential bottlenecks.

# Traffic Flows
- Typically occur in two ways: east-west or north-south.
	- <mark style="background: #BBFABBA6;">East-West:</mark> Data is flowing among devices within a specific datacenter.
	- <mark style="background: #BBFABBA6;">North-South:</mark> Data is flowing into the datacenter or out of the datacenter.

# Older Topologies: Bus and Ring
- Bus Topology:
	- Uses a trunk to connect all devices on a network
	- Devices connect using t-connectors (taps)
	- Each end of the physical bus must be terminated to avoid signal reflection.
	- Loose or missing terminators disrupt data transmissions.
- Ring Topology:
	- Logical, not physical, ring.
	- In a true ring, if a single computer or cable fails, the signal is interrupted.