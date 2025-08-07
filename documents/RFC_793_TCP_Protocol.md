# RFC 793: Transmission Control Protocol - DARPA Internet Program Protocol Specification

## High-Level Summary

**Document:** RFC 793  
**Author:** Jon Postel, Information Sciences Institute, University of Southern California  
**Publication Date:** September 1981  
**Status:** Standard (STD 7)  
**Type:** Internet Standard  
**Companion to:** RFC 791 (Internet Protocol)  

**📄 Original Document:** [RFC 793 - Transmission Control Protocol - IETF Datatracker](https://datatracker.ietf.org/doc/rfc793/)  

## Historical Context

RFC 793 defined the Transmission Control Protocol (TCP), the reliable transport layer protocol that, together with the Internet Protocol (IP) defined in RFC 791, forms the TCP/IP protocol suite that became the foundation of the modern internet. Published simultaneously with RFC 791 in September 1981, these specifications replaced earlier ARPANET protocols and provided the technical foundation for internet growth.

TCP was designed to provide reliable, ordered, and error-checked delivery of data between applications running on hosts communicating over an IP network. While IP handles addressing and routing of packets between networks, TCP ensures that data arrives correctly and completely at its destination.

## Key Technical Specifications

### Protocol Purpose
TCP provides a connection-oriented, reliable, byte-stream service between applications. It guarantees:
- **Reliable delivery**: All data sent is received correctly
- **Ordered delivery**: Data arrives in the same sequence it was sent
- **Error detection**: Corrupted data is detected and corrected
- **Flow control**: Prevents overwhelming the receiver
- **Congestion control**: Adapts to network capacity

### TCP Header Format
The specification defines a 20-byte minimum header containing:

- **Source Port (16 bits)**: Sending application identifier
- **Destination Port (16 bits)**: Receiving application identifier
- **Sequence Number (32 bits)**: Position of data in byte stream
- **Acknowledgment Number (32 bits)**: Next expected sequence number
- **Data Offset (4 bits)**: Header length in 32-bit words
- **Reserved (6 bits)**: Future use (must be zero)
- **Control Bits (6 bits)**: Connection state flags (URG, ACK, PSH, RST, SYN, FIN)
- **Window (16 bits)**: Flow control - bytes willing to accept
- **Checksum (16 bits)**: Error detection for header and data
- **Urgent Pointer (16 bits)**: Points to urgent data
- **Options (variable)**: Additional protocol options
- **Padding**: Ensures header ends on 32-bit boundary

### Three-Way Handshake
TCP establishes connections using a three-step process:

1. **SYN**: Client sends connection request with initial sequence number
2. **SYN-ACK**: Server acknowledges and sends its own sequence number
3. **ACK**: Client acknowledges server's sequence number

This handshake establishes synchronized sequence numbers and confirms both sides are ready for data exchange.

### Connection Management States
TCP connections progress through defined states:
- **CLOSED**: No connection exists
- **LISTEN**: Waiting for connection requests
- **SYN-SENT**: Connection request sent, awaiting response
- **SYN-RECEIVED**: Connection request received, response sent
- **ESTABLISHED**: Connection active, data transfer possible
- **FIN-WAIT-1**: Local close initiated
- **FIN-WAIT-2**: Remote close acknowledgment received
- **CLOSE-WAIT**: Remote close received, local close pending
- **CLOSING**: Both sides closing simultaneously
- **LAST-ACK**: Final acknowledgment pending
- **TIME-WAIT**: Waiting to ensure remote received close acknowledgment

## Fundamental TCP Features

### Reliable Data Transfer
TCP ensures reliability through:
- **Sequence numbers**: Every byte numbered for ordering
- **Acknowledgments**: Receiver confirms data receipt
- **Retransmission**: Lost data automatically resent
- **Duplicate detection**: Repeated data identified and discarded

### Flow Control
TCP prevents buffer overflow using:
- **Sliding window**: Receiver advertises available buffer space
- **Dynamic adjustment**: Window size changes based on capacity
- **Zero window**: Receiver can pause transmission when full

### Error Detection and Recovery
TCP handles transmission errors through:
- **Checksums**: Detect corrupted data
- **Timeouts**: Detect lost packets
- **Fast retransmit**: Quick recovery from packet loss
- **Selective acknowledgment**: Efficient handling of multiple losses

### Congestion Control
TCP adapts to network conditions via:
- **Slow start**: Gradual increase in transmission rate
- **Congestion avoidance**: Careful rate adjustment when network busy
- **Fast recovery**: Quick adaptation to temporary congestion
- **Additive increase/multiplicative decrease**: Stable convergence algorithm

## Impact on Internet Development

### TCP/IP Protocol Suite
Combined with RFC 791 (IP), RFC 793 established:
- **Layered architecture**: Clear separation of concerns
- **End-to-end reliability**: Applications don't need to handle network errors
- **Universal connectivity**: Any TCP application can communicate with any other
- **Scalable design**: Protocols work across networks of any size

### Application Development Foundation
TCP enabled development of:
- **Web browsing**: HTTP relies on TCP for reliable page delivery
- **Email**: SMTP uses TCP for reliable message transfer
- **File transfer**: FTP depends on TCP for accurate file delivery
- **Remote access**: SSH and Telnet use TCP for reliable connections

### Internet Infrastructure
TCP became essential for:
- **Network reliability**: Handling unreliable underlying networks
- **Performance optimization**: Adapting to varying network conditions
- **Interoperability**: Universal standard for reliable communication
- **Quality of service**: Ensuring acceptable application performance

## Technical Innovations

### Adaptive Algorithms
RFC 793 introduced self-adjusting mechanisms:
- **Round-trip time estimation**: Dynamic timeout calculation
- **Window scaling**: Adaptation to network capacity
- **Congestion detection**: Recognition of network overload
- **Recovery strategies**: Multiple approaches to error correction

### State Machine Design
TCP's formal state machine provided:
- **Predictable behavior**: Clear rules for all situations
- **Robust implementation**: Standardized handling of edge cases
- **Debugging support**: Well-defined states aid troubleshooting
- **Protocol evolution**: Framework for future enhancements

## Modern Relevance

### Contemporary Usage
TCP remains fundamental to:
- **World Wide Web**: HTTPS and HTTP over TCP
- **Email systems**: SMTP, IMAP, POP3 over TCP
- **File sharing**: FTP, SFTP, and peer-to-peer protocols
- **Real-time communication**: Many VoIP and video systems
- **Database connections**: Most database protocols use TCP
- **Cloud services**: API calls and web services

### Performance Evolution
Modern TCP implementations include:
- **High-speed extensions**: Support for gigabit+ networks
- **Mobile optimizations**: Adaptations for wireless networks
- **Datacenter improvements**: Low-latency, high-throughput variants
- **Congestion control advances**: BBR, CUBIC, and other algorithms

## Design Philosophy

### End-to-End Principle
TCP embodies the internet design principle that:
- Intelligence belongs at network endpoints
- Network core remains simple and robust
- Applications control their communication requirements
- Reliability implemented where it's needed

### Robustness Principle
Following the "Be liberal in what you accept, conservative in what you send" philosophy:
- Tolerant of variations in implementation
- Strict in protocol compliance
- Graceful degradation under stress
- Interoperability across diverse systems

## Legacy and Impact

### Internet Foundation
TCP/IP became:
- The universal internet protocol suite
- Foundation for the World Wide Web
- Basis for virtually all internet applications
- Model for network protocol design

### Technical Influence
RFC 793's design principles influenced:
- Development of other transport protocols
- Network programming interfaces (sockets)
- Distributed system design
- Modern microservice architectures

## Archival Information

**Primary Source**: RFC Editor (rfc-editor.org)  
**Standard Number**: STD 7  
**Related Standards**:
- RFC 791 (Internet Protocol)
- RFC 1122 (Host Requirements)
- RFC 5681 (TCP Congestion Control)
- RFC 7323 (TCP Extensions for High Performance)

## Significance Statement

RFC 793, together with RFC 791, created the TCP/IP protocol suite that became the universal foundation for internet communication. TCP's reliable transport service enabled the development of the World Wide Web, email, file sharing, and countless other applications that define modern digital communication.

---

## Related Documents in This Collection

### Protocol Suite Partnership
- **[RFC 791: Internet Protocol](RFC_791_Internet_Protocol.md)** - TCP and IP work together as the TCP/IP protocol suite, with TCP providing reliable, ordered delivery service on top of IP's unreliable datagram service. These companion specifications define the core protocols of the internet.

### RFC Series Foundation
- **[RFC 1: Host Software](RFC_1_Host_Software.md)** - The collaborative RFC process established by RFC 1 enabled the development of TCP through open discussion and community input.

### Network Applications
- **[RFC 822: Internet Text Messages](RFC_822_Internet_Text_Messages.md)** - Email systems use TCP's reliable delivery service to ensure messages are transmitted without loss or corruption between mail servers.

- **[RFC 2616: HTTP/1.1](RFC_2616_HTTP_1_1.md)** - The World Wide Web depends on TCP's connection-oriented, reliable service for web page delivery and interactive applications.

### Networking Evolution
- **[ARPANET Foundational Papers](ARPANET_Foundational_Papers.md)** - RFC 793 implements the internetworking vision described in foundational ARPANET papers, particularly Cerf and Kahn's original TCP/IP design.

### Theoretical Foundations
- **[A Mathematical Theory of Communication](Shannon_Mathematical_Theory_Communication.md)** - TCP's error detection, flow control, and congestion control algorithms implement Shannon's theoretical insights about reliable communication over noisy channels.

- **[On Computable Numbers](Turing_On_Computable_Numbers.md)** - TCP's state machine and algorithmic approach to reliable delivery represent practical applications of computational theory.

### System Architecture
- **[First Draft of a Report on the EDVAC](Von_Neumann_EDVAC_Report.md)** - Von Neumann architecture computers implement TCP's complex algorithms for connection management and reliable delivery.

### Software Engineering
- **[Go To Statement Considered Harmful](Dijkstra_Go_To_Statement_Considered_Harmful.md)** - TCP's state machine design embodies structured programming principles, avoiding the chaotic control flow that Dijkstra criticized.

- **[The Art of Computer Programming](Knuth_Art_of_Computer_Programming.md)** - TCP implementations use many of the algorithms and data structures that Knuth documented, particularly for queue management and optimization.

### Internet Infrastructure
TCP represents the practical realization of reliable network communication, building on the theoretical foundations and collaborative processes documented throughout this collection. Together with IP, TCP created the infrastructure that enables all modern internet applications and services.

*"TCP is based on concepts first described by Cerf and Kahn in [CERF74]. The TCP fits into a layered protocol architecture just above a basic Internet Protocol which provides a way for the TCP to send and receive variable-length segments of information enclosed in internet datagram 'envelopes'."* - RFC 793