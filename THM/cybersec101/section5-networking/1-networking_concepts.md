## OSI Model

The OSI (Open Systems Interconnection) model is a conceptual model developed by the International Organization for Standardization (ISO) that describes how communications should occur in a computer network.

1. Physical Layer  
    * Main function - Physical data transmission media
    * Examples - Electrical, optical, and wireless signals.

2. Data Link Layer
    * Main function - Reliable data transfer between adjacent nodes.
    * Examples - Ethernet (802.3), WiFi (802.11).

3. Network Layer
    * Main function - Logical addressing and routing between networks.
    * Examples - IP, ICMP, IPSec

4. Transport Layer
    * Main function - End-to-end communication and data segmentation between running application.
    * Examples - UDP, TCP

5. Session Layer
    * Main funciton - Establishing, maintaining, and synchronising sessions between application running on different host.
    * Examples - NFS, RPC

6. Presentation Layer 
    * Main funciton - data encoding, encryption, and compression.
    * Examples - Unicode, MIME, JPEG, PNG

7. Application Layer
    * Main function - Providing services and interfaces to application.
    * Examples - HTTP, FTP, DNS, POP3, SMTP

## TCP/IP Model
We have covered conceptual ISO OSI model,  it is time to study an implemented model developed by DoD in 1970.

* Application layer - layer 5,6 and 7 of OSI are grouped into the application layer in TCP/IP

* Transport Layer - Layer 4 of OSI

* Internet Layer - Layer 3 (network layer) in OSI.

* Link Layer - Layer 2

## IP Addresses and Subnets

* IP addresses is a unique identifier for the host. two versions IPv4 and IPv6.

* in special case 0 is reserved for for network address and 255 is reserved for broadcast address.

private IP range
    * 10.0.0.0 to 10.255.255.255
    * 172.16.0.0 to 172.31.255.255
    * 192.168.0.0 to 192.168.255.255

Routing
* A router forwards packet to the proper network. it functions at layer 3, inspecting the IP address and forwarding the packet to the best network(router).

## UDP and TCP

### UDP
* connectionless protocol opetates at layer 4
* Not ACK mechanism for data deliver ensurity

### TCP
* connection-oriented protocol
* ensures reliable data delivery
* use 3 way handshake for establish the connection

### Encapsulation
encapsulation refers to the process of every layer adding a header (and sometimes a trailer) to the received unit of data and sending the “encapsulated” unit to the layer below.
    * Application data
    * TCP segment or UDP datagram
    * Network packet
    * data link frame
the process has to be reversed on the receiving end until the application data is extracted.

## Telnet

allows you to connect to and communicate with a remote system and issue text commands. it is insecure because it sends the username and passwords in plaintext.

