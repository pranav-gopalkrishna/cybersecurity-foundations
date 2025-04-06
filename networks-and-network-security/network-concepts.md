<h1>NETWORK CONCEPTS</h1>

**_Network concepts about network design and functions_**

---

**Contents**:

- [Motivation](#motivation)
- [Key Concepts](#key-concepts)
  - [Network](#network)
  - [Network Addresses](#network-addresses)
  - [Network Diagram](#network-diagram)
  - [Network Types](#network-types)
    - [LAN](#lan)
    - [WAN](#wan)
- [Common Network Devices](#common-network-devices)
  - [Hub](#hub)
  - [Switch](#switch)
  - [Router](#router)
  - [Modem](#modem)
- [Wireless Access Point](#wireless-access-point)
- [Virtualisation Tools](#virtualisation-tools)
- [Software-Defined Network](#software-defined-network)
  - [Benefits of SDNs](#benefits-of-sdns)

---

# Motivation
Securing a network

=> Understsanding basic design of a network and how it functions

# Key Concepts
## Network
A group of connected\* devices.

\* Connected => Capable of communication with each other

## Network Addresses
Devices need to find each other on a network to connect.

-> These devices will use unique addresses/identifiers

_These are called the IP and MAC addresses._

---

- IP = Internet Protocol
    - Identify device locations in overall network
    - Public IP:
        - Provided by ISP\* for specific geographical region
        - Allows devices in that region to connect to internet
    - Private IP:
        - Assigned specific devices in specific geographical region
        - Allows communications to be directed to intended devices
- MAC = Medium Access Control / Media Access Control
    - Identify devices in network segment (part of overall network)
    - Primarily assigned by device manufacturers
    - Assigned to device's network interface controller (NIC)
    - Also called:
        - Burned-in address
        - Ethernet hardware address
        - Hardware address
        - Physical address

\* _Internet Service Provider_

## Network Diagram
Map that shows the devices on the network and how they connect

=> Map to _visualise network architecture_

## Network Types
### LAN
**Local Area Network**

A network geographically limited to a specific location

=> Assigned to a unique public IP address


### WAN
**Wide Area Network**

A network spanning multiple LANs.

**NOTE**: _The Internet is technically a WAN spanning the globe._

# Common Network Devices
## Hub
Broadcasts information to every device on a _local_ network.

## Switch
Directs communications between devices on a _local_ network =>

- More secure than hubs
- Allow for one-to-one communications
- Allow for load-balancing (improving network performance) <br> _Directing traffic to specific routers based on load_

## Router
Connects a network to one or more other networks.

---

Illustrative example of usage:


_Computer on network A to send information to tablet on network B._

1. Information travels from the computer to the router
2. Router does the following:
    - Reads the destination address
    - Forwards the data to the intended network's router
3. Receiving router directs that information to the tablet

## Modem
**Modulator-Demodulator**

BACKGROUND:

- **Modulation**:
    - Alters properties of a carrier wave <br> _Carrier wave = An information-carrying periodic waveform_\*
    - Does so for transmitting specific information
- **Demodulation**: 
    - Extracts information-bearing signal from a carrier wave
    - Does so for extracting information send through carrier wave

\* _Information-bearing signal is encoded into carrier wave._

---

FUNCTION:

Converts data from...

... digital format

_into_

... format suitable for analog transmission medium, e.g:

- Telephone
- Radio

---

- Transmits data by modulating one or more carrier wave signals <br> _To encode digital info_
- Receives data by demodulating signal to recreate digital info
- GOALS:
    - Produce a signal that can be transmitted and decoded reliably
    - Extract information from such a signal

---

Hence, modem is used to connect a router to the internet, as:

- LAN's may deal with digital signals
- WAN's may use analog transmission to carry signals <br> E.g.: _Telephone lines, coaxial cables_

---

**NOTE**: _Broadband technologies handle high-volume traffic vs. modems._

# Wireless Access Point
Sends and receives digital signals over radio waves.

_Thus, creates a wireless network._

---

**Related Concept: Wi-Fi**:

Set of standards network devices use to communicate wirelessly.

_Devices with wireless adapters connect to access point using Wi-Fi._


# Virtualisation Tools
- Network tools are physical devices
- Many of their functions can be done by _virtualisation tools_

---

**Virtualisation Tools**:

- Carry out operations normally done by a network device <br> E.g.: _Hub, router, modem, etc._
- Offered by Cloud Service Providers (CSP)
- Provide opportunities for cost savings and scalability

Learn more in [Software-Defined Network](#software-defined-network).

# Software-Defined Network
Network whose one or more functions are defined by software.

**NOTE**: _SDNs are an approach to network management._

---

Most modern network hardware devices also support:

- Network virtualisation
- Software-defined networking

=> Physical switches/routers use software to do packet routing

---

For cloud networking, SDN tools are hosted on the CSP's servers.

## Benefits of SDNs
Enable network configurations that are:

- Dynamic (or can be dynamically defined)
- Logically/algorithmically efficient

These can improve network performance and monitoring.