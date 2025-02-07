- Provides functionality enabling the network to operate.

# Dynamic Host Configuration Protocol
- <mark style="background: #BBFABBA6;">DHCP:</mark>
	- Enables scopes within address pools to be defined on a system running a DHCP server application.
- The server assigns an address from the scope to the client for a predetermined amount of time (lease / lease time)
- <mark style="background: #BBFABBA6;">DHCP is a protocol dependent service and is not platform dependent. The basic functionality is the same across the board.</mark>
- <mark style="background: #BBFABBA6;">IPv6 via DHCP6 uses Stateless Address Auto Configuration (SLACC).</mark>
	- Devices send a request for the prefix, then the device uses it and its MAC to create an IP address.

## DHCP and DNS Suffixes
- <mark style="background: #BBFABBA6;">Suffixes define the DNS servers to be used and the order in which to use them.</mark>
- DHCP settings can push a domain suffix search list to DNS clients; only used for name resolution.

## DHCP Relays and IP Helpers
- Relay: An agent on the router that acts as a go-between for clients and the server.
- IP Helper: Will forward broadcasts for DHCP/BOOTP, TFTP, DNS, TACACS/TACACS+, the time service, and the NetBIOS name/datagram service; can do more than a DHCP relay.

# Domain Name Service
- <mark style="background: #BBFABBA6;">DNS: Resolves hostnames to IP addresses.</mark>
- Before the internet, the network that would become the internet used a text file called HOSTS which had manual entries. HOSTS can still be used today.
- Systems that ask DNS servers for a name-to-IP address mapping are called resolvers.
- <mark style="background: #BBFABBA6;">Dynamic DNS (DDNS) updates DNS entries as changes are made.</mark>
- <mark style="background: #BBFABBA6;">DNS Caching: Storing results of previous resolutions; comes with a TTL to avoid stale information.</mark>

## DNS Namespace
- Logical divisions hierarchically organized.
- Top: .com, .edu, .uk/.de/.us , etc.
- Subdomains: rds.microsoft.com (rds is the subdomain)
- The domain name, along with any subdomains, is called the FQDN.
- DNS can perform IP-to-hostname resolution also. This is called reverse lookup and uses PTR records.
- <mark style="background: #BBFABBA6;">Iterative query: Client continuously queries the server.</mark>
- <mark style="background: #BBFABBA6;">Recursive query: DNS doesn't have an answer and forwards it to another server.</mark>

## Types of DNS Entries
- A records, MX records, CNAME
- CNAME: alias records for a system.

## <font color="#c3d69b">DNS Records</font>
- Address (A): Maps a domain to an IPv4 address.
- IPv6 Address (AAAA): Maps a domain to an IPv6 address.
- Canonical Name (CNAME): Stores additional hostnames, or aliases, for hosts in the domain.
- Mail Exchange (MX): Specifies the mail servers responsible for receiving email messages for a domain.
- TXT: Used for adding human readable information such as SPF, DKIM, and domain ownership verification records.
- PTR: A pointer to the canonical name, which is used for reverse lookups.
- Start of Authority (SOA): Contains data on DNS zones and other DNS records. A zone is the part of the domain for which an individual DNS server is responsible.
- Name Server (NS): Identifies the name servers in the domain.
- Service Locator (SRV): Used for newer protocols instead of creating protocol-specific records such as MX.
- The most common type of DNS zone is the forward lookup zone, which allows DNS clients to obtain information such as IP addresses that correspond to DNS domain names. 

# Time Protocols:
- Time synchronization is important to keep track of changes.
- <mark style="background: #BBFABBA6;">NTP uses a hierarchical, semi-layered system of time sources, where each level of the hierarchy is called a stratum.</mark>
	- Each stratum is assigned a number starting with zero for the reference clock at the top and incrementing from there with the number representing the distance from the reference clock. 
- <mark style="background: #BBFABBA6;">Precision Time Protocol (PTP): Can achieve sub-microsecond accuracy for applications where precision in time is criticial.</mark>
	- It operates by exchanging timing messages between one clock that has been selected to coordinate the timekeeping across all other clocks within the network.
- <mark style="background: #BBFABBA6;">Network Time Security (NTS): Uses digital signatures and encryption to protect time synchronization from security threats.</mark>

[[2 Routing & Switching Technologies|<- Prev Section]] | [[1 Common Networking Devices|Next Chapter ->]]