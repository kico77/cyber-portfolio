# Room: Into into LAN

**Date**: 12-11-2025

**Main task**: Learn about some of the technologies and designs that power private networks

## Notes

**Local Area Network (LAN) Topologies**

When we refer to the term "topology", we are actually referring to the design or look of the network at hand

Types of topoligies:

- Star

The main premise of a star topology is that devices are individually connected via a central networking device such as a switch or hub

- Bus

This type of connection relies upon a single connection which is known as a backbone cable

- Ring

Devices such as computers are connected directly to each other to form a loop (also known as token topology)

**What is a switch?**

Switches are dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet. These various devices plug into a switch's port. Switches are usually found in larger networks such as businesses, schools, or similar-sized networks, where there are many devices to connect to the network

**What is a router?**

It's a router's job to connect networks and pass data between them

Routing is the label given to the process of data travelling across networks. Routing involves creating a path between networks so that this data can be successfully delivered

**Subnetting**

Subnetting is the term given to splitting up a network into smaller, miniature networks within itself

Subnetting is achieved by splitting up the number of hosts that can fit within the network, represented by a number called a subnet mask

Subnets use IP addresses in three different ways:

- Identify the network address
- Identify the host address
- Identify the default gateway

**ARP**

Devices can have two identifiers: A MAC address and an IP address, the **A**ddress **R**esolution **P**rotocol or **ARP** for short, is the technology that is responsible for allowing devices to identify themselves on a network

When devices wish to communicate with another, they will send a broadcast to the entire network searching for the specific device. Devices can use ARP to find the MAC address (and therefore the physical identifier) of a device for communication

_How does ARP Work?_

Each device within a network has a ledger to store information on, which is called a cache. In the context of ARP, this cache stores the identifiers of other devices on the network.

In order to map these two identifiers together (IP address and MAC address), ARP sends two types of messages:

1. ARP Request

2. ARP Reply

When an ARP request is sent, a message is broadcasted on the network to other devices asking, "What is the mac address that owns this IP address?" When the other devices receive that message, they will only respond if they own that IP address and will send an ARP reply with its MAC address. The requesting device can now remember this mapping and store it in its ARP cache for future use.

**DHCP**

IP addresses can be assigned either manually, by entering them physically into a device, or automatically and most commonly by using a **DHCP** (**D**ynamic **H**ost **C**onfiguration **P**rotocol) server

When a device connects to a network, if it has not already been manually assigned an IP address, it sends out a request (DHCP Discover) to see if any DHCP servers are on the network. The DHCP server then replies back with an IP address the device could use (DHCP Offer). The device then sends a reply confirming it wants the offered IP Address (DHCP Request), and then lastly, the DHCP server sends a reply acknowledging this has been completed, and the device can start using the IP Address (DHCP ACK)



