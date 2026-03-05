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


## IDS/IPS  
These are like security cameras with artificial intelligence combined with an immediate response team. They don't just look at where a packet came from; they analyze what that packet is actually trying to do.

- What are they?
These are systems that monitor network traffic or system activity for suspicious actions or violations of security policies.
  - **IDS (Intrusion Detection System):** An observation system. It only watches traffic and "rings the alarm" (sends a notification to the administrator) if it detects an attack. It usually operates "alongside" the traffic flow by receiving a copy of the data (like a port mirror).
  - **IPS (Intrusion Prevention System):** A prevention system. It sits directly "in-line" with the traffic flow. If it detects an attack, it immediately blocks the malicious packets, preventing them from reaching their target.

- Analysis Methods:
  - **Signature-Based:** This method looks for specific, known patterns or "fingerprints" of viruses or attacks (similar to how traditional antivirus software works).
  - **Behavioral (Anomaly-Based):** This method learns what "normal" network behavior looks like. It raises an alert if it detects a sudden, unusual deviation from the baseline, for example, an accountant's workstation trying to download the entire database using PowerShell in the middle of the night.

- Why are they important?
  - ***Protection Against Zero-Day Attacks:*** Advanced IPS solutions can sometimes recognize the underlying logic or behavior of an attack, even if the specific exploit or virus has never been seen before and has no signature.
  - ***Deep Packet Inspection (DPI):*** The system can "reassemble" and look inside packets to see that, for example, what looks like a normal HTTP request actually contains a hidden SQL injection attack.
  - ***Automation:*** In modern networks, attacks can happen far too quickly for a human to react in time. An IPS can block a threat in milliseconds, automatically.
  - ***Compliance:*** The presence of such monitoring and prevention systems is often mandatory for organizations handling sensitive data, such as banks (under standards like PCI DSS) and government agencies.
