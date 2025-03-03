1. Which of the following definitions best describes the function of a firewall?
	1. A device that connects two networks forwarding traffic between them as needed
	2. ==A device located between two networks that enables administrators to restrict incoming and outgoing traffic==
	3. A device that caches Internet data for subsequent use by internal network clients
	4. A device that enables Internet network clients with private IP addresses to access the Internet

2. Review the following figure. Each of the switches has three ports connected to computers and one port for switch-to-switch connections. All of the computer ports and links are configured for half-duplex communication. The switch-to-switch links are configured for full-duplex communication. Which of the following statements about the switched network is true?![[Pasted image 20250220115650.png]]
	1. There is one collision domain for this network.
	2. There are three collision domains, one for each switch-to-switch connection.
	3. ==There are nine collision domains, one for each half-duplex connection.==
	4. There are twelve collision domains, one for each switch connection.

3. Which of the following network devices can provide authentication services for multiple remote access servers using the device's own account database?
	1. NAS
	2. IDS
	3. NGFW
	4. ==RADIUS==

4. You are designing the network for your company's new branch office, and you need a device on which administrators can create virtual local area networks (VLANs) and that will forward traffic between them. Which of the following devices can do this?
	1. Virtual router
	2. ==Multilayer switch==
	3. Broadband router
	4. Load balancer

5. You are setting up a new network for which you have been given the IPv4 network address 10.61.0.0/19. You want to calculate the number of hosts you can create on each subnet. How many bits are allocated to the host identifier in an IPv4 address on this network?
	1. 5
	2. 8
	3. ==13==
	4. 21

6. The protocols that are responsible for the delivery of data packets to their final destinations on an internetwork operate at which layer of the Open Systems Interconnection (OSI) reference model?
	1. Application
	2. Session
	3. ==Transport==
	4. Network
	5. Data link

7. Originally, storage area networks (SANs) were dedicated solely to storage-based traffic. A local area network (LAN) was also required for other types of traffic. Today, however, it is possible for SAN and LAN traffic to coexist on a single network medium. Which of the following SAN protocols are capable of sharing a network medium with standard LAN traffic? (Choose all that apply.)
	1. Fibre Channel
	2. InfiniBand
	3. ==iSCSI==
	4. ==FCoE==

8. Which of the following Application layer protocols do not include a program that enables a user to log on to a remote network device and execute commands using a character-based interface? (Choose all that apply.)
	1. Telnet
	2. ==Simple Mail Transfer Protocol (SMTP)==
	3. File Transfer Protocol (FTP)
	4. ==Domain Name System (DNS)==

9. Which of the following statements about switches are true? (Choose all that apply.)
	1. ==Switches provide internal crossover circuits and use uplink ports to form a hierarchical star/hub and spoke topology.==
	2. ==Switches are Data link layer devices that connect network devices in a star/hub and spoke topology.==
	3. Switches amplify and repeat signals received through one port out all other ports regardless of the destination.
	4. Switches use IP addresses to identify the devices connected to specific ports.

10. You are planning an automated operating system deployment for 100 new Windows workstations your company has received. You intend to configure the workstations to boot using Preboot Execution Environment (PXE), during which time the system will obtain an IP address from a Dynamic Host Configuration Protocol (DHCP) server and then download a boot image file from a Trivial File Transfer Protocol (TFTP) server. Which of the following well-known ports must you open on the firewall separating the workstations from the servers? (Choose all that apply.)
	1. 64
	2. 65
	3. 66
	4. ==67==
	5. ==68==
	6. ==69==

11. Your department is experiencing frequent delays as users wait for images to render using their outdated graphics software package. As a result, you submitted a change request for a new software product at the monthly meeting of the company's change management team. Now that the change request has been approved, it is time to implement the change. Which of the following administrative tasks will most likely be the change management team's responsibility during the implementation process? (Choose all that apply.)
	1. Notifying users
	2. Documenting all modifications made
	3. ==Authorizing downtime==
	4. ==Designating a maintenance window==

12. You are installing a new server that is equipped with two power supplies. The server's firmware enables you to set the mode in which the power supplies will be used. In which of the following modes must the dual power supplies be running in order for the system to be fault tolerant?
	1. Individual mode
	2. Combined mode
	3. ==Redundant mode==
	4. Hot backup mode

