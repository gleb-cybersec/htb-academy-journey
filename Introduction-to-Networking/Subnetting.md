# Subnetting
splitting an IPv4 address range into multiple smaller ranges. which uses IP addresses with the same network address

- parameters:
    - **Network address**
    - **Broadcast address**
    - **First host**
    - **Last host**
    - **Number of hosts**

## Mental Subnetting
- To determine the subnet size, take the remainder of dividing the mask by 8 (the Modulo operation, %). For /25: 25 % 8 = 1

    | Remainder | Number | Exponential Form |
    |-----------|--------|------------------|
    | 0 | 256 | 2^8 |
    | 1 | 128 | 2^7 |
    | 2 | 64 | 2^6 |
    | 3 | 32 | 2^5 |
    | 4 | 16 | 2^4 |
    | 5 | 8 | 2^3 |
    | 6 | 4 | 2^2 |
    | 7 | 2 | 2^1 |

    | 1st Octet | 2nd Octet | 3rd Octet | 4th Octet |
    |-----------|-----------|-----------|-----------|
    | /8 | /16 | /24 | /32 |


    ## Additional tasks for skill development
    - Submit the decimal representation of the subnet mask from the following CIDR: 192.168.10.0/27
        - answer: 255.255.255.254
    - Submit the decimal representation of the subnet mask from the following CIDR: 10.0.0.0/22
        - answer: 255.255.252.0
    - Submit the decimal representation of the subnet mask from the following CIDR: 172.16.5.0/19
        - answer: 255.255.224.0
    - Submit the decimal representation of the subnet mask from the following CIDR: 192.168.1.0/30
        - answer: 255.255.255.252
    - Submit the decimal representation of the subnet mask from the following CIDR: 10.15.0.0/25
        - answer: 255.255.255.128

    - Submit the broadcast address of the following CIDR: 192.168.10.0/27
        - answer: 192.168.10.31
    - Submit the broadcast address of the following CIDR: 10.0.0.0/24
        - answer: 10.0.0.255
    - Submit the broadcast address of the following CIDR: 172.16.5.0/26
        - answer: 172.16.5.63
    - Submit the broadcast address of the following CIDR: 192.168.1.128/25
        - answer: 192.168.1.255
    - Submit the broadcast address of the following CIDR: 10.15.0.0/22
        - answer: 10.15.3.255
    -Submit the broadcast address of the following CIDR: 172.31.0.0/23
        - answer: 172.31.1.255

    - Submit the network address of the following IP and CIDR: 192.168.10.34/27
        - answer: 192.168.10.32
    - Submit the network address of the following IP and CIDR: 10.0.15.8/22
        - answer: 10.0.12.0
    - Submit the network address of the following IP and CIDR: 172.16.5.130/26
        - answer: 172.16.5.128
    - Submit the network address of the following IP and CIDR: 192.168.1.200/25
        - answer: 192.168.1.128
    - Submit the network address of the following IP and CIDR: 10.15.3.5/23
        - answer: 10.15.2.0
    
    - Submit the first usable host of the following CIDR: 192.168.10.0/27
        - answer: 192.168.10.1
    - Submit the last usable host of the following CIDR: 10.0.0.0/24
        - answer: 10.0.0.254
    - Submit the first usable host of the following CIDR: 172.16.5.0/26
        - answer: 172.16.5.1
    - Submit the last usable host of the following CIDR: 192.168.1.128/25
        - answer: 192.168.1.254
    - Submit the first usable host of the following CIDR: 10.15.0.0/23
        - answer: 10.15.0.1
    - Submit the last usable host of the following CIDR: 172.31.0.0/23
        - answer: 172.31.1.254

    - Split the network 192.168.10.0/24 into 4 subnets and submit the broadcast address of the 3rd subnet
        - answer: 192.168.10.191
    - Split the network 172.16.0.0/24 into 8 subnets and submit the network address of the 5th subnet.
        - answer: 192.168.10.191
    - Split the network 10.0.0.0/24 into 4 subnets and submit the network address of the 2nd subnet.
        - answer: 10.0.0.64
    - Split the network 192.168.1.0/25 into 4 subnets and submit the broadcast address of the 4th subnet.
        - answer: 192.168.1.127
    - Split the network 172.20.10.0/24 into 16 subnets and submit the network address of the 12th subnet.
        - answer: 172.20.10.176