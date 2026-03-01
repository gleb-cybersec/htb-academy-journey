# DNS (Domain Name System) — This is the "phonebook" of the internet. It translates human-friendly domain names (e.g., google.com) into computer-friendly IP addresses (e.g., 142.250.190.46).

- What is it?
When you type a website address into your browser, your computer doesn't know where to send the request. It asks a DNS server. The server looks up the name in its database and returns the corresponding IP address.

- DNS Hierarchy:
  - ***Recursive Resolver:*** The first server your computer contacts (usually your ISP's server or a public one like Google's 8.8.8.8).
  - ***Root Servers:*** These servers know where to find the servers for top-level zones like .com, .ru, etc.
  - ***Top-Level Domain (TLD) Servers:*** These are the servers for specific domain zones (like .com, .org, .ru).
  - ***Authoritative Name Server:*** The final server that holds the actual DNS records for the specific domain name (e.g., the exact IP address for google.com).

- Why is it important?
  - ***Convenience:*** People are much better at remembering words than strings of numbers.
  - ***Flexibility:*** A website administrator can move the site to a different server (changing its IP address), but for users, the address mysite.com remains the same. Only the DNS record needs to be updated.
  - ***Load Balancing:*** A single domain name can point to different IP addresses based on the user's geographic location, distributing traffic.

- Why is it relevant for pentesting?
DNS is one of the "chattiest" protocols and often leaks company secrets.

  - ***Reconnaissance (DNS Enumeration):*** Pentesters can find subdomains that a company has forgotten about (e.g., dev.company.com or test-admin.company.com). These are often less protected and run older software.
  - ***DNS Zone Transfer (AXFR):*** If a DNS server is misconfigured, it might dump its entire list of internal DNS records to anyone who asks. This is effectively a map of the organization's entire network.
  - ***DNS Spoofing (Cache Poisoning):*** An attacker poisons the cache of a DNS server with a fake record. When a user types bank.com, they are sent to the attacker's IP address, which hosts a fake copy of the bank's site designed to steal credentials.
  - ***DNS Tunneling:*** A method of hiding other types of traffic (like SSH or HTTP) inside DNS queries and responses. This is often used to bypass firewalls, as DNS traffic is almost always allowed out of a network.

  - Information Gathering from Records:
    - ***MX Records:*** Reveal which email service a company uses.
    - ***TXT Records:*** Often contain verification keys for third-party services (like Office 365 or Slack), providing clues about the software in use.
