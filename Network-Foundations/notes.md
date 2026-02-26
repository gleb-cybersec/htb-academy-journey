# Network
   A network is a group of interconnected devices that can exchange data and share resources.
   
   - Key concepts:
     - ***Nodes*** are individual devices connected to the network.
     - ***Communication*** channels are the data transmission paths that connect network nodes (wired or wireless).
     - ***Data Sharing*** is the key purpose of a network, allowing devices to exchange information with each other.

  - Benefits:
    - ***Resource sharing***
    - ***Communication***
    - ***Access to data from any connected device***
    - ***Collaboration even from a distance***

  - Types:
    - **Local Area Network (LAN)** - connects devices over a short distance
      - Сharacteristics:
          - 1. Covers a small area;
          - 2. Belongs to one person or one organization
          - 3. High data transfer speed
          - 4. Uses wired or wireless connections.
    - **Wide Area Network (WAN)** - connects multiple LANs
        - Characteristic:
          - 1. Covers a lager area;
          - 2. Collective or distributed ownership
          - 3. Speed is slower than that of a LAN
          - 4. Utilizes fiber optics, satellite links, and leased telecommunication lines.


# OSI Model

## Layer 1 - Physical
Ethernet cables, hubs, and repeaters
deals with the physical connection

## Layer 2 - Data Link
Protocols: MAC (Media Access Control) addresses, switches, bridges
node-to-node data transfer

## Layer 3 - Network
IP addressing and routing.
Important for pivoting and internal discovery

## Layer 4 - Transport
Protocols: TCP, UDP
Used during port scanning.

## Layer 5 - Session
Protocols: APIs (Application Programming Interfaces), session protocols
creation of checkpoints and recovery

## Layer 6 - Presentation
Protocols: encryption, data compression
decryption, data compression, converting data formats

## Layer 7 - Application
Protocols: HTTP(Hypertext Transfer Protocol), FTP(File Transfer Protocol), SMTP (Simple Mail Transfer Protocol), DNS (Domain Name System)
a software interface that enables interaction between network services and application software


# TCP/IP Model

## Layer 1 - Link
NICs, Ethernet cables, modems, swithes
physical aspects of network hardware and media

## Layer 2 - Internet 
IP (Internet Protocol),  ICMP (Internet Control Message Protocol), routers, firewalls
logical addressing and routing 

## Layer 3 - Transport
TCP (Transmission Control Protocol), UDP (User Datagram Protocol)
end-to-end communication

## Layer 4 - Application 
HTTP (Hypertext Transfer Protocol), FTP (File Transfer Protocol), and SMTP (Simple Mail Transfer Protocol)
specific data communication



# Transmission Types

## Analog
uses continuous signals

##Digital
uses discrete signals (bits)



# Transmission Modes

## Simplex 
implements one-way communication

## Half-duplex mode
implements two-way communication, but not simultaneous

## Full-duplex
provides simultaneous two-way communication



# Components of a Network

## End Devices
A device that sends and receives data on a network(computers and smart devices). 
Allow users to seamlessly access network resources and services via wired and wireless connection.

## Intermediary Devices
Ensure the flow of data between end devices both within the local network and across different networks( routers, switches, modems, and access points)
Connect networks and manage traffic to improve performance and reliability
      
   - ## Network Interface Cards (NICs)
     A hardware device (card or adapter) that provides the physical connection of a computer to the network(has a unique MAC address)

   - ## Routers
     Forwarding data packets between networks and managing internet traffic.
     Protocols: Open Shortest Path First (OSPF), Border Gateway Protocol (BGP)
     Enhance security through the use of firewalls and access control lists

   - ## Switches
     A device that connects multiple computers and other equipment together within a single local area network (LAN).    
     Use MAC addresses

   - ## Hubs
     Connects devices on a network and forwards incoming traffic to all ports simultaneously, without considering the specific recipient(antiquated).

## Network Media and Software Components
***Network media*** provide the pathways for data movement: information, converted into signals, travels along these physical routes from the sender to the receiver.
- Wired: Ethernet cables, fiber-optic cables;
- Wireless: Wi-Fi, Bluetooth
***Software components*** A set of algorithms and syntactic rules that ensure correct interaction between network nodes. They govern the processes of encapsulation, addressing, switching, and data delivery at all stages.
- Protocols: TCP/IP, HTTP, FTP

## Servers
This is a powerful computer that operates on a network and provides its resources or services to other computers — the clients.
