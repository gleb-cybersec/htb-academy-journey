## P2P (Peer-to-Peer) — This is a decentralized network architecture where there is no strict division between a "master server" and "subordinate clients." In such a network, every device (peer) is both a consumer and a provider of resources.

- What is it?
In the classic model (Client-Server), everyone connects to a single central point. In P2P, devices communicate with each other directly. Imagine it as a circle of people sharing books: you don't need to go to a central library; you get the chapter you need from the neighbor on the left, while the neighbor on the right copies a page from you at the same time.

- Types of P2P Networks:
  - **Pure P2P:** Fully decentralized (e.g., the original Gnutella).
  - **Hybrid P2P:** There are "super-nodes" that help peers find each other, but the actual data transfer happens directly between them.
  - **Structured P2P:** Uses Distributed Hash Tables (DHTs) for efficient and deterministic file discovery.

- Why is it important?
  - **Fault Tolerance:** If one of Google's servers goes down, millions of people notice. In a P2P network, even if half of the nodes fail, the system can continue to operate.
  - **Scalability:** The more participants join, the higher the total bandwidth and processing power of the network becomes.
  - **Cost Efficiency:** The service owner doesn't have to pay for powerful data centers—the users themselves provide the resources.
  - **Anonymity and Censorship Resistance:*** A decentralized network is extremely difficult to block or control from a single central point.

- Why is it relevant for pentesting?
For a security specialist, P2P networks are the "Wild West" where standard protection methods often fail.

  - **Malware Distribution:** P2P networks are an ideal transport vector for viruses. A single infected file can quickly spread to thousands of computers, bypassing central filters.
  - **Data Leakage:** Users often accidentally "share" not just a movie folder but their entire hard drive, including passwords and documents. Pentesters look for such "holes" in corporate networks.
  - **Botnets:** Modern hackers use P2P architecture to control armies of infected devices (botnets). Because there is no central "command center," such a network is nearly impossible to shut down.
  - **Index Poisoning / Spoofing Attacks:** A pentester (or attacker) can flood the network with fake data or corrupted file indices, tricking users into downloading malicious software instead of the intended content.
  - **Eclipse Attack:** An attempt to isolate a specific node in a P2P network by surrounding it with attacker-controlled nodes, allowing them to manipulate the data the target node receives (particularly relevant for blockchain networks).


## Client-Server — This is the classic model of network interaction where tasks are distributed between service providers (servers) and service requesters (clients). It is the foundation of the modern internet.

- What is it?
In this model, the roles are clearly divided:
  - **Client:** A device (laptop, smartphone) or program (browser) that initiates a request. The client "wants" to receive data.
  - **Server:** A powerful computer or program that constantly waits for incoming requests. The server "gives" data, processes it, and stores it.
Key Principle: The client always initiates the conversation first, and the server responds. A server can serve thousands of clients simultaneously.

- Why is it important?
  - **Centralization of Data:** All important files and databases are stored in one secure location (on the server), rather than being scattered across all employee devices.
  - **Manageability:** To update a website or database, you only need to update it on the server—all users will see the changes immediately.
  - **Security:** Access to data can be finely controlled through an authentication system on the server side.
  - **Saving Client Resources:** Complex computations (like searching the web with Google or processing a video in the cloud) are done by the server, while your less powerful phone simply displays the result.

- Why is it relevant for pentesting?
The client-server architecture is the main "playground" for attacks. Most hacks are aimed either at tricking the server or at intercepting client data.

- 1.***Server-Side Attacks:***
  - **SQL Injections:** Attempting to send a request to the server that tricks it into revealing its entire database.
  - **DDoS (Distributed Denial of Service):** Attempting to overwhelm the server with so many requests that it can no longer respond to legitimate users.
- 2.***Client-Side Attacks:***
  - **XSS (Cross-Site Scripting):** An attacker injects malicious code onto a server, which is then executed in the browser of an unsuspecting client.
- 3.***Broken Authentication:*** If the server does a poor job of verifying a client's "identity," a pentester can hijack another user's session and access their private account without a password.
  - **Interception of Communication:** Attacking the data in transit between the client and server (e.g., through Man-in-the-Middle attacks) if the connection is not properly encrypted.
- 4.***Separation of Responsibilities:*** Pentesters always check where data validation occurs. If password checks or price verification for an item happen only on the client side (in the browser), they can be easily tampered with before being sent to the server.
