# Broadband vs Baseband Transmissions
- Baseband uses digital signaling over a single wire; bidirectional, but sending and receiving cannot be simultaneous.
	- To send multiple signals on a single cable, it uses time-division multiplexing, which divides a single channel into time slots. Most networks use this baseband technology.
- Broadband uses analog, and the medium must be split into two channels or two cables.
	- Multiple channels are created using frequency-division multiplexing, which enables broadband to accommodate traffic going different directions on a single medium simultaneously.

# Simplex, Half-Duplex, and Full-Duplex
- Simplex: Enables one-way communication of data through the network, with the full bandwidth of the cable used for the transmission.
- Half-duplex: Accommodates transmitting and receiving on the network, but not at the same time.
- Full-duplex: Can simultaneously send and receive.

# Data Transmission Rates
- Normally measured by the number of data bits that can traverse the medium in a single second; measured today in Mbps and Gbps.

# Wired v. Wireless
- A wireless network uses radio signals to transmit data between devices.
- Wired networks rely on physical cables.

# Cellular Technology Access
- GSM initially used TDMA to provide multiuser access by chopping up the channel into sequential time slices.
- TDMA was later replaced by DMA which uses different frequencies for each user to provide various means of coverage.
- Original GSM access with both TDMA and CDMA was 2G.
- 3G brought minor enhancements.
- 4G added the capability to implement mobile broadband.
- LTE was based on EDGE and HSMA technologies which increased the capacity and speed by using a different radio interface together with core network improvements.
- 5G brought faster speeds and met the needs of IoT devices.

# Satellite Access
- Used for wireless computer network access through satellite communication systems, which provide Internet connectivity to remote locations or areas where traditional wired infrastructure is unavailable or impractical.
- Operates using a two-way communication process: [[upstream]] and [[downstream]].

# Types of Network Media
- Two basic choices: copper and fiber-optic.

## Twisted-Pair Cabling (Copper)
- Originally created for voice transmissions, but now also used for networking. Two main types today:
	- UTP: More common than STP
	- STP: Used in environments where greater resistance to EMI and attenuation is required.
- Categories of TP cabling:
	- Cat 5: Operates at 100Mbps with a transmission range of 100 meters.
	- Cat 5e: Used on networks that run at 10/100 Mbps and even up to 1000 Mbps; can be used up to 100 meters. Minimum of 100 MHz of bandwidth.
	- Cat 6: Transmits data up to 10 Gbps; minimum of 250 MHz of bandwidth and specifies cable lengths up to 100 meters with 10/100/1000 Mbps transfer, along with 10 Gbps over shorter distances. Typically made up of four twisted pairs of copper wire.
	- Cat 6a: Offers a minimum of 500 MHz of bandwidth, 100 meters with 10 Gbps speeds.
	- Cat 7: Shielding has been added to individual pairs and to the cable as a whole to greatly reduce crosstalk. 600 MHz, backward compatible. Not recognized by EIA / TIA. STP.
	- CAT 8: 40 Gbps at 2000 MHz up to 30 meters.

## Coaxial Cables
- Coax: Copper core, plastic insulation, ground, and outer plastic.
- Made this way to add resistance to attenuation, crosstalk, and EMI.
- Thinnet and thicknet cables exist. Both are uncommon, but thinnet is more likely. Two types of thinnet:
	- RG-59: Used to generate low-power video connections. It cannot be used over long distances because of its high frequency power losses. 
	- RG-06: Often used for cable TV and cable modems.

## Direct Attach Copper
- DAC: Commonly used to connect networking equipment.
- Typically consists of copper conductors enclosed in a protective jacket and are terminated with standard connectors such as SFP or QSFP.
- Twinax has two inner conductors instead of one. Commonly used for short distances (10 meters or less). Great for SANs, server clustering, and HPC environments.

## Fiber-Optic Cables
- Because fiber-based media uses light transmissions instead of electronic pulses, EMI, crosstalk, and attenuation are nonissues.
- Although its more expensive, it is well suited for high-speed data communications. It eliminates the problems associated with copper-based media.
- Composed of a fiber glass core, silica cladding, silicone coating, a buffer jacket, strength members, then a polyurethane jacket.
- Two types available:
	- [[Multimode fiber]]
	- [[Single mode fiber]]
