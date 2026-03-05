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



## Hybrid Architecture — This is a network model that combines features of both the client-server architecture and P2P. In it, central servers are used for management, search, or authentication, while the main data transfer or computations happen directly between nodes (clients).

- What is it?
In a hybrid scheme, there is a "main headquarters" (the server) and "field agents" (the nodes).
  1. ***The Server Part:*** Stores a directory of resources, file indexes, or information about who is currently online.
  2. ***The P2P Part:*** Once one node finds another via the server, they begin exchanging data directly, without burdening the central server.

- Why is it important?
  - **Best of Both Worlds:** The speed and order provided by servers, combined with the scalability and bandwidth savings of P2P.
  - **Reduced Load:** Companies don't need to download terabytes of updates to every single user from their own servers; users help each other by downloading pieces of files from their peers.
  - **Fast Discovery:** Unlike pure P2P networks, where searching for a file can take a long time, here the server instantly tells you which peer has the resource you need.

- Why is it relevant for pentesting?
Hybrid systems are complex targets because they expand the "attack surface." A pentester looks for weaknesses in both components:
  1. ***Attacking "Supernodes":*** In some hybrid networks, powerful user computers act as temporary mini-servers or indexes. If such a supernode is compromised, an attacker can control or monitor the traffic of hundreds of other participants.
  2. ***Index Manipulation:*** If a pentester can tamper with the data on the central server (e.g., through a web application vulnerability), they could trick thousands of clients into connecting to a malicious peer for "updates," spreading malware.
  3. ***Bypassing Corporate Policies:*** Hybrid applications (like Skype or Spotify in their early days) often use unconventional methods to traverse firewalls, potentially creating unintended holes in the network perimeter's security.
  4. ***Analysis of Signaling Traffic:*** By studying how a client communicates with the central server before switching to direct P2P mode, an attacker might intercept IP addresses and metadata of network participants that are otherwise hidden behind NAT.



## Cloud Architecture — This is a model for delivering IT resources (servers, storage, databases, networks, and software) over the internet on demand. Instead of owning physical hardware, companies rent virtual capacities from providers like AWS, Azure, or Google Cloud.

- What is it?
The cloud consists of massive data centers whose resources are programmatically divided among thousands of users.

  - Main Service Models:
    - ***IaaS (Infrastructure as a Service):*** Renting "bare" computing, storage, and networking resources (e.g., AWS EC2). You are responsible for installing and managing the operating system and software.
    - ***PaaS (Platform as a Service):*** A ready-made environment for developers (e.g., Google App Engine, Heroku). You just write and deploy your code; the cloud provider manages the underlying infrastructure.
    - ***SaaS (Software as a Service):*** Ready-to-use applications accessible via a browser (e.g., Google Drive, Microsoft 365, Salesforce).

- Why is it important?
  - **Scalability:** If a website experiences a sudden surge in traffic, the cloud can automatically allocate additional resources to handle the load.
  - **Cost Efficiency (Pay-as-you-go):** You only pay for the computing time, storage, and bandwidth you actually consume.
  - **Accessibility:** Data and applications are accessible from anywhere in the world with an internet connection.
  - **Deployment Speed:** A new virtual server can be created in the cloud in seconds or minutes, compared to the weeks it might take to procure and set up physical hardware.

- Why is it relevant for pentesting?
Cloud computing has changed the rules of engagement for security testing. Pentesters now need to look not only for flaws in the application code but also for misconfigurations in the cloud environment itself.

  - **Misconfigurations:** This is the most common cause of cloud data breaches. For example, an S3 storage bucket (AWS) containing sensitive customer data is accidentally left open to the public internet.
  - **Identity and Access Management (IAM):** In the cloud, permissions and access rights define the new security perimeter. If a pentester steals an API key belonging to a developer that has excessive privileges, they could gain control over the company's entire cloud infrastructure.
  - **Shared Responsibility Model:** The cloud provider is responsible for the security of the cloud (physical hardware, data centers). The customer is responsible for security in the cloud (their data, configurations, user access). Attackers focus on the customer's side of this model.
  - **Serverless Attacks:** Attacking serverless functions (e.g., AWS Lambda). While there is no traditional server to exploit, attackers can manipulate the function's logic by injecting malicious input data.
  - **Container Escape:** Attempting to break out of a virtual machine or container (like Docker or Kubernetes) to gain access to the host hypervisor or other customers' environments.


## Software-Defined Networking (SDN) — This is a modern approach to computer networking that separates the network's "brains" (the control plane) from its "muscles" (the data plane).
In a traditional network, each router or switch makes its own decisions about where to forward packets. In SDN, a central controller is responsible for this, and the network devices simply execute its commands.

- What is it?
SDN divides the architecture into three layers:
  - **Infrastructure Layer (Data Plane):** The physical or virtual switches that simply forward traffic according to the rules they receive.
  - **Control Layer (Control Plane):** The "brain" – a software-based controller that has a holistic view of the entire network.
  - **Application Layer:** Programs that manage and manipulate the network, such as load balancers, firewalls, and network monitoring tools.

- Why is it important?
  - ***Flexibility:*** An administrator can change the topology of the entire network with a single software command, without needing to physically re-cable servers.
  - ***Automation:*** The network can automatically scale up or down based on current load, similar to cloud computing principles.
  - ***Centralization:*** Security policies and configurations can be applied to thousands of devices from a single, centralized management interface.
  - ***Reduced Costs:*** It allows for the use of simpler, cheaper "white box" switches because the complex logic resides in the centralized software controller.
