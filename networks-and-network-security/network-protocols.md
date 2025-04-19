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
  - [Transmission Control Protocol (TCP)](#transmission-control-protocol-tcp)
  - [User Datagram Protocol (UDP)](#user-datagram-protocol-udp)
  - [Hypertext Transfer Protocol (HTTP)](#hypertext-transfer-protocol-http)
  - [Domain Name System (DNS)](#domain-name-system-dns)
- [Additional Protocols](#additional-protocols)
  - [Network Address Translation (NAT)](#network-address-translation-nat)
  - [Dynamic Host Configuration Protocol (DHCP)](#dynamic-host-configuration-protocol-dhcp)
  - [Address Resolution Protocol](#address-resolution-protocol)
  - [Secure Shell (SSH)](#secure-shell-ssh)
    - [RELATED CONCEPT: SSH Tunnelling](#related-concept-ssh-tunnelling)
  - [Telnet](#telnet)
  - [Post Office Protocol (POP)](#post-office-protocol-pop)
  - [Internet Message Access Protocol (IMAP)](#internet-message-access-protocol-imap)
  - [Simple Mail Transfer Protocol (SMTP)](#simple-mail-transfer-protocol-smtp)
- [Port Number per Protocol](#port-number-per-protocol)
- [Wireless Network Protocols (WNPs)](#wireless-network-protocols-wnps)
  - [Wi-Fi (Wireless Fidelity)](#wi-fi-wireless-fidelity)
    - [Wired Equivalent Privacy (WEP)](#wired-equivalent-privacy-wep)
      - [Goals](#goals)
      - [Background facts](#background-facts)
    - [Wi-Fi Protected Access (WPA)](#wi-fi-protected-access-wpa)
      - [Goals](#goals-1)
      - [Improvements over WEP](#improvements-over-wep)
      - [Vulnerability: KRACK Attack](#vulnerability-krack-attack)
      - [Background Facts](#background-facts-1)
    - [WPA2](#wpa2)
      - [Improvements on WPA](#improvements-on-wpa)
      - [Vulnerability: KRACK Attack](#vulnerability-krack-attack-1)
      - [Setup Modes](#setup-modes)
        - [Personal](#personal)
        - [Enterprise](#enterprise)
      - [Background Facts](#background-facts-2)
    - [WPA3](#wpa3)
      - [Improvements on WPA2](#improvements-on-wpa2)
      - [Background Facts](#background-facts-3)
    - [Tabular Comparison of WES, WPA, WPA2 and WPA3](#tabular-comparison-of-wes-wpa-wpa2-and-wpa3)
    - [References](#references)
  - [Relevance of Knowing History of Wireless Protocols](#relevance-of-knowing-history-of-wireless-protocols)

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

- Dictate the format and timing of transmitted data
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
## Transmission Control Protocol (TCP)
_For establishing connection and streaming data._

- **Category**: Communication
- **TCP/IP layer**: Transport
- Steps to establish (SYN => synchronise, ACK => acknowledge): <br> **_3-way handshake_**
    - Device 1 sends a SYN request to device 2 <br> _Requesting connection_
    - Device 2 sends a SYN, ACK request to device 1 <br> _Accepting connection request_
    - Device 1 sends an ACK request <br> _Acknowledging permission to connect_

## User Datagram Protocol (UDP)
_For sending data to a device without confirming connection._

- **Category**: Communication
- **TCP/IP layer**: Transport
- Less reliable than TCP but faster due to lack of checks
- Useful for time-efficient operations <br> E.g.: _Data streaming, repeated data requests_
- Useful in the face of resource-constraints <br> E.g.: _Requests to a (likely busy) DNS server, video streaming, etc._

## Hypertext Transfer Protocol (HTTP)
_For transferring hypertext data._

- **Category**: Communication
- **TCP/IP layer**: Application
- Hypertext => <br> (1) _Text containing references to other texts\*_ <br> (2) _Software system enabling text/media cross-referencing_
- Hypertext file => <br> _File that contains/encodes hypertext features_
- HTML is a scripting language for creating hypertext files
- Useful for transfer of website data from servers to clients

## Domain Name System (DNS)
_For converting internet domain names to IP addresses._

- **Category**: Communication
- **TCP/IP layer**: Application
- DNS servers act as interface between:
    - Clients using internet domain names
    - Servers hosting the corresponding resources/services
- SIDE NOTE 1: DNS server uses UDP for general replies
- SIDE NOTE 2: DNS server uses TCP for lengthy replies

\* E.g.: _Dictionary, encyclopedia, catalogues._

# Additional Protocols
## Network Address Translation (NAT)
_For converting to and from private and public IPs._

- **Category**: Communication
- **TCP/IP layer**: Internet and transport
- Requires specifically configured router/firewall

## Dynamic Host Configuration Protocol (DHCP)
_For dynamically configuring on-network devices._

- **Category**: Management
- **TCP/IP layer**: Application
- Configure devices dynamically on a network <br> => Assign IP addresses, DNS server and gateway per device

## Address Resolution Protocol
_For retrieving unknown MAC address given IP address._

- **Category**: Communication
- **TCP/IP layer**: Network access and internet
- Obtains unknown MAC address given IP address, within LAN

## Secure Shell (SSH)
_For remote encrypted (i.e. secure) connections._

- **Category**: Security
- **TCP/IP layer**:
    - Application: Allows remote application interface
    - Transport: Uses TCP to establish connection
- Builds on TCP => Is connection-oriented <br> _I.e. establishes a connection before data transfer_
- PURPOSE: Remote transfer of data and instructions <br> => Remote system _file access/transfer_ + _command execution_ <br> => Remote access of another system, in effect
- READ MORE: [_What is SSH? | Secure Shell (SSH) protocol_, **Cloudflare.com**](https://www.cloudflare.com/learning/access-management/what-is-ssh)

---

SSH is a standard for:

- Secure remote logins
- File transfers over untrusted networks

A key method of achieving the above is via SSH tunnelling.

### RELATED CONCEPT: SSH Tunnelling

_Method of carrying networking data over encrypted SSH connection._

Can be used to:

- Add encryption to legacy applications
- Implement VPNs (Virtual Private Networks)
- Access intranet services across firewalls

---

**Elaboration**:

SSH gives the means secure data traffic of any application using **port forwarding**. This is called [SSH tunneling](#related-concept-ssh-tunnelling), i.e. tunnelling any TCP/IP port over SSH. This involves directing application data traffic to flow inside an encrypted SSH connection so that it cannot be eavesdropped or intercepted while it is in transit. _SSH tunneling enables adding network security to legacy applications that do not natively support encryption._

---

> **Reference**: [_SSH Tunneling_, **ssh.com**](https://www.ssh.com/academy/ssh/tunneling)

## Telnet
_Similar to SSH in function, but without encryption._

## Post Office Protocol (POP)
_For incoming mail._

I.e.:

_For managing and retrieving mails from a server._

- **Category**: Communication
- **TCP/IP layer**: Application
- May or may not maintain mails in the server <br> => Mails may be deleted from server after downloading

## Internet Message Access Protocol (IMAP)
_For incoming mail._

I.e.:

_For managing and retrieving mails from a server._

- **Category**: Communication
- **TCP/IP layer**: Application
- Maintains mails in the server <br> => Mails can be synchronised across devices

## Simple Mail Transfer Protocol (SMTP)
_For outgoing mail._

I.e.:

_For transmitting + routing mail to intended recipient._

- **Category**: Communication
- **TCP/IP layer**: Internet

# Port Number per Protocol

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

# Wireless Network Protocols (WNPs)
Define rules and standards for communication on wireless networks.

Wireless technology examples:

- Radio waves
- VIsible light (e.g. tight-beam lasers)
- Sonic waves

---

**KEY POINT**:

- WNPs are solutions for:
    - [Network Access Layer](./network-models.md#1-network-access-layer) (TCP/IP model)
    - [Physical Layer](./network-models.md#1-physical-layer) and [Data Link Layer](./network-models.md#2-data-link-layer) (OSI model)
- Higher-layer protocols (TCP, HTTP, DNS, etc.) can build on WNPs

## Wi-Fi (Wireless Fidelity)
A set of...

- standards
- protocols

... that define communication for wireless _LANs_.

---

**KEY POINTS**:

- Wi-Fi is a suite of protocols, not a single protocol
- Wi-Fi uses high-frequency radio waves

---

**NOTE: Background Facts about Wi-Fi**:

Wi-Fi is...

- A marketing term commissioned by WECA
    - WECA = Wireless Ethernet Compatibility Alliance
    - WECA has since renamed their organisation Wi-Fi Alliance
- Based on IEEE's 802.11 family of internet communication standards
    - IEEE = Institute of Electrical and Electronics Engineers
    - Hence, Wi-Fi may be referred to as IEEE 802.11

---

**NOTE**: _The below protocols are part of the Wi-Fi family._

### Wired Equivalent Privacy (WEP)
#### Goals
Ensure:

Level of privacy in wireless network communications

=

Level of privacy as on wired network connections

#### Background facts
- Developed in 1999
- Is the oldest of the wireless security standards
- Too old to support newer Wi-Fi security protocols <br> _Hence, considered a high-risk protocol_

### Wi-Fi Protected Access (WPA)
#### Goals
- Improve upon WEP
- Address the security issues that it presented
- Replace it (by enabling backward compatibility with old hardware)

_Intended to be a transitional measure to fix WEP's flaws._

#### Improvements over WEP
- Use of Temporal Key Integrity Protocol (TKIP)
- Use of larger secret keys than WEP for encryption <br> _Making brute-force breaches harder_
- Includes a **message integrity check**
    - This includes a message authentication tag per transmission
    - Attempts to either... <br> 1) alter the transmission in any way <br> 2) resend at another time <br> ...  are thwarted by WPA's message integrity check <br> _Which will identify the attack and reject the transmission_
#### Vulnerability: KRACK Attack
**KRACK Attack**:

**Key reinstallation attack** to decrypt transmissions using WPA.

---

Attack outline:

- Insert oneself in the WPA authentication handshake process
- Insert a new encryption key <br> _Instead of the dynamic key assigned by WPA_
- Setting new key to all zeros == No encryption in transmission

---

Elucidation:

- Handshake => Process of establishing wireless connection <br> _Done before sending the data; e.g.: [TCP's SYN-SYN,ACK-ACK](#transmission-control-protocol-tcp)_
- Handshake involves communication about encryption key to be used
    - Lets receiving device to decrypt sender's encrypted messages
    - Involves unencrypted data; can let attackers infer the key\* <br> _Since not both devices know encryption key at first_
- An interceptor may acquire and alter the encryption key used <br> _To either all 0s or to a key known to them_
- Hence, ensuing data transmission can be interpreted by them

\* _This is not necessarily direct communication of keys._

---

WPA2 aims to overcome this significant vulnerability.

#### Background Facts
- Developed in 2003
- Ensures backward compatibility with older hardware
- Intended as a transitional measure to fix WEP's flaws

### WPA2
#### Improvements on WPA
WPA2 improves upon WPA by:

- Using Advanced Encryption Standard (AES) instead of TKIP <br> _Provides stronger encryption compared to TKIP_
- Improving on WPA's use of TKIP
- Using CCM Mode Protocol (CCMP) <br> _CCM = Counter with Cipher Block Chaining Message Authentication_
    - Provides encapsulation <br> _Encapsulation = Containing data packets in encrypted packets_
    - Ensures message authentication and integrity
    - Sources: [_CCMP (cryptography)_, **Wikipedia.org**](https://en.wikipedia.org/wiki/CCMP_(cryptography)), [_CCM mode_, **Wikipedia.org**](https://en.wikipedia.org/wiki/CCM_mode)

#### Vulnerability: KRACK Attack
To read on KRACK attacks, see: ["Vulnerability: KRACK Attack" (previous section)](#vulnerability-krack-attack).

This vulnerability led to the development of WPA3 in 2018. 

#### Setup Modes
##### Personal
Best suited for home networks for a variety of reasons:

- Easy to implement
- Initial setup takes less time for personal <br> _Compared to enterprise version_

---

Setup outline:

- There exists a global passphrase for WPA2 personal version
- ↑ Must be applied to each computer and access point in a network
- => Ideal for home networks, but unmanageable for organisations 

##### Enterprise
Works best for business applications, as it provides:

- Necessary security for wireless networks in business settings
- Individualised and centralised control over the Wi-Fi access <br> _To a business network_ <br> => Network admins can easily grant/remove user access to network

---

Furthermore, users never have access to encryption keys

=>

Potential attackers cannot recover keys on individual computers

#### Background Facts
- Released in 2004
- Aims to improve on WPA
- Considered security standard for all Wi-Fi transmissions today <br> _Due to its security strength_

### WPA3
#### Improvements on WPA2
_Addresses authentication handshake vulnerability to KRACK._

How?

By using Simultaneous Authentication of Equals (SAE), a...

- password-authenticated
- cipher-key-sharing

... agreement. 

Prevents attackers from downloading data from wireless network

=> They cannot attempt to decode the data in their systems

---

_Increased encryption to make passwords more secure._

How?

By using 128-bit encryption.

**NOTE**: _WPA3-Enterprise mode offers optional 192-bit encryption._

#### Background Facts
- Is a secure Wi-Fi protocol
- Growing in usage as more WPA3 compatible devices are released

### Tabular Comparison of WES, WPA, WPA2 and WPA3
| Protocol | Year | Encryption | Vulnerabilities | Status |
| --- | --- | --- | --- | --- |
| WEP | 1999 | RC4 (static) | Easily cracked | Obsolete |
| WPA | 2003 | TKIP | KRACK | Deprecated |
| WPA2 | 2004 | AES + CCMP | KRACK | Standard |
| WPA3 | 2018 | AES + SAE | Few known | Emerging |

### References
- [_What is WPA3 vs. WPA2?_, **portnox.com**](https://www.portnox.com/cybersecurity-101/wpa3)
    - Compares WPA3 handshake to WPA2's
    - Discusses WPA3's superior encyrption
    - Discusses WPA3's superior IoT support
- [_WPA vs WPA2_, **AVG.com**](https://www.avg.com/en/signal/what-is-wpa2)
    - Mentions WPA2 replaces TKIP encryption with AES encryption
    - Discusses WPA2's dynamic key encryption system
- [_WPA and WPA2 4-Way Handshake_, **NetworkLessons.com**](https://networklessons.com/wireless/wpa-and-wpa2-4-way-handshake)
    - More detailed overview of handshake process in WPA and WPA2
    - Looks at packets captured via Wireshark to illustrate
- [_Wireless security: WEP, WPA, WPA2 and WPA3 differences_, **TechTarget.com**](https://www.techtarget.com/searchnetworking/feature/Wireless-encryption-basics-Understanding-WEP-WPA-and-WPA2)
    - Deeper comparison of WEP, WPA, WPA2 and WPA3
    - Deeper look into KRACK and other vulnerabilities
- [_IEEE 802.11 Architecture_, ](https://www.geeksforgeeks.org/ieee-802-11-architecture/)
    - Deeper overview of Wi-Fi as a whole
    - More detailed discussion of IEEE 802.11 specifications
    - Discussion of IEEE 802.11's advantages and disadvantages

## Relevance of Knowing History of Wireless Protocols
- Older systems/admin settings may use older protocols
- Helps understand/justify design choices behind current protocols
    - Helps grasp tradeoffs/necessary vulnerabilities
    - Helps grasp how threats have evolved over time
- Helps keep you aware of what updates to watch out for <br> _Hence, helps keep you up-to-date with latest protocols_
- Improves your own grasp of network security <br> _By learning from past design choices/implementations_