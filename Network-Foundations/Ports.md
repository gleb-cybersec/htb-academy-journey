# Port — This is a numerical identifier (from 0 to 65535) that allows the operating system to understand which specific application an incoming network packet should be delivered to.

A single IP address (server) can simultaneously host a website, email, and file storage. Ports separate these data streams.

## Port Categories:
- ***System Ports (0–1023):*** Reserved for standard services (HTTP, FTP, SSH).
- ***User Ports (1024–49151):*** For specific software (databases, games).
- ***Dynamic/Private Ports (49152–65535):*** Temporary ports that your browser opens to receive a response from a server.

## Why is it important?
- ***Multitasking:*** Allows a single server to perform dozens of different functions simultaneously.
- ***Traffic Routing:*** Without ports, a computer wouldn't know whether an incoming byte belongs to a video call in Telegram or a page update in a browser.
- ***Security (Firewall):*** Firewalls primarily work by closing "unnecessary" ports to prevent anyone from connecting to system services from the outside.

## Why is it relevant for pentesting?
Port scanning is the foundation of any hack or audit. As long as you don't know which ports are open, you don't know what to attack.

- ***Service Identification (Banner Grabbing):*** A pentester looks not only at the port number but also at what "lives" behind it. For example, port 80 (HTTP) might hide an outdated Apache server with a known security hole.
- ***Finding "Forgotten" Entries:*** System administrators often leave ports open for testing or remote management (e.g., 3389 — RDP or 22 — SSH), forgetting to set a strong password.
- ***Exploiting Vulnerabilities:*** Each attack has its "favorite" port. For example, the WannaCry ransomware worm penetrated networks through port 445 (the SMB protocol).
- ***Bypassing Security:*** If all ports are closed except for 443 (HTTPS), a hacker will try to "smuggle" malicious traffic through that allowed channel.
