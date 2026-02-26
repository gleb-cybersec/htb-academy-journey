## MAC Address (Media Access Control) — This is a unique identifier assigned to each network interface card (NIC) during manufacturing. If an IP address can be compared to a mailing address that changes when you move, then a MAC address is like a passport serial number or a car's VIN (Vehicle Identification Number).

- What is it?
  - It is the "hardware" address of a device, operating at the Data Link layer (Layer 2) of the OSI model. It is necessary for data within a local network (Ethernet or Wi-Fi) to know exactly which physical port it needs to be delivered to.

- Structure:
  - It typically consists of 48 bits (6 bytes) and is written in hexadecimal format, for example: 00:1A:2B:3C:4D:5E.
  - First 3 bytes (OUI): The manufacturer's identifier (e.g., Intel, Apple, Cisco).
  - Last 3 bytes: The unique serial number of the device itself.

- Why is it important?
  - **Local Delivery:** Without MAC addresses, switches would not know where to send packets inside an office or apartment.
  - **DHCP and Static IPs:** Routers often use the MAC address to consistently assign the same IP address to your computer.
  - **Security (Basic):** MAC address filtering can allow only "authorized" devices to access the network.

- Why is this relevant for pentesting?
  For a cybersecurity specialist (or a hacker), the MAC address is a primary entry point and reconnaissance tool.
  - **Target Identification:** The first digits of a MAC address reveal the device's manufacturer. If it's "Axis Communications," it might be a camera; if it's "Cisco," it's likely networking equipment.
  - **Bypassing Filters (MAC Spoofing):** Many networks are protected by a whitelist of MAC addresses. A pentester can "sniff" the traffic, learn a legitimate address, and spoof their MAC to that one to gain network access.
  - **Man-in-the-Middle Attacks (ARP Spoofing):** An attacker can send fake ARP messages, claiming that their MAC address belongs to the network gateway. This redirects all traffic through them.
  - **Stealth:** Changing your MAC address regularly helps avoid Intrusion Detection Systems (IDS) that track suspicious activity from a specific node.
