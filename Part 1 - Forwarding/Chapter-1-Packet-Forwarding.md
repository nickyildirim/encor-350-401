
### Network Device Comm.
- Network
	- Primary function is to provide connectivty between devices.
	- Almost everything runs on TCP/IP which based on OSI.
	- Flow of data: 
		- Starts with app and goes down to 1.
		- The data gets modified/changed as needed.
		- At Layer 3: the device/host decideds whether the data needs to be in different app in the same host or to a different host.
	- Additional notes:
		- First L2 devices were bridges and switches. L3 devices were strickly routers.
		- As tech evolved, multi layer switches were invented (MLS). They can forward L2/L3 traffic.
	- OSI Model:


| Layers | Name         | Functionatily                            |
| ------ | ------------ | ---------------------------------------- |
| 7      | Application  | Interface for receiving and sending data |
| 6      | Presentation | Formatting of data and encryption        |
| 5      | Session      | Tracking of packets                      |
| 4      | Transport    | End-to-end comm                          |
| 3      | Network      | Logical addressing and routing           |
| 2      | Data Link    | Harware addressing                       |
| 1      | Phisical     | Media type and connector                 |

### Layer 2 Forwarding
- AKA: Data link layer, handles addressing under IP protocol.
- Network packets have L2 addressing with unique source and destination addresses for segments.
- Ethernet commonly uses *media access control* (MAC) addresses.
	- Other data link layer protocols such as Frame Relay use an entirely different method of Layer 2 addressing.
- Note: MAC address is a 48-bit address that is split across six octets and notated in hexadecimal.
	- The first three octets are assigned to a device maker - known as - unique identifier (OUI)
	- The manufacturer is responsible for last three octat is unique. 
- A device listens for network traffic that has its MAC before moving L3
- Network broadcast with MAC address FF:FF:FF:FF:FF:FF will always processed by all devices.

### Collision Domains
- First protocols were 10Base-2 and 10Base-5 (Thick and Thin) where all the devices were connected on a single cable with T connectors.
- When devices talk at the same time, CSMA/CD used to solve it.
- This also means devices only can operate with half-dublex.
- On the other hand, switch maintains MAC table to forward traffic instead of forwarding to each port.

### Virtual LANs
- Provide logical segmentation by creating multiple broadcast domains on tghe same network switch.
- Devices with different VLANs can't communicate via L2 or broadcast traffic.