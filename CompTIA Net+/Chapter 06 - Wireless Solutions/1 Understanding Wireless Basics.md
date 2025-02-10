# Wireless Channels and Frequencies
- [[Channel]]
- [[Channel width]]
- 802.11a: 5.15 - 5.875 GHz
- 802.11b and 802.11g: 2.4 - 2.497 GHz
- 802.11n: 2.4 or 5 GHz
- 802.11ac: 5 GHz
- 802.11ax: 2.4 or 5 GHz. Extended uses the 6 GHz frequency.
- [[Band steering]]
- 802.11b/g uses 11 channels, 3 of which are nonoverlapping.

![[Pasted image 20250210103600.png]]

# Speed, Distance, and Bandwidth
- Data rate refers to the theoretical maximum of a wireless standard.
- Throughput refers to the actual speeds achieved after all implementation and interference factors.

# Channel Bonding
- Two channels can be used at once which increases performance.
- 802.11n can go from 40 MHz to 80-160 MHz. It uses the orthogonal frequency-division multiplexing (OFDM) transmission strategy.
- 802.11n has four spatial streams, and 802.11ac goes to eight.
- 802.11ax replaces OFDM with OFDMA, a multiuser version of OFDM that uses a digital modulation scheme. The multiple access is achieved by assigning subnets of subcarriers to individual users.

# MIMO / MU-MIMO  / Directional / Omnidirectional

- MIMO and MU-MIMO are advanced antenna technologies that are key to wireless standards such as 802.11n, 802.11ac, 802.11ax, and LTE.

## Antenna Ratings
- To determine an antenna's strength, refer to its gain value.
- An antenna's gain value represents the difference between the 0dBi isotropic and the antenna's power.
- A higher gain means stronger send and receive signals.
- Every 3 dB of gain doubles an antenna's effective power output.

## Antenna Coverage
- In a typical configuration, an antenna can either be omnidirectional or directional.
- Omnidirectional: Designed to provide a 360-degree dispersed wave pattern. Used when coverage in all directions is required. Wide.
- Directional: Designed to focus the signal in a particular direction. Narrow.

# Network Types
- Ad Hoc: When devices connect directly to each other without the need for a central AP.
- Infrastructure network: Most common wireless network. AP acts as a bridge between wireless clients and the wired network, facilitating communication between devices and providing internet access.

# Establishing Communications Between Wireless Devices
- If you use an infrastructure wireless network design, the network has two key parts: the station (STA) and the AP.
- When a single AP is connected to the wired network and to a set of wireless stations, it is called a basic service set (BSS)
- An extended service set (ESS) describes the use of multiple BSSs that form a single subnetwork.
- Ad hoc mode is sometimes called an independent basic service set (IBSS)
- Communication between the AP and client is a two step process:
	- [[Association]]
	- [[Authentication]]
- ESSID is not unique to a single AP. Multiple APs within the same network share the same ESSID. BSSID identifies individual access points, where ESSID identifies the entire wireless network or WLAN.

# Configuring the Wireless Connection
- Most of the broadband routers similar to a simple small network router differ in the following:
	- Wireless bands
	- Switch speed
	- Security supported
	- Antenna
- The following can be confirmed on an AP:
	- SSID
	- Channel
	- SSID broadcast
	- Authentication
	- Wireless mode
	- DTIM period in seconds
	- Max connection rate
	- Network type

# Autonomous and Lightweight Access Points
- The main difference between autonomous and lightweight APs is their management architecture. Auto APs operate independently and are managed individually, while lightweight APs require a centralized wireless LAN controller for management and coordination. The choice between the two types of APs depend