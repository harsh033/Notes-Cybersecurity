## Basic Packet Capture

| Command                | Explanation |
| ---------------------- | ----------- |
| `tcpdump -i INTERFACE` | Capture packets on a specific network interface |
| `tcpdump -w FILE`      | Writes captured packets to a file |
| `tcpdump -r FILE`      | Reads captured packets from a file |
| `tcpdump -c COUNT`     | Captures a specific numbers of packets |
| `tcpdump -n`           | Don't resolve IP address |
| `tcpdump -nn`          | Don't resolve IP address and protocol numbers |
| `tcpdump -v`           | Verbose display; increased with `-vv` and `-vvv` |

`-i any` - listen on all available interface.


## Filtering Expressions
it is impossible to see everything at once; we need to be specific and capture what we are interested in inspecting.

| Command                 | Explanation
| :---------------------: | :-------------------------|
| `tcpdimp host [IP/HOSTNAME]`    | Filters packets by IP address or hostname |
| `tcpdump src host IP`           | Filters packets by a specific source host |
| `tcpdump dst host IP`           | Filters packtes by a specific destination host |
| `tcpdump port PORT_NUMBER`       | Filters packets by port number |
| `tcpdump src port PORT_NUMBER`   | Filters packets by a specified source port number |
| `tcpdump dst port PORT_NUMBER`   | Filters packets by a specified destination port number | 
|`tcpdump PROTOCOL`               | Filters packets by protocol; ex `ip`, `ip6`, `icmp` |

**Logical operators** - we can use `and`, `or`, `not` in the command. eg `tcpdump host 1.1.1.1 and tcp`.

## Advanced Filtering

### Binary operations
Bitwise operators - `&`, `|`, and `!`

### Header Bytes
Tcpdump allows you to refer to the conents to any byte in the header using the syntax: `proto[expr:size]` where
* `proto` refers to protocol. for example, `arp`, `ether`, `ip`, ip6`, `icmp`, `tcp` and `udp`
* `expr` indicates the bytes offset, where `0` refers to the first byte.
* `size` indicates the number of bytes. one is default.


