# DHCP (Dynamic Host Configuration Protocol) — This is a network protocol that acts like an "automatic administrator." Its main task is to provide devices with all the necessary settings to connect to the network without human intervention.

- What is it?
Imagine you walk into a café with your laptop. To access the internet, you need: an IP address, a subnet mask, a gateway (router) address, and a DNS server. Instead of entering them manually, your computer "shouts" into the network: "I'm new here, give me the settings!", and the DHCP server immediately sends them.

- The process of obtaining an address is called DORA:
  - ***Discover:*** The client searches for a server.
  - ***Offer:*** The server offers an IP address.
  - ***Request:*** The client agrees to the offer.
  - ***Acknowledgment:*** The server finalizes the lease.

- Why is it important?
  - ***Automation:*** In an office with 500 people, a system administrator would have to spend a week configuring each device manually. DHCP does it in seconds.
  - ***Conflict Prevention:*** The server ensures that two devices do not accidentally receive the same IP address (which would cause a network malfunction).
  - ***Mobility:*** You can move between Wi-Fi access points, and your device will smoothly obtain new settings.

- Why is it relevant for pentesting?
  DHCP is a protocol based on "blind trust," which makes it an excellent target for attacks within a network.
  
  - DHCP Starvation: An attacker generates thousands of requests with fake MAC addresses, filling up the server's entire IP address table. The result: legitimate users cannot connect to the network (a DoS attack).
  - Rogue DHCP Server: A pentester runs their own DHCP server. When a new client requests settings, the fake server responds faster than the real one and gives the client its own IP address as the gateway.
  - Man-in-the-Middle (MITM): If a client accepts settings from the hacker, all their traffic now flows through the pentester's device. This allows for intercepting passwords, reading correspondence, or replacing files on the fly.
  - Information Gathering: DHCP packets can reveal computer names, types of operating systems, and the structure of the internal network even before active scanning begins.
