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
- NAT is required to communic