- Common types include:
	- 62.5-micron core / 125-micron cladding multimode
	- 50-micron core / 125-micron cladding multimode
	- 8.3-micron core / 123-micron cladding single mode

## Plenum V. PVC Cables
- Cables that occupy the space above a drop ceiling must be plenum rated. Plenum-rated cables are coated with a nonflammable material.
- Plenum-rated cables must be flame resistant and must not produce toxic fumes if exposed to intense heat.

# Types of Media Connectors

## BNC Connectors
- Associated with coaxial media and 10BASE2 networks.
- Barrel connectors, T-connector, and terminiators.
- Connectors = couplers.

![[Pasted image 20250210092807.png]]

## RJ-11 Connectors
- Used on telephone cables.
- They have capacity for six small pins. In many cases, not all pins are used. Telephones use two, DSL uses four.

![[Pasted image 20250210092914.png]]


## RJ-45 Connectors
- Used with twisted-pair cabling.
- Supports eight wires.

![[Pasted image 20250210093028.png]]

## F-Type Connectors
- Screw-on connections used to attach coax to devices.
- Has a "nut" that provides a gripping point.

![[Pasted image 20250210093113.png]]

## Fiber Connectors
- Any connectors can either be angled physical contact (APC) or ultra-physical contact (UPC)
	- UPC has an end face polished at a zero degree angle.
	- APC has an eight degree angle.
- Multifiber push-on (MPO): Utilizes a push-on coupling system.
	- Compatible with SM and MM.
	- 12-fiber, 24-fiber, and 48-fiber variants.

### ST
- Uses a half twist bayonet type of lock.
![[Pasted image 20250210093149.png]]

### SC
- Uses a push-pull connector.
![[Pasted image 20250210093218.png]]

### LC
- Has a flange on top, similar to an RJ-45.

![[LC-Premium-unibody-connector-e1665758303719.png]]
### MT-RJ
- Small form factor; popular.

![[1280_cmrhTKfKMcK11wBa.jpg]]

### FC
- Has a threaded body.
- Used in environments where vibration is a problem.

![[Pasted image 20250210093448.png]]

## Transceivers
- SFP and GBIC modules are often used to link a gigabit Ethernet port with a fiber network.
- Fiber transceivers are bidirectional and can operate in duplex mode. 
- There is a receiver port (RX) and transmitter port (TX)
- When RX and TX ports are transposed, communication errors and performance degradation typically occur. One device may be configured for full duplex while the other is set to half duplex. In this case, one side of the communication expects to send and receive data simultaneously, but the other side can only send or receive data at a time.
- Communications can fail if the RX/TX ports are dirty or if there's a connector mismatch.

## Media Couplers & Converters
- When you have two dissimilar types of network media, a media converter is used to allow them to connect.
- Commonly implemented converters:
	- Single-mode fiber to Ethernet
	- Single-mode to multimode fiber
	- Multimode fiber to Ethernet
	- Fiber to coax

## Rollover and Loopback Cables
- Rollover cable: Cisco proprietary; used to connect a computer system to a router or switch console port.
- Loopback cable: Used to test and isolate network problems. If made correctly, the loopback plug causes the link light on a device such as a NIC to come on.

## Ethernet Copper and Fiber Standards
- [[10BASE-T]]
- [[100BASE-TX]]
- [[100BASE-FX]]
- [[1000BASE-T]]
- [[40GBASE-T]]

## Multiplexing Options
- Bidirectional wavelength division multiplexing (WDM) is the transmission of optical channels on a fiber propagating simultaneously in both directions.
	- DWDM replaces SONET/SDH regenerators and can amplify signal and enable it to travel a greater distance.
		- Terminal multiplexer
		- Line repeaters
		- Terminal demultiplexer
	- CWDM has relaxed stabilization requirements, so you can have vastly different speeds for download than upload.







