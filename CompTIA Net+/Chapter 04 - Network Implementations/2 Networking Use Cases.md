# Software-Defined Networking
- SDN: Used to bypass the physical limitations of standard networking by using cloud architectures.
- Contains its own architecture, top to bottom:
	- [[Application layer]]
	- [[Control Layer]]
	- [[Infrastructure Layer]]
	- [[Management plane]]

# SDNs and the SD-WAN
- SD-WAN: An extension of the SDN that is commonly used in telco and data centers.
- Makes cloud computing available at the WAN level by adopting a virtual WAN architecture.
- Was evolved from MPLS and implements a central controller for managing the implementation.
- Transport agnostic.
- Application aware; can identify, classify, and prioritize network traffic based on the specific apps or services being used. 
	- Deep Packet Inspection
	- Application recognition
	- Dynamic policies and QoS
	- Path selection and routing optimization
	- Traffic steering and load balancing
	- Security and access controls
- Application awareness of SD-WAN allows organizations to optimize application performance, gain granular visibility and control, and improve network efficiency and security.
- Zero-touch provisioning: Automate deployment and configuration of SD-WAN devices with minimal manual intervention.
- Central policy management is crucial in SD-WANs because:
	- They are consistent and uniform.
	- It simplifies configuration.
	- It provides granular control and visibility.
	- It allows for dynamic policy enforcement.
	- Scalability & flexibility
	- Policy orchestration and automation

# Virtual Extensible Local-Area Network
- VXLAN: An extension of a VLAN that utilizes network virtualization to overcome the scalability limitations of traditional VLANs by allowing the creation of logical layer 2 networks over layer 3.
	- First creates an overlay network on top of an existing IP infrastructure.
	- Then, uses a 24-bit VNI to identify and segregate virtual networks.
- VTEPs are responsible for encapsulating and decapsulating VXLAN packets.
- Some key benefits and features:
	- Scalability: up to 16 million VNIs.
	- Flexibility: Interoperable with existing network technology.
	- Isolation
	- Efficiency: Dodges the 4096 VLAN ID limitation.
- DCI is what connects multiple datacenters together in a VXLAN.

# Zero Trust Architecture
- ZTA: Assumes no implicit trust within the network, regardless of whether the connection is internal or external.
- Key principles:
	- Policy-based authentication
	- Authorization
	- Least privilege access
	- Microsegmentation
	- Continuous monitoring and inspection
	- Encryption and data protection
	- Dynamic trust assessment

# Secure Access Secure Edge / Security Service Edge
- SASE: A concept that combines network security features with WAN capabilities to provide secure and scalable access to cloud-based applications and resources.







