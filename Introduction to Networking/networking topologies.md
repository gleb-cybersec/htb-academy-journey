# Networking Topologies
diagram of the location and connection of devices in the network

## Connections
they are divided into wired (twisted pair, fiber optic cables) and wireless (Wi-Fi)

## Network nodes
these are the connection points of the transmission medium to the transmitters and receivers of electrical, optical or radio signals in that medium

## Classifications
- **Point-to-Point** physical connection between two hosts (telephony)
- **Bus** connected via the same transmission medium. At a time, only one can transmit information, and all the others can only receive
- **Star** All devices are connected to a network component (router, hub, switch). The network component performs the function of forwarding data
- **Ring** each connected by two cables (1. reception, 2. transmission). The logical topology is based on a physical star (the distributor forwards from one port to the next). Transmission from station to station is accomplished using a ***token*** (a bit pattern that travels in one direction).
- **Mesh** decision about connections at the physical level and about routing at the logical level.
  - ***fully meshed structure*** every host is connected to every other host on the network
  - ***partially meshed structure*** the endpoints are connected by only one connection
- **Tree** extended star for larger networks. there is both logical(spanning tree) and physical
- **Hybrid** combines several topologies, as a result it does not represent any of the standard ones
- **Daisy Chain** connected by a cable from one to the other (based on the physical arrangement of nodes)
