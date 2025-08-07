# RFC 791: Internet Protocol - DARPA Internet Program Protocol Specification

## High-Level Summary

**Document:** RFC 791  
**Author:** Jon Postel, Information Sciences Institute, University of Southern California  
**Publication Date:** September 1981  
**Status:** Standard (STD 5)  
**Replaces:** RFC 760  
**Type:** Internet Standard  

## Historical Context

RFC 791 defined version 4 of the Internet Protocol (IPv4), which became the foundation of the modern internet. Published in 1981 as part of the DARPA Internet Program, this specification provided the addressing and routing mechanisms that enabled diverse networks to interconnect into what would become the global internet.

This RFC was part of a coordinated release with RFC 793 (TCP), establishing the TCP/IP protocol suite that replaced earlier networking protocols and became the universal standard for internet communication.

## Key Technical Specifications

### Protocol Purpose
The Internet Protocol provides a packet delivery service between hosts across interconnected networks. It defines how data packets (called datagrams) are addressed, routed, and delivered across network boundaries.

### IPv4 Header Format
The specification defines a 20-byte header containing:

- **Version (4 bits)**: Protocol version number (4 for IPv4)
- **Header Length (4 bits)**: Length of header in 32-bit words
- **Type of Service (8 bits)**: Quality of service parameters
- **Total Length (16 bits)**: Total datagram length in bytes
- **Identification (16 bits)**: Unique identifier for fragmented packets
- **Flags (3 bits)**: Control fragmentation behavior
- **Fragment Offset (13 bits)**: Position of fragment in original packet
- **Time to Live (8 bits)**: Maximum hops before packet is discarded
- **Protocol (8 bits)**: Identifies next level protocol (TCP, UDP, etc.)
- **Header Checksum (16 bits)**: Error detection for header
- **Source Address (32 bits)**: Originating host address
- **Destination Address (32 bits)**: Target host address
- **Options (variable)**: Additional protocol options

### Addressing Scheme
IPv4 uses 32-bit addresses organized into classes:

- **Class A**: 1-126.x.x.x (large networks, 16 million hosts)
- **Class B**: 128-191.x.x.x (medium networks, 65,000 hosts)  
- **Class C**: 192-223.x.x.x (small networks, 254 hosts)
- **Special ranges**: Reserved for multicast, experimental use

### Key Functions

#### Fragmentation and Reassembly
The protocol handles packets larger than network maximum transmission units (MTU) by:
- Fragmenting large packets at intermediate routers
- Reassembling fragments at destination hosts
- Using identification and offset fields for proper reconstruction

#### Routing
IP provides connectionless routing where:
- Each packet is routed independently
- No end-to-end connection state is maintained
- Routing decisions made at each network hop

#### Error Handling
Limited error detection and reporting:
- Header checksums detect transmission errors
- Time-to-live prevents infinite routing loops
- ICMP protocol provides error reporting

## Impact on Internet Development

### Fundamental Architecture
RFC 791 established core internet principles:
- **Packet switching**: Data broken into independent packets
- **Connectionless service**: No circuit setup required
- **Best effort delivery**: No guaranteed delivery or ordering
- **End-to-end principle**: Intelligence at network edges, not center

### Scalability Design
The specification enabled internet growth through:
- Hierarchical addressing supporting large-scale routing
- Modular design allowing protocol evolution
- Separation of concerns between network and transport layers

### Interoperability Foundation
Created universal standard allowing:
- Different network technologies to interconnect
- Diverse computer systems to communicate
- Independent network development and operation

## Historical Significance

### Internet Protocol Suite
RFC 791 was part of the foundational TCP/IP specification that:
- Replaced earlier ARPANET protocols
- Enabled transition from research network to public internet
- Provided technical foundation for internet commercialization

### Standardization Impact
- Established DARPA/DoD as leader in internet standards
- Demonstrated value of open protocol specifications
- Created model for collaborative internet development

### Long-term Influence
- IPv4 addresses have numbered over 4 billion devices
- Protocol remains in use 40+ years after publication
- Design principles influenced all subsequent network protocols

## Technical Evolution

### Limitations Addressed Later
- Address space exhaustion led to IPv6 development
- Security concerns addressed by IPSec
- Quality of service enhanced in later specifications

### Extensions and Enhancements
- Classless Inter-Domain Routing (CIDR)
- Network Address Translation (NAT)
- Virtual Private Networks (VPNs)
- Mobile IP for device mobility

## Modern Relevance

### Current Usage
IPv4 remains the predominant internet protocol despite IPv6 availability:
- Billions of devices use IPv4 addresses
- Core internet infrastructure built on IPv4
- Gradual transition to IPv6 ongoing

### Design Lessons
Key principles that remain relevant:
- Simplicity enables scalability
- Layered architecture supports evolution
- Open standards foster innovation
- End-to-end connectivity creates value

## Legacy and Recognition

### Jon Postel's Contribution
As editor of RFC 791 and many other foundational RFCs, Jon Postel earned recognition as a key architect of the internet. His careful specification work enabled global interoperability.

### Protocol Longevity
Few technical specifications have had such lasting impact:
- 40+ years of continuous use
- Foundation for trillion-dollar internet economy
- Enables communication for billions of users

## Archival Information

**Primary Source**: RFC Editor (rfc-editor.org)  
**IETF Datatracker**: datatracker.ietf.org/doc/rfc791/  
**Standard Number**: STD 5  
**Related RFCs**: 
- RFC 793 (TCP)
- RFC 792 (ICMP)
- RFC 950 (Subnetting)

## Significance Statement

RFC 791 represents one of the most successful technical specifications in history. Its design for the Internet Protocol created the addressing and routing foundation that enabled the internet to scale from a research network to a global communication platform serving billions of users.

---

*"The internet protocol is specifically limited in scope to provide the functions necessary to deliver a package of bits (an internet datagram) from a source to a destination over an interconnected system of networks."* - RFC 791