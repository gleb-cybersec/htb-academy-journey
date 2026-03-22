# MAC Addresses
physical address of our network interfaces(6 bytes)
## Standards for the MAC address:
    - Ethernet (IEEE 802.3)
    - Bluetooth (IEEE 802.15)
    - WLAN (IEEE 802.11)

## Organization Unique Identifier (OUI) 
first 3 bytes

## Individual Address Part or Network Interface Controller (NIC)
the remaining 3 bytes (assigned once by the organization)

## Unicast (the last bit **0**)
the packet will only reach one specific host.
## Multicast (the last bit **1**)
the packet is sent once to all hosts on the local network, which then decide whether to accept it or not.

## Global (the penultimate bit **0**)
globally defined
## Local (the penultimate bit **1**)
locally administered

## MAC Address Attack Vectors:
    - **MAC spoofing** - address substitution for unauthorized access
    - **MAC flooding** - sending a large number of packets with addresses to a switch to overflow the address table and disrupt the operation of the switch
    - **MAC address filtering** - bypassing restrictions by replacing them with an authorized MAC address


## Address Resolution Protocol (ARP)
converts IP address (layer 3) to MAC address (layer 2)
    
    - Two types of request messages:
        - **ARP Request** - sends a request to everyone with the IP address of the device to obtain the MAC address of the required device
        - **ARP Reply** - the device sends a MAC address in response
