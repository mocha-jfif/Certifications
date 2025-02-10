# Service Models
- NIST defines three primary service models: SaaS, PaaS, and IaaS.

## Software as a Service
- SaaS involves delivering a licensed application to customers over the web to use a service on demand.
- Some examples are:
	- Netflix
	- Adobe
	- Dropbox
	- Slack
	- Mailchimp

# Platform as a Service
- PaaS involves delivering a platform to develop applications over the Internet, without downloads or installation.
- Some examples are:
	- Azure
	- Oracle Cloud Platform
	- OpenShift

# Infrastructure as a Service
- IaaS involves delivering the computer infrastructure in a hosted service model over the Internet.
- Some examples are:
	- AWS
	- RackSpace

# Deployment Models

## Private Cloud
- A cloud infrastructure is provisioned for exclusive use by a single organization comprising multiple consumers.

## Public Cloud
- A cloud infrastructure is provisioned for open use by the general public.
- Owned by the cloud provider and uses a pay-as-you-go model.

## Hybrid Cloud
- A cloud infrastructure that is a composition of two or more distinct infrastructures that remain unique entities, but are bound together by standardized or proprietary technology that enables data and application portability.

# Multitenancy
- Puts data from various clients on the same machines.
- Workloads form different clients can be on the same system so a flaw in implementation can compromise security.

# Elasticity
- Capabilities can be elastically provisioned and released to scale rapidly outward and inward to commensurate with demand.

# Scalability
- Elasticity is required and automatic autoscaling of resources is critical.
- Relates to resources relating to capacity.

# Network Functions Virtualization (NFV)
- Involves the virtualization of network functions and services that traditionally relied on dedicated, proprietary hardware appliances.
- Not an alternative to cloud computing, but an extension that adds virtualization technology.

# Cloud Connectivity Options
- Most cloud providers offer a number of methods that clients can employ to connect with them.
- One of the most common methods is an IPSec hardware VPN.
- Another is a dedicated direct connection (private-direct). You can combine the dedicated network connection(s) with the hardware VPN to create a combination of IPSec-encrypted private connections at a reduced network cost.
- Private cloud to public cloud.

# Virtual Private Cloud (VPC)
- Allows users to create isolated and logically segmented private networks within a public cloud environment via an endpoint that allows the VPC to be connected with other services without the need for additional technologies.
- Key features:
	- Network isolation
	- Customizable network configuration
	- Security controls
	- Endpoint usage
	- Scalability
	- Connectivity options

# Cloud Gateways
- Acts as a bridge between the internal network infrastructure and the cloud.
- Two popular approaches are to utilize Internet gateways to intelligently route network traffic between different locations.
- NAT is required to communicate over the Internet with private IP addresses. Although internet routers are almost always required for routing, by default they won't route private IP addresses to public IP addresses.
- An Internet gateway facilitates communication between resources within a VPC and the broader Internet.
	- Acts as the entry and exit point for traffic flowing in and out of the VAC.
- A NAT is used to manage outbound Internet connectivity for resources within a private subnet of a VAC.
	- Allows private resources that do not have public IP addresses to initiate outbound connections to the Internet while keeping them protected and hidden behind the NAT gateway's public IP address.

# Network Security, Groups, and Lists
- Software and services not necessary for the implementation should be removed, or at least disabled.
- Patches/firmware updates should be kept current and log files carefully monitored.
- Encrypt data
- Backup data frequently
- Implement access control
- Network Security Groups (NSGs) serve as a virtual firewall by:
	- Rule-based filtering
	- Inbound/outbound control
	- Port-level filtering
	- Source and destination IP address filtering
	- Priority and rule evaluation
	- Logging and monitoring
	- Integration with subnets and resources
	- Dynamic updates 
- Network security lists preceded NSGs.