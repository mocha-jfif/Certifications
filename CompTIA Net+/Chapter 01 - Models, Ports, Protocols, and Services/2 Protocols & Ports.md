# Connection Oriented Versus Connectionless Protocols
- Connection-oriented:
	- <mark style="background: #BBFABBA6;">Data delivery is guaranteed</mark>; communication continues until transmissions are complete and verified. TCP.
- Connectionless:
	- <mark style="background: #BBFABBA6;">Best effort delivery</mark> with no acknowledgement. UDP.

# <font color="#c3d69b">Internet Protocol</font>
- IP: Defined in RFC 791
	- Used to transport data from one node to another.
	- Connectionless; TCP is required.
	- Performs fragmentation and reassembly tasks for network transmissions because of the [[MTU]], which is limited in IP.
	- Responsible for addressing.

# <font color="#c3d69b">Transmission Control Protocol</font>
- TCP: Defined in RFC 793; 14 fields.
	- Mutually establishes sessions and provides reliability to IP.
	- Adds flow control, sequencing, and error detection / correction.
	- Time-outs help accommodate and handle errors. 

## How TCP Works: The TCP Three-Way Handshake
- SYN -> SYN is sent to target host.
- SYNACK -> Target host opens connection for the request and sends back an acknowledgement.
- ACK -> Origin host sends another acknowledgement to confirm the session is ready.

# <font color="#c3d69b">User Datagram Protocol</font>
- UDP: Defined in RFC 768.
	- Fire and forget protocol.
	- No session is established between hosts.
	- More efficient than TCP, but not as reliable.

# <font color="#c3d69b">Internet Control Message Protocol</font>
- ICMP: Defined in RFC 792.
	- Works with the IP layer to provide error checking and reporting functionality.
	- Commonly used for the ping utility.
	- Provides error messages like "destination unreachable" and "time exceeded"
	- Performs source quench; receiving host cannot handle the influx of data, so ICMP sends source quench messages to tell the sender to slow down transmissions.

# <font color="#c3d69b">Internet Protocol Security</font>
- IPSec: 
	- Designed to provide secure communications between systems.
	- It can encrypt and authenticate network transmissions.
	- Made up of two protocols: Authentication Header (AH) and Encapsulating Security Payload (ESP)
	- Three key services provided:
		- Data verification
		- Protection from data tampering
		- Private transactions
	- Internet Key Exchange (IKE): 
		- Key management protocol used with IPSec to establish secure communication channels and negotiate cryptographic keys for encrypted VPN connections.
		- Establishes security associations between communicating devices.

# <font color="#c3d69b">Generic Routing Encapsulation</font>
- GRE: Cisco-created tunneling protocol.
	- Encapsulation: Data packets are encapsulated within GRE headers, which includes a GRE header and a new IP header.
	- GRE header: Contains fields such as protocol type, a key field, and a sequence number field.
	- New IP header: Specifies source and destination IP address, protocol type, and TTL.
	- Transmission: Transmitted like every over IP packet.
	- Decapsulation: Both headers are removed at the end of the tunnel.
- Often used in scenarios where direct layer 2 connectivity is not possible or practical.
- Protocol independent.

# <font color="#c3d69b">File Transfer Protocol</font>
- FTP: Defined in RFC 959.
	- Provides for the uploading and downloading of files from a remote host running FTP software.
	- Uses TCP to guarantee delivery.
	- Has weak security mechanisms used to authenticate.
	- Assumes all files are ASCII files unless transfer mode is switched.

# <font color="#c3d69b">Secure File Transfer Protocol</font>
- SFTP: 
	- Based on SSH, more secure version of FTP. 
	- Has more robust authentication features and supports encryption.

# <font color="#c3d69b">Secure Shell</font>
- SSH: 
	- Alternative to Telnet.
	- Provides security by encrypting data as it travels between systems.
	- SSH1 and SSH2 are available, but incompatible with one another.

# <font color="#c3d69b">Telnet</font>
- Telnet: Defined in RFC 854
	- Virtual terminal protocol.
	- Primarily used to access managed network devices.

# <font color="#c3d69b">Simple Mail Transfer Protocol</font>
- SMTP: Defined in RFC 821.
	- Defines how mail is sent between hosts.
	- Uses TCP.
	- Destination host must always be available.
	- Can send and receive.

# <font color="#c3d69b">Domain Name System</font>
- DNS: 
	- Resolves hostnames to IP addresses.

# <font color="#c3d69b">Dynamic Host Configuration Protocol</font>
- DHCP: Defined in RFC 2131.
	- Enables IP address scope, or pre-defined groups within address pools, to be defined on the DHCP server.
	- DHCP clients request an address, and the server leases it one. 

# <font color="#c3d69b">Trivial File Transfer Protocol</font>
- TFTP: Defined in RFC 1350
	- Doesn't have the level of security or functionality that FTP has.
	- No directory navigation.
	- Uses UDP.

# <font color="#c3d69b">Hypertext Transfer Protocol</font>
- HTTP: Defined in RFC 2068.
	- Enables media to be downloaded from an HTTP server.
	- Web clients make requests, and the HTTP server returns an HTML file.
	- Uses URL to determine what webpage to serve.

