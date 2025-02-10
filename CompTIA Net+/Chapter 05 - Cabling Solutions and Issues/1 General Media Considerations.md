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

## RJ-11 connectors
- Used on telephone cables.
- They have capacity for six small pins. In many cases, not all pins are used. Telephones use two, DSL uses four.

![[Pasted image 20250210092914.png]]


