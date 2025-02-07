# Unicast
- <mark style="background: #BBFABBA6;">Traffic is one-to-one</mark>.
- Most common in IP networks.
- Point-to-point, one-to-one address link.

# Multicast
- <mark style="background: #BBFABBA6;">Groups of network devices can send and receive data between the members of the group at one time. (One-to-many)</mark>.
- Grouping is established by configuring each device with the same multicast IP address.
- Commonly used for IPTV, gaming, and video streaming.

# Anycast
- <mark style="background: #BBFABBA6;">Traffic is one-to-nearest.</mark>
- Multiple devices share the same anycast IP address, but packets are routed to the nearest (or best) destination based on routing metrics such as shortest path or lowest latency.
- Commonly used in CDNs, DNS, and load balancers.

# Broadcast
- <mark style="background: #BBFABBA6;">Traffic is one-to-all.</mark>
- Each packet is addressed to a specical broadcast IP address.
- Commonly used in Arp, DHCP, and network discovery.
- Does not propagate across routers.

[[2 Protocols & Ports |<- Prev Section]] [[1 Network Topologies|Next Chapter ->]]