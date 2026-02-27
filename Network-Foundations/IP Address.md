# IP Address (Internet Protocol) — This is the dynamic mailing address of a device on a network. It is a logical address that allows data to find its path between different networks across the globe.

- What is it?
  - An IP address operates at the Internet Layer (Layer 3) of the OSI model. It determines "where" a device is located within a global or local hierarchy, they can change and are assigned based on the network topology and policies

- There are two main standards:
  - **IPv4:** The classic format (e.g., 192.168.1.15). It consists of 32 bits, divided into 4 octets. The number of combinations is limited (about 4.3 billion), which is why addresses are "running out."
  - **IPv6:** The modern format (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334). A 128-bit address, created so that there are enough resources for every device in the universe.

- Why is it important?
  - **Routing:** Routers use IP addresses to forward data packets from Moscow to New York, or from one subnet to another.
  - **Hierarchy:** IP addresses are divided into public (visible on the entire internet) and private (used inside your home or office).
  - **Connection to Domains:** Thanks to the DNS system, we type google.com into our browser, but the computer translates this into the server's IP address to send the request.

- Why is it relevant for pentesting?
The IP address is the primary target and starting point for any remote investigation.

  - **Reconnaissance:** Knowing an IP address, a pentester can perform port scanning (e.g., using nmap) to understand which services are running on the server (website, database, mail).
  - **Geolocation and Attribution:** A public IP address allows for an approximate determination of the target's city and internet service provider.
  - **Bypassing Security Systems (WAF/Firewall):** Pentesters look for the real IP address of a server hidden behind services like Cloudflare, in order to attack it directly, bypassing the filters.
  - **Spoofing (IP Spoofing):** Faking the source IP address in a packet to deceive a system's trust (for example, making a server think the request came from within its own network).
  - **Tunneling and Proxies:** To hide their own real address, researchers use chains of proxy servers or a VPN to "emerge" onto the network under a different IP.