# <font color="#c3d69b">Hypertext Transfer Protocol Secure</font>
- HTTPS: Encrypts data exchange with TLS / SSL.
	- Both client and server must support it.
	- Almost all popular clients and servers do.

# <font color="#c3d69b">Network Time Protocol</font>
- NTP: Defined in RFC 958.
	- Facilitates communication and synchronization of time between systems.
	- Runs on UDP.

# <font color="#c3d69b">Simple Network Management Protocol</font>
- <mark style="background: #BBFABBA6;">SNMP</mark>: Uses port 161 to send, and port 162 to receive.
	- Enables network devices to communicate information about their state to a central system.
	- Enables passing of configuration parameters to devices.
	- Not an NMS itself.
- <mark style="background: #BBFABBA6;">Components of SNMP</mark>
	- A manager is the central communication port for SNMP devices on a network.
	- Each device to be managed has an SNMP agent installed.
	- Communicates and receives information from managed devices.
	- Messages from certain events are called traps.

![[Blank board(2).png]]
- <mark style="background: #BBFABBA6;">SNMP Management Systems</mark>
	- A computer running NMS software.
	- Most NMS applications use graphical maps of the network to locate and query a device.
	- Using SNMP and an NMS, all network devices can be monitored.
- SNMP Agents
	- An agent can be any device that can run a software component to facilitate communication to the manager.
	- Agents can report when a threshold is passed and can send a trap to the NMS.
- <mark style="background: #BBFABBA6;">Management Information Bases (MIBs)</mark>
	- Communication goes both ways.
	- *Get* and *Get Next* read information from the agent.
	- *Walk* automatically moves through *Get Next* commands.
	- MIBs define what parameters are accessible, which are read-only, and which can be set.
	- MIB is controlled by ISO. ISO will assign an applicant an ID.
	- Assignment of numbers structured within the hierarchical tree.
- <mark style="background: #BBFABBA6;">SNMP Communities</mark>
	- Logical grouping of systems.
	- Only communicates between community members.
	- Public: Read only
	- Private: Read/write
- SNMPv2c
	- One iteration of SNMPv2 is v2c. C is "Community"
		- Lacks robust security features and has reliance on a community-based security model.
		- Devices using this must share a community string.
		- Maintains backward compatibility with SNMPv1.
- <mark style="background: #BBFABBA6;">SNMPv3</mark>
	- Current version of SNMP
	- Supports authentication and encryption.

# <font color="#c3d69b">Light Directory Access Protocol</font>
- LDAP: 
	- Provides a mechanism to access and query directory services and systems.
	- Most LDAP interactions are via utilities like net logon or locating a resource through searching.

# <font color="#c3d69b">Server Message Block</font>
- SMB:
	- Provides access to network resources like files, printers, ports, etc., that are running on Windows.
		- Samba allows file and printer access between Windows and Linux.

# <font color="#c3d69b">System Log</font>
- Syslog: 
	- Most Unix/Linux based systems include the capability to write messages to log files via syslog.
		- Done for management or security reasons and allows devices with no access to write a central repository with logger utilities.

# <font color="#c3d69b">Structured Query Language Server</font>
- SQL:
	- The most common DB language.
	- Queries are configured in real time and passed to DB servers.

# <font color="#c3d69b">Remote Desktop Protocol</font>
- RDP: 
	- Provides a way for a client system to connect to a server as if it were a local client application (aka thin client).
		- Only sends mouse movements, key strokes, and bitmap images of the screen on the server to the local client; no actual data.

# <font color="#c3d69b">Session Initiation Protocol</font>
- SIP: 
	- Designed to establish and maintain multimedia sessions.
	- Uses TCP and UDP.
	- Also includes a suite of security services which includes DOS prevention, authentication, integrity protection, and encryption / privacy.

# Understanding Port Functions
- TCP/IP has 65535 ports available, with 0-1023 labelled as well known ports.


# <span style="background:#d3f8b6">Port Table</span>

| **Protocol** | **Port**   | **TCP/UDP** |
| ------------ | ---------- | ----------- |
| FTP          | 20, 21     | TCP         |
| SSH/SFTP     | 22         | TCP         |
| Telnet       | 23         | TCP         |
| SMTP         | 25         | TCP         |
| DNS          | 53         | TCP/UDP     |
| HTTP         | 80         | TCP         |
| SMB          | 445        | TCP         |
| SMTPS        | 587        | TCP         |
| LDAPS        | 636        | TCP         |
| SQL          | 1433       | TCP         |
| RDP          | 3389       | TCP/UDP     |
| SIP          | 5060, 5061 | TCP/UDP     |
| DHCP         | 67, 68     | UDP         |
| TFTP         | 69         | UDP         |
| NTP          | 123        | UDP         |
| SNMP         | 161, 162   | UDP         |
| Syslog       | 514        | UDP         |
|              |            |             |
[[1 The OSI Model |<- Prev Section]] [[3 Traffic Types| Next Section ->]]