13. The Domain Name System (DNS) defines a hierarchical name space, in which locations are reflected in fully qualified domain names (FQDNs). Which of the words in the FQDN [`www.paris.mydomain.org`](http://www.paris.mydomain.org/) represents the bottommost layer in the DNS namespace's domain hierarchy?
	1. `www`
	2. ==`paris`==
	3. `mydomain`
	4. `org`

14. The term _datagram_ is typically used by protocols offering connectionless delivery service. Which of the following protocols use the term _datagram_ to describe the data transfer unit it creates? (Choose all that apply.)
	1. TCP
	2. IP
	3. ==UDP==
	4. Ethernet

15. Which element of the CIA triad prevents unauthorized viewing of protected data?
	1. ==Confidentiality==
	2. Integrity
	3. Availability
	4. None of the above

16. You have just received notification of a new software release for an application you are running on your servers. The release is intended to address a newly discovered security vulnerability. Which of the following is the correct term for a software release containing a fix designed to address one specific issue?
	1. An upgrade
	2. ==A patch==
	3. A service pack
	4. An update

17. Twisted-pair cables consist of multiple pairs of wires within a sheath, with each pair of wires twisted together separately. Which of the following statements best explain the reason for the twists in twisted-pair cabling? (Choose all that apply.)
	1. ==The twists help to prevent crosstalk in adjacent wire pairs.==
	2. The twists make it easier for installers to attach connectors to the cable ends.
	3. The twists extend the cable's bend radius allowance, making it easier to install.
	4. ==The twists limit the effects of electromagnetic interference (EMI) on the signals carried over the cable.==
	5. The twists help to prevent data collisions from occurring.

18. The figure shown here lists the processes currently running on a Linux workstation. Which of the following performance monitoring tools, provided in Linux and Unix operating systems, enables you to display information about processes that are currently running on a system?![[Pasted image 20250220120818.png]]
	1. `netstat`
	2. `dig`
	3. `perfmon`
	4. ==`top`==

19. You are contracting with a provider to obtain email services for the clients on your network, using their existing email servers in the public cloud. You do not need anything from the provider other than email. Which of the following service models will you be using?
	1. PaaS
	2. ==SaaS==
	3. IaaS
	4. All of the above

20. Security information and event management (SIEM) is a combination tool that uses information gathered from logs and network devices to provide a real-time analysis of the network's security condition. Which of the following SIEM processes performs searches for specific criteria, during specific time frames, in logs located on different computers?
	1. Data aggregation
	2. Correlation
	3. Retention
	4. ==Forensic analysis==

21. When you start a Dynamic Host Configuration Protocol (DHCP) client, it transmits DHCPDISCOVER messages to locate and initiate contact with DHCP servers. Which of the following types of transmissions does the client use for this purpose?
	1. ==Broadcast==
	2. Unicast
	3. Multicast
	4. Anycast

22. Which of the following technologies enables virtual private network (VPN) users to establish a connection using only a web browser?
	1. VPN concentrator
	2. DMVPN
	3. SIP trunk
	4. ==MPLS==
	5. Clientless VPN

23. You are installing a wireless network in a site that has many 2.4 GHz wireless telephones. Which of the following wireless networking technologies can you use that will never experience interference from the telephones? (Choose all that apply.)
	1. IEEE 802.11b
	2. IEEE 802.11g
	3. ==IEEE 802.11ac==
	4. ==IEEE 802.11a==
	5. IEEE 802.11n

24. Which of the following is another term for a switch?
	1. Multicast hub
	2. Multiport repeater
	3. ==Multiport bridge==
	4. Multihomed router

25. You are working at a client site with a managed router that includes a console port for administrative access, which you can use to connect a laptop and run a terminal program to access the device's interface. Which of the following is the best term for this type of access to the device?
	1. Client-to-site
	2. In-band
	3. BYOD
	4. ==Out-of-band==

26. Which of the following describes the primary difference between single sign-on (SSO) and same sign-on?
	1. Single sign-on (SSO) credentials consist of one username and one password, whereas same sign-on credentials consist of one username and multiple passwords.
	2. ==Single sign-on (SSO) requires the user to supply credentials only once, whereas with same sign-on, the user must supply the credentials repeatedly.==
	3. Single sign-on (SSO) requires multifactor authentication, such as a password and a smartcard, whereas same sign-on requires only a password for authentication.
	4. Single sign-on (SSO) enables users to access different resources with one set of credentials, whereas same sign-on requires users to have multiple credential sets.

27. You have a laptop that requires you to hold your finger on a scanner pad before you can use it. A device equipped with a fingerprint scanner that is part of a multifactor authentication mechanism is using which of the following types of technology?
	1. Tamper detection
	2. ==Biometrics==
	3. Hand geometry
	4. Pattern recognition

28. You have been asked to locate the computers on a network that the previous consultant has configured with incorrect IPv6 addresses. Which of the following are not correctly formatted IPv6 addresses? (Choose all that apply.)
	1. e00::c955:c944:acdd:3fcb
	2. ==fe00::b491:cf79:p493:23ff==
	3. ==2001:0:44ef68:23eb:99fe:72bec6:ea5f==
	4. 2001:0:49e6:39ff:8cf5:6812:ef56

29. During a physical security evaluation by an outside contractor, you are asked whether your company uses a fail open or fail closed policy for the datacenter. You do not know what the contractor means. Which of the following physical security mechanisms can either fail close or fail open?
	1. ==Door locks==
	2. Motion detectors
	3. Honeypots
	4. Video cameras

30. A disgruntled senior associate in the IT department at your company was terminated today and had to be escorted from the building. The IT director has instructed you to disable all of the former employee's accounts, change all network device passwords to which the employee had access, and have the datacenter door locks rekeyed. Which of the following terms best describes the director's concern in asking you to do these things?
	1. Logic bombs
	2. ==Internal threats==
	3. Rogue devices
	4. Social engineering
	5. External threats

31. Ralph is troubleshooting a Windows server, and while doing so he runs the following command: `ping 127.0.0.1`. The command completes successfully. What has Ralph proven by doing this?
	1. That the computer's network adapter is functioning properly
	2. That the computer's IP address is correct for the network
	3. ==That the computer's TCP/IP networking stack is loaded and functioning properly==
	4. Nothing at all

32. Which of the following are not examples of multifactor authentication (MFA)? (Choose all that apply.)
	1. A system that requires a smartcard and a PIN for authentication
	2. ==A system that uses an external RADIUS server for authentication==
	3. ==A system that requires two passwords for authentication==
	4. A system that requires a password and a retinal scan for authentication

33. A user calls Ed at the help desk to report that he cannot access the Internet. He can access systems on the local network, however. Ed examines the routing table on the user's workstation and sees the following. Which of the following statements explains why the user cannot access the Internet?![[Pasted image 20250220123150.png]]
	1. The routing table does not specify a loopback address.
	2. The routing table does not specify a DNS server address.
	3. ==The routing table does not specify a default gateway address.==
	4. The routing table contains two different routes to the 224.0.0.0 network.

34. Which of the following statements about single-mode fiber-optic cable are true? (Choose all that apply.)
	1. ==Multimode cables use an LED light source, while single-mode cables use a laser.==
	2. Multimode cables can span longer distances than single-mode cables.
	3. Multimode cables have a smaller core filament than single-mode cables.
	4. ==Multimode cables have a smaller bend radius than single-mode, making them easier to install.==
	5. Multimode fiber-optic cables require a ground, whereas single-mode cables do not.

35. A user swipes a smartcard through the reader connected to a laptop and then types a password to log on to the system. Which of the following actions is the user performing?
	1. Auditing
	2. Accounting
	3. Authorization
	4. ==Authentication==

36. Which of the following cabling topologies have never been used by standard Ethernet networks? (Choose all that apply.)
	1. Bus
	2. ==Ring==
	3. Star/hub and spoke
	4. Mesh

37. Pulling into your company parking lot at lunchtime, you notice a person without a company parking sticker on his car working at a laptop. You have seen this more than once, and you begin to suspect that unauthorized users are connecting to the company's wireless access point and gaining access to the network. Which of the following are steps you can take to prevent this from happening in the future? (Choose all that apply.)
	1. Use RADIUS for authentication.
	2. Place the access point in a screened subnet.
	3. ==Disable SSID broadcasting.==
	4. ==Implement MAC address filtering.==

38. Which of the following is a fault tolerance mechanism for the default gateway on a specific TCP/IP LAN?
	1. Open Shortest Path First (OSPF)
	2. ==First Hop Redundancy Protocol (FHRP)==
	3. Spanning Tree Protocol (STP)
	4. Network address translation (NAT)

39. Multiprotocol switches are devices that perform functions associated with two different layers of the Open Systems Interconnection (OSI) reference model. Which of the following layers are often associated with network switching? (Choose all that apply.)
	1. Application
	2. Presentation
	3. Session
	4. Transport
	5. ==Network==
	6. ==Data link==
	7. Physical

40. You are attempting to connect your new laptop to your company's wireless network. The wireless access point on the network has an SSID that is not broadcasted and uses WPA3 for security. Which of the following describes what you must do to connect your laptop to the network?
	1. Select the SSID from a list and allow the client to automatically detect the security protocol.
	2. ==Type the SSID manually and then select WPA3 from the security protocol options provided.==
	3. Type the SSID manually and allow the client to automatically detect the security protocol.
	4. Select the SSID from a list and then select WPA3 from the security protocol options provided.

41. Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA) is a media access control mechanism designed to prevent two systems using the same network medium from transmitting at the same time. Which of the following IEEE standards calls for the use of CSMA/CA?
	1. 802.3
	2. ==802.1X==
	3. 802.11ac
	4. All of the above

