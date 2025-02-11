# Components of Wiring Distribution
- The wiring closet is the place in the network where you connect the cables and networking devices. 
- These rooms contain key network devices, and they also contain the network media.

## Network Cross-Connects
- The cable that runs throughout a network can be divided into two distinct sections:
	- [[Horizontal cabling]]
	- [[Vertical (backbone) cabling]]
- There are three types of cable distribution:
	- [[Vertical (Main) cross-connect]]
	- [[Horizontal cross-connect]]
	- [[Intermediate cross-connect]]
- The term "cross-connect" refers to the point where the cables running throughout the network meet and are connected.

## 66 and 110 Blocks (T568A, T568B)
- Type 66 is an older punchdown block used to connect wiring for telephone systems and other low-speed network systems.
	- Has 50 rows of IDC contacts to accommodate 25-pair TP cable.
	- Not suitable for anything above 10BASET due to crosstalk.
- Type 110 is used to connect network cable to patch panels.
	- Can also be used at the other end of the network cable at the RJ-45 wall jack.
	- Supports higher frequencies and less crosstalk.
	- Termination will be a T568A or T568B, depending on the wiring standard used.
- Krone and Bix blocks also exist.
	- These two require different blades in the punchdown tools to work with them.
	- Bix is more popular in older implementations
	- Krone is more popular internationally.

## MDF and IDF Wiring Closets
- Two types of wiring closets are the main distribution frame (MDF) and intermediate distribution frame (IDF).
- The main wiring closet typically holds the majority of the network gear and where outside lines run into the network (MDF)
	- One key component is the primary patch panel.
	- The network connector jacks attached to this patch panel lead out to the building for network connections.
- Some networks use multiple wiring closets. A secondary closet (IDF) connects to the MDF using a backbone cable.

## Rack Size
- Standard rack sizes, such as 19-inch or 23-inch widths, are commonly used in the industry and provide compatability with a wide range of networking equipment from vari