<h1>NETWORK MODELS</h1>

---

**Contents**:

- [Introduction](#introduction)
- [TCP/IP Model](#tcpip-model)
  - [Breaking Down the Terms](#breaking-down-the-terms)
  - [The 4 Layers of TCP/IP Model](#the-4-layers-of-tcpip-model)
    - [1. Network Access Layer](#1-network-access-layer)
    - [2. Internet Layer (also called "Network Layer")](#2-internet-layer-also-called-network-layer)
    - [3. Transport Layer](#3-transport-layer)
    - [4. Application Layer](#4-application-layer)
  - [Protocols Per Layer](#protocols-per-layer)
- [OSI Model](#osi-model)
  - [7 Layers](#7-layers)
    - [1. Physical Layer](#1-physical-layer)
    - [2. Data Link Layer](#2-data-link-layer)
    - [3. Network Layer](#3-network-layer)
    - [4. Transport Layer](#4-transport-layer)
    - [5. Session Layer](#5-session-layer)
    - [6. Presentation Layer](#6-presentation-layer)
    - [7. Application Layer](#7-application-layer)

---

# Introduction
**Network Models**:

Conceptual organisation of network components and their functions.

=>

- Hierarchy of information complexity
- Division of layers by broad functionality
- Visualisation of how data is organised and transmitted

# TCP/IP Model
## Breaking Down the Terms
- TCP = Transmission Control Protocol
    - Internet communication protocol for 2 devices to:
        - Form a connection
        - Stream data (once connection is formed)
    - Includes instructions to organise data <br> _So it can be sent across a network_
- IP = Internet Protocol
    - Standards for routing and addressing data packets <br> _As they travel between devices on a network_
    - IP address is a part of these standards <br> _Functions as an address for each private network_

---

**NOTE**: TCP-based network is not limited to just 2 devices

- Establishes direct connection between two endpoints
- But underlying network infrastructure can handle multiple <br> _It can handle routing data packets across multiple devices_

## The 4 Layers of TCP/IP Model
TCP/IP model has 4 layers:

1. Network access layer
2. Internet layer
3. Transport layer
4. Application layer

_Higher layers rely on the functionality of lower layers._

### 1. Network Access Layer
FOCUS: _The physical aspects of communications._

Involves:

- Creation of data packets
- Transmission of data packets across a network; this includes:
    - Hardware devices connected to physical cables
    - Switches that direct data to their destination

### 2. Internet Layer (also called "Network Layer")
FOCUS: _Accurate routing of data packets._

Involves:

- Defining sender and receiver locations <br> _Using IP addresses_
- How networks connect to each other
- Determine routing of data packets (locally or remotely)

### 3. Transport Layer
FOCUS: _Flow of network traffic._

Involves:

- Control of the flow of traffic across a network
- Permitting/denying communication between devices
- Information about the status of the connection
- Error control (i.e. detection and/or correction)

### 4. Application Layer
FOCUS: _Interaction between data packets and receiving devices._

Involves:

- Determining the purpose of received data packets, e.g.:
    - File transfers
    - Email services
- Determining the way data packets must be processed
- Making network requests or responding to requests
- Defining internet services and applications users can access

## Protocols Per Layer
**NOTE**:

- CN = Computer Network
- Technologies are italicised
- Protocols are put in bold font

| Layer | Techs/Protocols | Description |
| --- | --- | --- |
| 1 | _Ethernet_ | <ul><li>Family of wired CN technologies</li><li>Commonly used in local area networks</li> |
| 1 | _Wireless LAN_ | Generally implemented with Wi-Fi |
| 2 | **IP** | [Internet Protocol](./network-concepts.md#network-addresses) |
| 3 | **TCP** | [Transmission Control Protocol](#breaking-down-the-terms) |
| 3 | **UDP** | User Datagram Protocol: <br> <li>Connectionless* protocol</li><li>Unconcerned with transmission reliability</li><li>Useful for performance-sensitive use-cases</li> |
| 4 | **HTTP** | Hypertext Transfer Protocol |
| 4 | **SMTP** | Simple Mail Transfer Protocol |
| 4 | **SSH** | Secure Shell |
| 4 | **FTP** | File Transfer Protocol |
| 4 | **DNS** | Domain Name System |

\* Connectionless => Does not try to establish connection

# OSI Model
## 7 Layers
1. Physical Layer
2. Data Link layer
3. Network Layer
4. Transport Layer
5. Session Layer
6. Presentation Layer
7. Application Layer

---

Correspondence with TCP/IP model layers (given on the right):

```
7 |
6 |
5 |__Application Layer

4 |__Transport Layer

3 |__Internet Layer

2 |
1 |__Network Access Layer
```

### 1. Physical Layer
Physical hardware involved in network transmissions.

### 2. Data Link Layer
Sending/receiving data packets within a single (local) network.

### 3. Network Layer
Routing from the sending network to the receiving network.

**NOTE**: _These could be the same network._

### 4. Transport Layer
Delivering data appropriately between devices.

---

Involves:

- Handling the speed and rate of data transfer \[1\]
- Segmenting data to facilitate transportation and processing \[2\]

---

\[1\] Transmission speed/rate to match destination connection speed.

\[2\] Segments need to be reassembled at their destination.

### 5. Session Layer
Managing sessions, i.e. established device-to-device connections.

**NOTE**: _Open session allows device-to-device communication._

---

Involves:

- Manage session opening and termination:
    - Keep the session open while data is being transferred
    - Terminate the session once the transmission is complete. 
- Authentication
- Reconnection
- Setting checkpoints during a data transfer <br> _If session is interrupted, next session resumes transmission_

---

**NOTE**: Functions in session layer:

- Respond to requests for service from processes in layer 6
- Send requests for services to layer 4

### 6. Presentation Layer
Data translation in network communications, which means:

- Translation between data formats of systems
    - Sender and receiver may use different formats
    - Presentation layer standardises their interface
- Encryption/decryption
- Compression/extraction

---

Some formatting functions that occur at layer 6:

- Encryption and decryption
- Compression and extraction
- Confirmation of interpretable character code set <br> _I.e. that can be interpreted on the receiving system_

---

E.g.: SSL\* encrypts data between servers and browsers with HTTPS.

\* _SSL = Secure Socket Layer_

### 7. Application Layer
User connection to the internet via applications and requests.

---

E.g.:

- Web browser uses HTTP to send/receive info from website server
- Email app uses SMTP to send/receive email info
- Browsers use DNS to get IP addresses for website domain names\*

\* _To identify the web server hosting info for the website._