<h1>NETWORK PROTOCOLS</h1>

---

**Contents**:

- [Definition](#definition)
- [Relevance for Security](#relevance-for-security)
- [Categories](#categories)
  - [Communication Protocols](#communication-protocols)
  - [Management Protocols](#management-protocols)
  - [Security Protocols](#security-protocols)
- [Common protocols](#common-protocols)
- [Additional Protocols](#additional-protocols)
- [Port number per protocol:](#port-number-per-protocol)

---

# Definition
Set of rules for exchange/transmission of data between devices.

---

They serve to describe:

- Order of delivery (e.g. segmentation order, priority, etc.)
- Structure of data (e.g. format for metadata, content, etc.)

---

SIMILAR TO: Interface for 2+ applications to interact.

ANALOGOUS TO: Language to communicate between 2+ people.

# Relevance for Security
Some protocols have vulnerabilities that malicious actors exploit.

E.g.: DNS to divert traffic from intended to malicious website.

# Categories
## Communication Protocols
_Govern the exchange of information in network transmission._

- Dictate how the format and timing of transmitted data
- Also include methods to recover data lost in transit

E.g.: TCP, UDP, HTTP, DNS

## Management Protocols
_Help monitor and manage activity on a network._

They include protocols for:

- Error reporting (e.g. ICMP)
- Reporting on network performance (e.g. SNMP)
- Optimising performance on the network

## Security Protocols
_Ensure data is sent and received securely across a network._

=>

_Use of encryption algorithms to protect data in transit._

E.g.: HTTPS, SFTP

---

**NOTE**: Encryption here only conceals content, not addresses\*.\

\* _Because any router must be able to read these addresses._

# Common protocols
- Transmission Control Protocol (TCP) <br> _For establishing connection and streaming data_
    - **Category**: Communication
    - **TCP/IP layer**: Transport
    - Steps to establish (SYN => synchronise, ACK => acknowledge): <br> **_3-way handshake_**
        - Device 1 sends a SYN request to device 2 <br> _Requesting connection_
        - Device 2 sends a SYN, ACK request to device 1 <br> _Accepting connection request_
        - Device 1 sends an ACK request <br> _Acknowledging permission to connect_
- User Datagram Protocol (UDP) <br> _For sending data to a device without confirming connection_
    - **Category**: Communication
    - **TCP/IP layer**: Transport
    - Less reliable than TCP but faster due to lack of checks
    - Useful for time-efficient operations <br> E.g.: _Data streaming, repeated data requests_
    - Useful in the face of resource-constraints <br> E.g.: _Requests to a (likely busy) DNS server, video streaming, etc._
- Hypertext Transfer Protocol (HTTP) <br> _For transferring hypertext data_
    - **Category**: Communication
    - **TCP/IP layer**: Application
    - Hypertext => <br> (1) _Text containing references to other texts\*_ <br> (2) _Software system enabling text/media cross-referencing_
    - Hypertext file => <br> _File that contains/encodes hypertext features_
    - HTML is a scripting language for creating hypertext files
    - Useful for transfer of website data from servers to clients
- Domain Name System (DNS) <br> _For converting internet domain names to IP addresses_
    - **Category**: Communication
    - **TCP/IP layer**: Application
    - DNS servers act as interface between:
        - Clients using internet domain names
        - Servers hosting the corresponding resources/services
    - SIDE NOTE 1: DNS server uses UDP for general replies
    - SIDE NOTE 2: DNS server uses TCP for lengthy replies

\* E.g.: _Dictionary, encyclopedia, catalogues._

# Additional Protocols
- Network Address Translation (NAT) <br> _For converting to and from private and public IPs_
    - **Category**: Communication
    - **TCP/IP layer**: Internet and transport
    - Requires specifically configured router/firewall
- Dynamic Host Configuration Protocol (DHCP) <br> _For dynamically configuring on-network devices_
    - **Category**: Management
    - **TCP/IP layer**: Application
    - Configure devices dynamically on a network <br> => Assign IP addresses, DNS server and gateway per device
- Address Resolution Protocol <br> _For retrieving unknown MAC address given IP address_
    - **Category**: Communication
    - **TCP/IP layer**: Network access and internet
    - Obtains unknown MAC address given IP address, within LAN
- Secure Shell (SSH) <br> _For remote encrypted and persistent connections_
    - **Category**: Security
    - **TCP/IP layer**:
        - Application: Allows remote application interface
        - Transport: Uses TCP to establish connection
    - Builds on TCP => Is connection-oriented <br> _I.e. establishes a connection before data transfer_
    - Like WebSocket, maintains a persistent connection <br> _Note that WebSocket is also built on TCP_
    - PURPOSE: Remote transfer of data and instructions <br> => Remote system _file access/transfer_ + _command execution_ <br> => Remote access of another system, in effect
    - READ MORE: [_What is SSH? | Secure Shell (SSH) protocol_, **Cloudflare.com**](https://www.cloudflare.com/learning/access-management/what-is-ssh)
- Telnet (similar to SSH in function, but without encryption)
- Post Office Protocol (POP) :: _For incoming mail_ <br> _For managing and retrieving mails from a server_
    - **Category**: Communication
    - **TCP/IP layer**: Application
    - May or may not maintain mails in the server <br> => Mails may be deleted from server after downloading
- Internet Message Access Protocol (IMAP) :: _For incoming mail_  <br> _For managing and retrieving mails from a server_
    - **Category**: Communication
    - **TCP/IP layer**: Application
    - Maintains mails in the server <br> => Mails can be synchronised across devices
- Simple Mail Transfer Protocol (SMTP) :: _For outgoing mail_ <br> _For transmitting + routing mail to intended recipient_
    - **Category**: Communication
    - **TCP/IP layer**: Internet

# Port number per protocol

| Protocol | Port |
| --- | --- |
| HTTP | TCP/UDP port 80 |
| DNS | UDP port 53 (servers; clients do not implement DNS) |
| HTTPS | TCP/UDP port 443 |
| SFTP | TCP port 22 |
| DHCP | UDP port 67 (servers) <br> UDP port 68 (clients) |
| ARP | none |
| Telnet | TCP port 23 |
| SSH | TCP port 22 |
| POP3 | TCP/UDP port 110 (unencrypted) <br> TCP/UDP port 995 (encrypted, SSL/TLS) |
| IMAP | TCP port 143 (unencrypted) <br> TCP port 993 (encrypted, SSL/TLS) |
| SMTP | TCP/UDP Port 25 (unencrypted) |
| SMTPS | TCP/UDP port 587 (encrypted, TLS) |