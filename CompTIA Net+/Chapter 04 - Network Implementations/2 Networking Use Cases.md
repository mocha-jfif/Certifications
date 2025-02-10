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
- SASE extends security and networking capabilities to the SSE, providing secure access and low latency connectivity to cloud-based applications and services.
- SASE deploys Global Secure Access Points (GSAPs) at strategic locations worldwide, providing secure connectivity and access to cloud-based resources.

# Infrastructure as Code
- IaC: Involves managing and provisioning computing infrastructure using machine-readable configuration files or scripts, rather than manual processes or physical hardware configuration.
- Key aspects:
	- Declarative configuration
	- Version control
	- Automated provisioning
	- Scalability and consistency
	- Immutable infrastructure
	- Integration with continuous integration/continuous deployment.
- Utilizes [[playbooks]].
- [[Reusable tasks]]
- Version control systems support branching, which allows users to create separate branches or copies of the code base to work on independent features, fixes, or experiments without affecting the main codebase. 

# IPv6 Addressing

## Mitigating Address Exhaustion
- IPv4 is quickly running out of unique addresses.
- IPv6 uses a 128-bit addressing scheme, enabling a massive amount of possible addresses.

## Identifying IPv6 Addresses
- An IPv6 address is divided along 15 bit boundaries, and each 16-bit block is converted into a four digit hexadecimal number and separated by colons.
- 0s can be compressed, but 0s cannot be eliminated when they are not the first in the number sequence.
- The formula is to subtract the number of blocks from 8 and then multiply that number by 16. For example, 2001:4000::3 uses three blocks, so it would be (8-3) * 16 = 8





