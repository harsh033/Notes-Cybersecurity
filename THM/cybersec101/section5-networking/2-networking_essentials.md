## DHCP
DHCP is application level protocol that assigns IP addresses and other network  configurations to devices.

DHCP follows four steps: discover, Offer, Request, Acknowledge (DORA)

1. DHCP discover: The client broadcast a DHCPDISCOVER message seeking the local DHCP server if one exists.

2. DHCP Offer: The server responds with a DHCPOFFER message with an IP address available for the client  to accept.

3. DHCP Request: The client responds with a DHCPREQUEST message to indicate that it has accepted the offered IP.

4. DHCP Acknowledge: The server responds with a DHCPACK message to confirm that the offered IP address is now assigned to this client.

we expect that the DHCP server has provided us with the following:
    * The leased IP address to access network resources.
    * The gateway to route our packets outside the local network.
    * A DNS server to resolve domain names.

## ARP: Bridging Layer 3 addressing to Layer 2 addressing
Address Resolution Protocol (ARP) makes it possible to find the MAC address of another device on the Ethernet. demonstration with tshark:
```
user@ubuntu$ tshark -r arp.pcapng -Nn
    1 0.000000000 cc:5e:f8:02:21:a7 → ff:ff:ff:ff:ff:ff ARP 42 Who has 192.168.66.1? Tell 192.168.66.89
    2 0.003566632 44:df:65:d8:fe:6c → cc:5e:f8:02:21:a7 ARP 42 192.168.66.1 is at 44:df:65:d8:fe:6c
```

## ICMP: Troubleshooting Networks
Internet Control Message Protocol is maily used for network diagnostics and error reporting. Two popular ICMP commands are:
    * ping - This command uses ICMP to test connectivity to a target system and measures  the round-trip time (RTT). (ICMP type 8 and ICMP type 0)
    * traceroute - It uses ICMP to discover the route from your host to the target. it utilise the Internet protocol header field called Time-to-Live (TTL). (ICMP type 11)

## NAT
The idea behind NAT (Network Address Translation) lies in using one public IP address to provide Internet access to many private IP addresses.