42. A large enterprise network will—at a minimum—have demarcation points for telephone services and a connection to an Internet service provider's network. In many cases, these services will enter the building in the same equipment room that houses the backbone switch. Which of the following is the term used to describe this wiring nexus?
	1. MTBF
	2. IDF
	3. RDP
	4. ==MDF==

43. You have configured your company's wireless network to enable a client to authenticate only when the signal strength of their connection exceeds a specified level. Which of the following terms best describes the security mechanism provided by this configuration?
	1. ==Geofencing==
	2. Local authentication
	3. Motion detection
	4. Port security

44. Social engineering has become an increasingly serious problem on your company network. Which of the following is an effective method for preventing sensitive data from being compromised through social engineering?
	1. Install a firewall between the internal network and the Internet.
	2. Install an antivirus software product on all user workstations.
	3. ==Implement a program of user education and corporate policies.==
	4. Use IPsec to encrypt all network traffic.

45. You have been given a Class B network IP address with which to configure the new network you are designing. Which of the following is the default subnet mask you should use for an IPv4 Class B network?
	1. 255.255.255.255
    1. 255.255.255.0
    2. ==255.255.0.0==
    3. 255.0.0.0

46. Alice's company has just started working with sensitive government data. To enhance the security of the datacenter, she has implemented some additional security measures. All the servers now have crimped metal tags holding the cases closed. All the hardware racks are locked in clear-fronted cabinets. All the cable runs are installed in transparent conduits. These are all examples of which of the following physical security measures?
	1. Geofencing
	2. ==Tamper detection==
	3. Port security
	4. Asset tracking

