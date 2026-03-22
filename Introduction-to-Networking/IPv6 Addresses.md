# IPv6 Addresses
length 128 bits. The prefix defines the network and host parts.  follows the end-to-end principle 

- advantages:
    - Larger address space
    - Address self-configuration (SLAAC)
    - Multiple IPv6 addresses per interface
    - Faster routing
    - End-to-end encryption (IPsec)
    - Data packages up to 4 GByte

## Types of IPv6 addresses:

| Type | Description |
|------|-------------|
| Unicast | Addresses for a single interface |
| Anycast | Addresses for multiple interfaces, where only one of them receives the packet |
| Multicast | Addresses for multiple interfaces, where all receive the same packet |

## Hexadecimal System:

| Decimal | Hex | Binary |
|---------|-----|--------|
| 1 | 1 | 0001 |
| 2 | 2 | 0010 |
| 3 | 3 | 0011 |
| 4 | 4 | 0100 |
| 5 | 5 | 0101 |
| 6 | 6 | 0110 |
| 7 | 7 | 0111 |
| 8 | 8 | 1000 |
| 9 | 9 | 1001 |
| 10 | A | 1010 |
| 11 | B | 1011 |
| 12 | C | 1100 |
| 13 | D | 1101 |
| 14 | E | 1110 |
| 15 | F | 1111 |


## In RFC 5952, the IPv6 address notation was defined:
- all letters in lowercase
- leading zeros are omitted
- consecutive blocks of zeros are reduced to :: (only once in the address)