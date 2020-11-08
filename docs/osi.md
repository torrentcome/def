# Osi
## OSI model = Open Systems Interconnection model 

The Open Systems Interconnection model (OSI model) is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology. Its goal is the interoperability of diverse communication systems with standard communication protocols.

### Schema

| Layer | Name | Description |
| ----- | ------ | ------ |
| 7 | Application | The top layer (apart from layer 8, the user) is responsible for a wide area. Some examples are resource sharing, remote file access, remote printer access and e-mail amongst other. Protocols using layer 7 includes FTP, DNS, and HTTP. |
| 6 | Presentation | This layer is responsible for character code translation such as ASCII, Unicode, and EBCDIC. TLS and SSL protocols operate at this level. |
| 5 | Session | Layer 5 is responsible for session establishment, termination and maintenance of sessions. Here we find the NetBIOS protocol and L2TP tunneling protocol. |
| 4 | Transport | This layer is responsible for traffic control, session-multiplexing and segmenting messages. Two commonly used protocols are TCP and UDP. |
| 3 | Network | The network layer is responsible for routing network packages. The layer provides traffic control, local addressing, and fragmentation. The most used protocol is IP, ICMP, and IGMP |
| 2 | Data Link |  This layer is responsible for link establishment, acknowledgment, error-checking to name a few. Protocols operating here are the 802.3 (Ethernet), ARP and LLDP (Link Layer Discovery Protocol).|
| 1 | Physical | This layer is responsible for transmission and reception of the physical medium. Protocols like DSL and USB use layer 1. |