47. You have just installed a web server for your company that is configured to host a public Internet site using the registered domain name [adatum.com](http://www.adatum.com/). The server's hostname in the Domain Name System (DNS) is `www`. The web server also has an administrative site, which you want to be able to access remotely. You have configured the administrative site to be encrypted and to use the port number 12354. Which of the following URLs must you use to access the administrative website from the Internet?
	1. ==[`www.adatum.com:12354`](http://www.adatum.com:12354/)==
	2. [`www.adatum.com`](http://www.adatum.com/)
	3. [`www.adatum.com:80`](http://www.adatum.com/)
	4. [`www.adatum.com:12354`](http://www.adatum.com:12354/)

48. To prevent outside users from accessing your wireless network, you configure the access point not to broadcast the network's SSID. However, you later discover that outsiders are still accessing the network. For which of the following reasons is disabling SSID broadcasts a relatively weak method of device hardening?
	4. Every access point's SSID is printed on a label on the back of the device.
	5. Attackers have software that can easily guess a network's SSID.
	6. ==Attackers can capture packets transmitted over the network and read the SSID from them.==
	7. Attackers have ways of connecting to the network without the SSID.

49. You are installing a web server farm in your corporate headquarters that will be used to host websites for the corporation's subsidiaries, which are located all around the world. In which of the following cloud models does a single organization function as both the provider and the consumer of all cloud services?
	1. ==Private cloud==
	2. Public cloud
	3. Ad hoc cloud
	4. Hybrid cloud

50. Your supervisor has recently begun using the terms _on-boarding_ and _off-boarding_, with which you are unfamiliar. With which of the following types of policies are these terms typically associated?
	1. Incident response
	2. ==Identity management==
	3. Inventory management
	4. Data loss prevention

51. Virtual private networks (VPNs) use a data transmission technique called tunneling, which encapsulates a data packet within another packet for transmission over a network connection, typically using the Internet. The system also encrypts the entire encapsulated data packet for protection. Split tunneling is a variation of this method that provides which of the following advantages? (Choose all that apply.)
	1. Additional data integrity protection
	2. ==Access to local network devices while connected to the VPN==
	3. Faster data transmission through multiplexing
	4. ==Conservation of VPN bandwidth==

52. Your supervisor wants you to disable all of the ports on the network's switches that are not in use. You tell her that this is not necessary; she wants to know why you think so. Which of the following are valid reasons not to disable unused switch ports? (Choose all that apply.)
	1. The unused ports are not patched into wall jacks.
	2. ==The datacenter is already secured from unauthorized access.==
	3. ==The switch is configured to use a MAC-based access control list.==
	4. Leaving some ports enabled facilitates the on-boarding of new users.

53. Which of the following are security mechanisms that fall into the category of deception technologies?
	1. ==Honeypots and honeynets==
	2. Root guards
	3. Screened subnets
	4. Geofencing

54. Which of the following network devices can employ access control lists (ACLs) to restrict access? (Choose all that apply.)
	1. ==Routers==
	2. ==Servers==
	3. ==Switches==
	4. Hubs
	5. ==Wireless access points==

55. Which of the following terms is not associated with Data link layer communications?
	1. ==Administrative distance==
	2. Spanning Tree Protocol
	3. Maximum transmission unit
	4. Jumbo frames

56. Which of the following statements about DHCP snooping are true? (Choose all that apply.)
	1. ==DHCP snooping is implemented in network switches.==
	2. DHCP snooping prevents DNS cache poisoning.
	3. ==DHCP snooping detects rogue DHCP servers.==
	4. ==DHCP snooping drops DHCP messages arriving over the incorrect port.==

57. A user reports that she cannot connect to a server on her network. You want to identify the scope of the problem, so you try to reproduce the problem on the user's computer. The problem persists. No other users are reporting the same problem. What is the next logical step that you should perform to identify the affected area?
	1. Examine the server's configuration for the correct settings.
	2. Verify that the local router is forwarding traffic.
	3. Confirm that the switch the client is connected to is functioning.
	4. ==Perform the same task on another computer connected to the same segment.==

58. On a wireless network, which of the following best describes an example of a captive portal?
	1. A web page stating that the data on a user's computer has been locked and will only be unlocked after payment of a fee
	2. A dedicated switch port used to connect to other switches
	3. ==A web page with which a user must interact before being granted access to a wireless network==
	4. A series of two doors with an intervening airlock through which people must pass before they can enter a secured space

59. In the standard troubleshooting methodology, you begin by taking steps to identify the problem. After you have done this, which of the following steps should you perform next?
	1. Verify full system functionality.
	2. ==Establish a theory of probable cause.==
	3. Establish a plan of action.
	4. Implement the solution.

60. The secured version of the Hypertext Transfer Protocol (HTTPS) uses a different well-known port from the unsecured version (HTTP). Which of the following ports are used by HTTP and HTTPS by default? (Choose all that apply.)
	1. 25
	2. ==80==
	3. 110
	4. ==443==

61. Which of the following are criteria typically used by load balancers to direct incoming traffic to one server out of a group of servers? (Choose all that apply.)
	1. ==Fastest response time==
	2. Fastest processor
	3. ==Lightest load==
	4. ==The next in an even rotation==

62. You are responsible for a network that has a Domain Name System (DNS) server, a proxy server, and an Internet router. A user is reporting that she cannot connect to hosts on her own local area network (LAN) or other internal LANs, and she also cannot access hosts on the Internet. No one else has reported a problem. What is the most likely location of the issue preventing the user's access to the network
	1. The router
	2. The DNS server
	3. The proxy server
	4. ==The user's computer configuration==

63. Virtual LAN (VLAN) hopping is a type of attack directed at network switches. Which of the following best describes how VLAN hopping is a potential threat?
	1. ==VLAN hopping enables an attacker to access different VLANs using 802.1q spoofing.==
	2. VLAN hopping enables an attacker to scramble a switch's patch panel connections.
	3. VLAN hopping enables an attacker to change the native VLAN on a switch.
	4. VLAN hopping enables an attacker to rename the default VLAN on a switch.

64. You are a first-tier support technician working the IT help desk at your company. In your first hour of duty, you receive four trouble calls. Your job is to prioritize the calls based on their severity. Which of the following should be the problem that receives the lowest priority?
	1. ==A fatal error that causes a single computer to fail==
	2. A problem with a mission-critical backbone router that affects an entire network
	3. A problem with an application server that affects a single LAN
	4. A problem with an order entry or customer service call center resource that affects an entire department, with multiple local area networks (LANs)

65. You are attempting to access a Domain Name System (DNS) server located on the other side of a router, but your attempt fails with an error stating that the destination port UDP 53 is unreachable. Your first step in troubleshooting the problem is to try using the `nslookup` utility to access that specific DNS server. This attempt also fails. Next, you use the `ping` utility with the DNS server's IP address. The ping test is successful, indicating that the server is up and running. Which of the following are possible causes of the problem? (Choose all that apply.)
	1. The TCP/IP host settings on your computer are improperly configured.
	2. The router connecting the networks is not running DNS and will not forward this type of datagram.
	3. ==There is a firewall blocking the DNS server's UDP port 53.==
	4. ==The DNS process on the remote server is not running.==
	5. The TCP/IP host settings on the DNS server are improperly configured.

66. Which of the following types of switch performs a cyclical redundancy check (CRC) on an entire frame's contents prior to forwarding it out a port leading to the destination system?
	1. Packet filtering
	2. Cut-through
	3. Source route
	4. ==Store-and-forward==

67. Which of the following attack types does not specifically target wireless network clients?
	1. ==Logic bomb==
	2. Deauthentication
	3. Evil twin
	4. Rogue AP

68. You are having trouble installing a wireless LAN using IEEE 802.11n equipment in a new office complex. The wireless devices have trouble connecting to the access point, and when they do, they achieve only low speeds. When you use a Wi-Fi analyzer to scan the 2.4 GHz frequency band, you see literally dozens of other networks in the area, spread across all of the available channels. Which of the following tasks should you perform to enable your wireless devices to connect to the network reliably and at their best possible speeds?
	1. Configure the access point to suppress SSID broadcasts.
	2. ==Configure all of the wireless network devices to use the 5 GHz band.==
	3. Upgrade all of the network devices to the latest firmware.
	4. Configure all of the network devices to use WPA3 encryption with AES.


69. Which Windows command-line utility produced the output shown here? ![[Pasted image 20250220141858.png]]
	1. ==`arp`==
	2. `ping`
	3. `tracert`
	4. `netstat`

70. Your boss is working in the crawlspace under the floor of the datacenter, and he asks you to hand him the pliers. You hand him the tool shown in the following figure, and he throws it back at you. What is the real function of the tool shown in the figure? ![[Pasted image 20250220141947.png]]
	1. When you connect the tool to pins in a punchdown block, you can access telephone circuits in order to test them or place telephone calls.
	2. When you attach the tool to one end of a wire, it generates a tone that can be detected at the other end.
	3. ==To attach a bulk cable end to an RJ-45 connector, you use the tool to squeeze the connector closed, forcing the wire ends to contact the connector's pins.==
	4. When you attach the tool to a copper cable, you can detect and measure the electrical current flowing through it.

71. You are starting work for a contractor who performs telecommunications cable installations. One of the tools in the kit you have been given is unfamiliar to you. What is the name of the tool shown in the following figure? ![[Pasted image 20250220142114.png]]
	1. Crimper
	2. ==Punchdown tool==
	3. Butt set
	4. Toner and probe

72. You are seeking to upgrade your company's IEEE 802.11g access point to one that provides faster transmission speeds for your newer workstations. Which of the following wireless networking standards is capable of supporting speeds faster than the 54 Mbps of 802.11g but is still backward compatible with your existing IEEE 802.11g workstations?
	1. IEEE 802.11
	2. Bluetooth
	3. IEEE 802.11ac
	4. IEEE 802.11a
	5. ==IEEE 802.11n==

73. You are working on your company's screened subnet (also known as a perimeter network), which has five Linux web servers, a Cisco router, a CSU/DSU providing a leased line connection, and a Windows-based firewall on it. While trying to troubleshoot a network communications failure, you type the following command on one of the systems: `traceroute` [`adatum.com`](http://www.adatum.com/). Which of the following systems might you be working on? (Choose all that apply.)
	1. ==The Cisco router==
	2. ==One of the Linux web servers==
	3. The CSU/DSU console
	4. The Windows-based firewall

74. Which of the following are network topologies used by IEEE 802.11 wireless local area networks (WLANs)? (Choose all that apply.)
	1. Bus
	2. Spine and leaf
	3. Ad hoc
	4. ==Star/hub and spoke==
	5. ==Infrastructure==

75. Which version of the Simple Network Management Protocol (SNMP) uses as its security mechanism two separate unencrypted community strings?
	1. SNMPv1
	2. SNMPv2
	3. ==SNMPv2c==
	4. SNMPv3

76. You are working the help desk at a local computer store, and you receive a call from a customer trying to set up a home network using computers running Windows 11 and wired Ethernet equipment. The customer reports that she cannot access the other two computers in the house from her workstation, nor can she access the Internet. You ask her to run the `ipconfig /all` command and read the results to you. She says that her IP address is 192.168.0.2, her subnet mask is 255.255.255.0, and her default gateway is 192.168.0.1. Which of the following is the most likely cause of the customer's problem?
	1. The customer's network address cannot include a zero.
	2. The customer has an incorrect subnet mask.
	3. ==The customer's network cable is damaged or unplugged.==
	4. The customer has an incorrect default gateway address.

77. Some networks are designed with a switching fabric that contains redundant paths for fault tolerance purposes. However, in this type of design it is possible for packets to circulate endlessly around the network, which is called a switching loop. Which of the following protocols prevents network switching loops from occurring by shutting down redundant links until they are needed?
	1. NAT
	2. RIP
	3. VLAN
	4. ==STP==

78. You are responsible for an internetwork that consists of four internal local area networks (LANs) with 50 users each. Each internal LAN uses twisted-pair Gigabit Ethernet links that connect the users to a switch. Each of the four switches is connected to a separate router. All four routers connect to the same backbone network, which has a single additional router to connect the company's network to the Internet using a T-1 wide area network (WAN) link. Today, users on one of the four internal LANs are reporting that when they came in this morning, they could not access the Internet or resources on the other three internal LANs. However, they could access resources on their own LAN with no problems. Which network component is the likeliest source of the problem in this scenario?
	1. The switch on the problem LAN
	2. The Internet router
	3. The router connecting the problem LAN to the backbone
	4. The cable on the backbone network

79. You are negotiating an agreement with a provider for your company's email service. You have been told to require a 99.99 percent guaranteed rate of service reliability, but the provider is only willing to guarantee 99 percent. Eventually, you and the provider agree on a compromise of 99.9 percent. Which of the following documents will include the negotiated language on this particular point?
	1. AUP
	2. SLA
	3. BYOD
	4. NDA

80. Which of the following networking devices can split a single network into multiple collision domains while maintaining a single broadcast domain? (Choose all that apply.)
	1. Switch
	2. Bridge
	3. Router
	4. Firewall

81. You have just finished installing a web server farm on your company's network, along with a router to create a screened subnet (perimeter network) on which the web servers are located. However, you now cannot access the web servers from your workstation on the internal network. Which of the following is not one of the tasks you will have to complete before you can access the screened subnet from the internal network?
	1. Change MAC addresses.
	2. Change IP addresses.
	3. Update the DNS records.
	4. Change default gateway addresses.

82. You are testing a twisted-pair cable run using a toner and probe. When you apply the toner to a particular pin at one end of the cable, you detect a tone on two pins at the other end. Which of the following faults have you discovered?
	1. Split pair
	2. Open
	3. Short
	4. Crosstalk

83. Your network has been experiencing intermittent service slowdowns and outages ever since the company moved into their new building. You have tried every troubleshooting modality you can think of, but you have not been able to determine the cause. One particular user, perhaps hoping to be the squeaky wheel that gets the grease, has taken to calling you every time he experiences a problem. One day, as you are working in the datacenter, you notice that the user calls every time you hear an additional humming noise. After examining the doors in the hallway, you realize that the racks containing the network switches are located right next to the elevator machinery room. Which of the following conditions is probably causing this intermittent network communication problem?
	1. Bottleneck
	2. EMI
	3. Latency
	4. Crosstalk

84. Ralph is installing a pair of redundant servers and must choose whether to run them in an active-active or active-passive configuration. Running the servers in an active-active configuration provides which of the following advantages that the same servers in an active-passive configuration do not? (Choose all that apply.)
	1. Fault tolerance
	2. Load balancing
	3. Data encapsulation
	4. Increased performance

85. You are starting work at a new company, and on your first day you ask about wireless access for your laptop. You are given an SSID and a WPA3 passphrase. Later, in the lunchroom, when you try to connect your laptop to the network, you cannot see the SSID you were given in the list of available networks, although you can see other networks. What should you do first to try to resolve the problem?
	1. Move closer to the wireless access point.
	2. Move away from the microwave in the lunchroom.
	3. Type in the WPA3 passphrase.
	4. Type the SSID in manually.

86. You are responsible for a wireless LAN that consists of an 802.11n 2x2 access point and laptop computers with a variety of network adapters. Some of the laptops support 802.11n, and a few older models have 802.11g adapters. The wireless LAN is located in a large office building with many other wireless networks, and you are having trouble finding a channel on the 2.4 GHz band that is not congested with traffic. Scanning the 5 GHz band, you find relatively little traffic, so you reconfigure the access point to use a 5 GHz channel. The result is that some of the laptops are able to connect to the network, whereas others are not. What is the most likely reason for the connection failures, and what must you do to enable all the laptops to connect to the wireless network?
	1. The 802.11g standard does not support communication using the 5 GHz band. You must replace the network adapters in those laptops with newer models for them to connect successfully.
	2. The 5 GHz band does not support automatic channel selection. You must configure each laptop to use the same channel as the access point for all the laptops to connect successfully.
	3. The 5 GHz band does not support MIMO communications, so the 802.11n laptops are unable to connect to the network. You must replace the access point with an 802.11g unit for all the laptops to connect successfully.
	4. The 802.11g standard does not support communication using the 5 GHz band. You must configure the access point to support 2.4 GHz for all the laptops to connect successfully.

87. In the Domain Name System (DNS), a zone is a contiguous area of the DNS namespace for which authority is delegated to one or more DNS servers. Which of the following DNS resource record types specifies the IP addresses of the authoritative DNS servers for a particular zone?
	1. PTR
	2. SRV
	3. MX
	4. NS

88. You are experiencing poor performance on your home 802.11n wireless network. You live in a large apartment complex, and when you run a Wi-Fi analyzer, you see many other nearby networks using the often-recommended channels 1, 6, and 11 on the 2.4 GHz frequency. Using the 5 GHz frequency is not an option for your equipment. What should you do to improve the network's performance?
	1. Configure your equipment to use channel 10.
	2. Configure your equipment to use channel 9.
	3. Configure your equipment to use channel 5.
	4. Configure your equipment to use channel 2.

89. Your company's office building is having a fire inspection, and you are the only person on duty in the datacenter. The inspector from the fire department is reviewing the company's asset inventory and asks you where they can find documentation about all chemicals and equipment used in the company's datacenter. You lead the inspector to the director's office, but you are not sure what the documents he needs are called. Which of the following document types contains this information?
	1. MSDS
	2. ESD
	3. NDA
	4. BYOD

90. Which of the following Power over Ethernet (PoE) specifications supplies power to devices using the spare wire pair on a 100Base-TX twisted-pair network?
	1. Alternative A
	2. 4PPoE
	3. Alternative B
	4. All of the above

91. Which of the following statements about the differences between storage area networks (SANs) and network attached storage (NAS) are not true? (Choose all that apply.)
	1. NAS devices typically provide a filesystem, whereas SAN devices do not.
	2. NAS devices typically contain integrated iSCSI targets.
	3. NAS provides file-level storage access, whereas SAN provides block-level storage access.
	4. SAN devices have an operating system, whereas NAS devices do not.

92. You are deploying an 802.11n wireless network for a client who is asking for the best possible security you can provide without deploying additional servers. When setting up the wireless access point, you disable SSID broadcasts, select Wi-Fi Protected Access Preshared Keys (WPA-PSK), and configure MAC address filtering. Which of the following statements about the security of this arrangement is true?
	1. You should not disable SSID broadcasts, because this prevents users from connecting to the network.
	2. The configuration is as secure as you can make it with the specified equipment.
	3. You should use Wi-Fi Protected Access 3 (WPA3) instead of WPA, since it is more resistant to certain types of attacks.
	4. You should not use MAC address filtering, because it exposes MAC addresses to possible attacks.

93. Which of the following connector types are used with fiber-optic cables? (Choose all that apply.)
	1. DB-9
	2. SC
	3. BNC
	4. ST
	5. MPO
	6. RJ-11

94. Which of the following are available as Internet of Things (IoT) devices?
	1. Refrigerators
	2. Doorbells
	3. Thermostats
	4. Speakers
	5. All of the above

95. You are designing an Ethernet network for your company's newest branch office. Your current task is to decide which Ethernet specification to use for the network, a decision that you know will determine what type of cabling you need to purchase and the topology with which the cable will be installed. Which layers of the Open Systems Interconnection (OSI) reference model apply to the cabling and topology elements of a network?
	1. The Application and Transport layers
	2. The Transport and Network layers
	3. The Network and Data link layers
	4. The Data link and Physical layers

96. You are troubleshooting a workstation that cannot access the network. The workstation is plugged into a wall plate that should provide it with access to a DHCP-equipped network using the 192.168.4.0/24 network address. No one else on that network is reporting a problem. You check that the patch cable is properly plugged into the workstation and the wall plate, which it is, and then run `ipconfig /all` on the workstation and examine the output. Which of the following could be the explanation for the workstation's problem, based on the following `ipconfig` results? ![[Pasted image 20250220145507.png]]
	1. The DNS server addresses are incorrect.
	2. The Default Gateway address is missing.
	3. The Subnet Mask value is incorrect.
	4. The DHCP scope is exhausted.

97. A user calls you at the IT help desk and reports that she is having intermittent problems accessing both local servers and Internet websites. Which of the following potential problems can you rule out immediately?
	1. Malfunctioning DNS server
	2. Duplicate MAC addresses
	3. Duplicate IP addresses
	4. Malfunctioning router

98. You have recently discovered a rogue DHCP server on your network. After disabling the rogue server, you now need to terminate all of the rogue IP address leases currently held by DHCP clients on the network and then have them request new leases from the authorized DHCP server. Which of the following commands must you run on each client to do this? (Choose all that apply.)
	1. `ipconfig /dump`
	2. `ipconfig /lease`
	3. `ipconfig /release`
	4. `ipconfig /renew`
	5. `ipconfig /discard`

99. Ralph is reading an article about datacenter design, and he is puzzled by references to east-west and north-south traffic. Which of the following statements best describes the difference between east-west and north-south traffic in a datacenter?
	1. East-west is switch-to-switch traffic, while north-south is switch-to-router traffic.
	2. East-west describes traffic between devices at the same layer of the Open Systems Interconnection (OSI) reference model, while north-south describes traffic between OSI model layers.
	3. East-west traffic stays within the datacenter, while north-south traffic does not.
	4. East-west is backbone traffic among switches and routers, while north-south is traffic to end systems, such as servers.

100. Which of the following Windows command-line utilities produced the output shown here? ![[Pasted image 20250220150859.png]]
	1. `arp`
	2. `ping`
	3. `tracert`
	4. `netstat`
	5. `hostname`
