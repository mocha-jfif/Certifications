# The Seven-Layer Model

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

## Physical Layer
- <mark style="background: #BBFABBA6;">Identifies hardware and network topology</mark>.
- USB, Ethernet, Bluetooth, DSL, ISDN, etc., run here.
- <mark style="background: #BBFABBA6;">Defines voltage, frequency, speed/distance, and bandwidth</mark>.

## Data Link Layer
- <mark style="background: #BBFABBA6;">Responsible for data transfer to the physical layer, error detection / correction, and hardware addressing.</mark>
- A [[frame]] describes the logical grouping of data at this layer.
- Two sublayers:
	- Media Access Control (MAC) layer: Address is burned into the NIC; controls access to network media. 
		- Defined in IEEE 802.2.
	- Logical Link Control (LLC) layer: Error and flow control mechanisms.
- Protocols: HDLC, L2TP, PPP, PPTP, STP, VLANs.

## Network Layer
- <mark style="background: #BBFABBA6;">Responsible for routing.</mark>
- Provides mechanisms to pass data and route selection. 
	- Routing protocols are software components.
	- Contains IP headers.
	- Utilizes [[packets]].
- Routes can be configured manually by adding them to the routing table (static) or by using RIP and DSPF (dynamic).
- [[2 Protocols & Ports#Internet Protocol|IP]], ARP, RARP, ATM, IS-IS, [[2 Protocols & Ports#Internet Protocol Security|IPSec]], [[2 Protocols & Ports#Internet Control Message Protocol|ICMP]], MPLS

## Transport Layer
- <mark style="background: #BBFABBA6;">Responsible for mechanisms to transport data</mark> in three ways:
	- Error checking
	- Service addressing
	- Segmentation
- <mark style="background: #BBFABBA6;">Also responsible for data flow control</mark> using two common methods:
	- Buffering
	- Windowing

## Session Layer
- <mark style="background: #BBFABBA6;">Responsible for managing and controlling the synchronization of data between applications on two devices; establishes, maintains, and breaks sessions</mark>.
- Performs the same essential functions as the transport layer, but on behalf of the applications.
- NetBIOS, NFS, [[2 Protocols & Ports#Server Message Block|SMB]].

## Presentation Layer
- <mark style="background: #BBFABBA6;">Responsible for converting data to appropriate formats</mark>.
- <mark style="background: #BBFABBA6;">Also responsible for encryption</mark>; TLS runs here.

## Application Layer
- <mark style="background: #BBFABBA6;">Responsible for taking requests / data and passing it to other layers</mark>.
- Information is displayed here.
- Not the applications themselves, but the protocols that allow network capabilities.
- [[2 Protocols & Ports#Secure Shell|SSH]], BGP, [[2 Protocols & Ports#Dynamic Host Configuration Protocol|DHCP]], [[2 Protocols & Ports#Domain Name System|DNS]], NTP, RTP, [[2 Protocols & Ports#Session Initiation Protocol|SIP]], [[2 Protocols & Ports#Simple Mail Transfer Protocol|SMTP]], SNB, FTP, HTTP/S, IMAP, POP3


# OSI Versus TCP/IP

![[Blank board(1).png]]

# Data En/Decapsulation and OSI
- As data <mark style="background: #BBFABBA6;">moves down</mark> the model, it is <mark style="background: #BBFABBA6;">encapsulated</mark> with a header and trailer.
- Once received and <mark style="background: #BBFABBA6;">moving back up</mark> the model, these are <mark style="background: #BBFABBA6;">stripped off</mark>. 


[[2 Protocols & Ports |Next Section ->]]