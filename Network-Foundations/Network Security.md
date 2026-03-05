## CIA triad
| Principle | Description |
|-----------|-------------|
| Confidentiality | Only authorized users can view the data |
| Integrity | The data remains accurate and unaltered |
| Availability | Network resources are accessible when needed |


## Firewall 
This is the "border control" of your network. It is a software or hardware solution that analyzes incoming and outgoing traffic and decides whether to allow it or block it, based on a set of predefined security rules.

- Types of Firewalls:
  - **Packet Filtering:** Inspects only the packet headers (source IP, destination IP, port). It's fast but operates at a shallow level.
  - **Stateful Inspection:** Keeps track of the state of active connections. It will only allow traffic that is part of a legitimate, previously established connection. If you didn't request data from a particular source, it won't be allowed in.
  - **NGFW (Next-Generation Firewall):** These intelligent firewalls look "inside" the packet to identify specific applications. For example, they might allow Skype traffic but block file transfers within Skype.
  - **WAF (Web Application Firewall):** Specialized protection for websites, designed to detect and block attacks like SQL injections and Cross-Site Scripting (XSS).

- Why is it important?
  - **Isolation:** Protects the internal company network from threats originating from the public internet.
  - **Access Control:** Allows administrators to block employee access to dangerous, unproductive, or non-compliant websites and resources.
  - **Preventing Data Leaks:** Can be configured to block malicious software (malware) from successfully sending stolen data out to an attacker's server (egress filtering).
  - **Logging:** Keeps a record of all connection attempts, which is crucial for security audits and investigating incidents.
