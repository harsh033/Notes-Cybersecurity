> Nmap is a open-source tool used for network discovery. It also asssists in the exploration of network hosts and services, providing information obout open ports, operating systems, and other details.

different approaches that nmap uses to discover live host
1. ARP scan
2. ICMP scan
3. TCP/UDP ping scan

## Enumerating target
we can provide:-
* list (`example1.com example2.com`)
* range ( `10.11.12.15-20` ) 
* subnet (` IP/30`)
* host file ( `nmap -iL list_of_hosts.txt`)

`nmap -sL TARGET` - returns the list of hosts that nmap will scan 

Nmap will attempt a reverse-DNS resolution on all targets if IP range provided (we can use `-n` to override it)

## Discovering Live hosts
we will leverage the protocols to discover the live hosts.
* ARP from link layer
* ICMP from network layer
* TCP form transport layer
* UDP from transport layer

## Nmap host discovery using ARP
Nmap follows the following approaches to discover live hosts:
* When privileged (sudo) user tries to scan target on local network, Nmap uses ARP request.
* When a privileged user tries to scan target outside the local network, Nmap uses ICMP echo requests, TCP ACK to port 80, TCP SYN to port 443, and ICMP timestamp request.
* When an unprivileged user tries to scan target outside the local network, Nmap resorts the TCP 3-way handshake by sending SYN packets to port 80 and 443.

`nmap -sn TARGETS` - to discover hosts without port-scanning the live systems.

`sudo nmap -PR -sn TARGETS` - to perform ARP scan without port-scanning.

## Nmap host discovery using ICMP 
although `ping (ICMP Type 8/echo)` would be the most straight forward approach for finding live host but it is not always reliable. many firewalls block ICMP echo.

`sudo nmap -PE -sn TARGET` - sending ICMP echo packets to the target for finding live host without port-scanning.

`sudo nmap -PP -sn TARGET` - sending ICMP timestamp request (`-PP`)

`sudo nmap -PM -sn TARGET` - Nmap uses address mask queries (ICMP Type 17) and checks whether it gets an address mask reply (ICMP Type 18).

## Nmap host discovering using TCP and UDP 

### TCP SYN Ping - send packet with a syn flag set to a tcp port, 80 by default and wait for the response. An open port should reply with a SYN/ACK, a closed port would result in an RST. any response infer that the host is up. 

`nmap -PS80,443,8080 -sn TARGET`

### TCP ACK Ping - You must be running Nmap as a privileged user to be able to accomplish this. It send the packet with ACK flag set. target respond with the RST flag set because the TCP packet with the ACK flag is not part of any ongoing connection.

`sudo nmap -PA80,443,8080 -sn TARGET`

### UDP Ping - If we send a UDP packet to a closed UDP port, we expect to get an ICMP port unreachable packet; this indicates that the system is up and available.

`nmap -PU -sn TARGET` 

note: we can use `-R`:(reverse DNS lookup for all host) for query the DNS server even for offline hosts.
