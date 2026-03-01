# NAT (Network Address Translation) — This is a technology that allows multiple devices on a private network to access the internet using only one shared public IP address.

- What is it?
NAT operates on a router. When your laptop (e.g., 192.168.1.10) requests a website, the router replaces your local address with its own external address (e.g., 203.0.113.50), remembers who made the request, and upon receiving the response from the internet, forwards it back to you.

- Main Types:
  - ***8Static NAT:*** A one-to-one mapping of a single internal IP address to a single external IP address (1:1).
  - ***Dynamic NAT:*** Uses a pool of public addresses for a group of internal devices.
  - ***PAT (Port Address Translation):*** The most common type (what works in your home network). Thousands of devices access the internet through a single IP address, and the router distinguishes them by their port numbers.

- Why is it important?
  - ***Conserving IPv4 Addresses:*** If every smartphone and smart device in the world needed a unique public IP address, the internet would have "run out" of addresses long ago.
  - ***Security (Topology Hiding):*** The external internet cannot see how many computers are on your network or what their internal addresses are. The router acts as a shield, not allowing incoming connections that were not requested from inside.
  - ***Convenience:*** You can change your internet service provider and your external IP address, but your internal network settings (addresses of printers, servers, etc.) remain the same.

- Why is it relevant for pentesting?
NAT is both an obstacle and a point of manipulation for a security researcher.

  - ***Barrier for Reverse Shells:*** If a computer inside a network is compromised, it cannot simply "call back" to your laptop if you are also behind NAT. Attackers need to use external servers (VPS) or port forwarding.
  - ***NAT Detection:*** Pentesters use analysis of TTL (Time to Live) values or specific packet headers to try and determine how many devices might be hidden behind a single public IP address.
  - ***Bypassing NAT (NAT Traversal):*** Techniques like STUN/TURN or UDP Hole Punching allow two devices behind different NATs to establish direct communication. Attackers may use this to maintain communication with malware.
  - ***Attacks on the Translation Table:*** Flooding a router with a massive number of requests can overflow its NAT table, leading to a Denial of Service (DoS) for the entire local network.



## RFC 1918 specifies private IP ranges

- Class|	Address Range               |	Mask (CIDR) |	Number of Addresses |	Where Typically Used
- A	   |10.0.0.0 — 10.255.255.255     |	/8	        |~16.7 million	      |Large corporations
- B	   |172.16.0.0 — 172.31.255.255   |	/12	        |~1 million	          |Medium-sized networks, VPNs
- C	   |192.168.0.0 — 192.168.255.255 |	/16	        |65,536	              |Small offices, home networks

