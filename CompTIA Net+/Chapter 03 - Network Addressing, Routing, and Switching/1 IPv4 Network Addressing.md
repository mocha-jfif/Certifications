- <mark style="background: #BBFABBA6;">The IPv4 address space has five addresses (A-E), but only A-C assign addresses to clients.</mark>
	- Class D: Multicast addressing
	- Class E: Reserved for future development and research.
- <mark style="background: #BBFABBA6;">The three classes available for assignments:</mark>
	- Class A: Uses only the first octet to represent the network.
	- Class B: Uses two octets to represent the network.
	- Class C: Uses three octets to represent the network.

| Address Class | Range   | Number of Networks | Number of Hosts | Binary   |
| ------------- | ------- | ------------------ | --------------- | -------- |
| A             | 1-126   | 126                | 16777214        | 0xxxxxxx |
| B             | 128-191 | 16384              | 65534           | 10xxxxxx |
| C             | 192-223 | 2097152            | 254             | 110xxxxx |
| D             | 224-239 | N/A                | N/A             | 1110xxxx |
| E             | 240-255 | N/A                | N/A             | 1111xxxx |
# Subnet Mask Assignment
- Most commonly expressed in 32-bit dotted decimal format.
- <mark style="background: #BBFABBA6;">Defines which parts of the IP address refers to the network address and which refers to the host address.</mark>

| Address Class | Default Subnet Mask |
| ------------- | ------------------- |
| A             | 255.0.0.0           |
| B             | 255.255.0.0         |
| C             | 255.255.255.0       |
# Subnetting
- <mark style="background: #BBFABBA6;">A process by which the host portions off an IP address create more networks than if you used the default subnet mask.</mark>
- You use bits from the node portion of the address to create more network addresses.
- Two reasons for subnetting:
	- More effective use of IP ranges.
	- More secure and manageable; using multiple networks confines traffic to the network it needs to be on which reduces overall traffic levels. Creates more broadcast domains which reduces broadcast traffic.
- <mark style="background: #BBFABBA6;">Variable Length Subnet Masking (VLSM) allows a different subnet mask for the same network number on different subnets.</mark>
- The routing protocol used must be able to advertise the mask for each subnet, so it <mark style="background: #BBFABBA6;">must be classless. </mark>

# IPv4 Public vs Private Networks
- <mark style="background: #BBFABBA6;">A public network can be connected to by anyone. Addressing is more considered.</mark>
- <mark style="background: #BBFABBA6;">A private network has restricted access.</mark>
- An ISP assigns you an IP address; they offer large blocks for more permanent entities.
- RFC 1918 defines private ranges for classes A, B, and C.

| Class | Address Range                 | Default Subnet Mask |     |
| ----- | ----------------------------- | ------------------- | --- |
| A     | 10.0.0.0 - 10.255.255.255     | 255.0.0.0           |     |
| B     | 172.16.0.0 - 172.31.255.255   | 255.255.0.0         |     |
| C     | 192.168.0.0 - 192.168.255.255 | 255.255.255.0       |     |
# Classless Interdomain Routing (CIDR)
- <mark style="background: #BBFABBA6;">An IPv4 method of assigning addresses outside of the standard class standard</mark>.
- <mark style="background: #BBFABBA6;">Addresses are assigned using a value called a slash.</mark>
	- The value of the slash depends on how many bits of the mask are used to express the network portion of the address.

>[!info] For example, a subnet mask that uses all 8 bits form the first octet and 4 from the second would be described as /12. /12 has 2^12 addresses available, which would be 4096 available addresses (4094 when considering restricted addresses.)

# Default Gateways
- <mark style="background: #BBFABBA6;">The means by which a device can access hosts on other networks for which it does not have specifically configured route.</mark>
- If the host is on a remote network, the system looks in the routing table to determine whether it has an entry. If it does, it uses it. If not, it uses the default gateway.
- Any system that does not have a default gateway or any static routes is limited to operating on its own network segment.

# Assigning IP Addresses 
- There are two ways for a device to receive an IP address; statically or dynamically.
- <mark style="background: #BBFABBA6;">Static Addressing:</mark>
	- The manual assignment of IP addresses. Two main problems:
		- Complexity grows as devices are added.
		- If an address scheme changes, all devices need reconfigured.
- <mark style="background: #BBFABBA6;">Dynamic Addressing:</mark>
	- The automatic assignment of IP addresses using DHCP.
		- Scopes are defined on a DHCP server.
		- DHCP reservations ensure a device with a specific MAC address always is assigned the same IP.
		- Can also assign the subnet mask, default gateway, and DNS info.

# BOOT Protocol
- <mark style="background: #BBFABBA6;">BOOTP: Originally created so diskless workstations could obtain network information.</mark>
- System broadcasts for a BOOTP server. If the server exists, it compares the MAC address of the system issuing the BOOTP request with a database of entries. From the database, information is supplied and a file must be downloaded.

# Automatic Private IP Addressing
- APIPA: Introduced in Win 98 and implemented beyond.
- <mark style="background: #BBFABBA6;">A system can give itself an IP address if it cannot receive one from a DHCP server.</mark>
- <mark style="background: #BBFABBA6;">164.254.0.0 IP address range</mark>.
- Does not provide a default gateway. If you can only connect to local devices, APIPA address is likely active (DHCP is down.)
- If a system doesn't support APIPA and cannot get an address from DHCP, it assigns itself an address of 0.0.0.0.

# Identifying MAC Address
- <mark style="background: #BBFABBA6;">6-byte (48-bit) hexadecimal address that enables a NIC to be identified on a network.</mark>
- IEEE assigns them to avoid duplicates. Each manufacturer has an ID, then they can further assign the address. The first 3 bytes are the manufacturer, and the last 3 are assigned by the manufacturer.
- The first 3 bytes are called the organizationally unique identifier (OUI)
- Only A-F and 0-9 are used in hex.
- EUI-48 and EUI-64 exist (Extended Unique Identifier)