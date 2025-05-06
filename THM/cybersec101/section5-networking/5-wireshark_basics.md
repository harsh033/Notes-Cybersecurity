## Tool Overview

### Use Cases
wireshark is the most potent(powerful) traffic analyser tool available in the wild.
* Detecting and troubleshooting network problems.
* Detecting security anomalies, such as rogue hosts, abnormal port usage, and suspicious traffic.
* Investigating and learning protocol details, such as response codes and payload data.

### GUI and data
* Toolbar
* Display Filter Bar
* Recent Files
* Capture Filter and Interfaces
* Status Bar

### Packet Details
Packet details are shown in three different panes, which allow us to discover them in different fomats

* **Packet List Pane** - Summary of each packet. (src IP, dst IP, protocol etc)
* **Packet Details Pane** - Detailed protocol breakdown of the selected packet.
* **Packet Bytes Pane** - Hex and decoded ASCII representation of the selected packet.

### Colouring Packets
`View --> Coloring Rules` for find the rules.

### Traffic Sniffing
You can use the blue "shark button" to start network sniffing (capturing traffic), the red button will stop the sniffing, and the green button will restart the sniffing process

### Merge PCAP files
`File --> Merge` - combine two pcap files into one single file.

### View file details
 You can view the details by following "Statistics --> Capture File Properties" or by clicking the "pcap icon located on the left bottom" of the window.

## Packet Dissection
Packet dissection is also known as protocol dissection, which investigaes packet details by decoding available protocols and fields. Wireshark supports a long list of protocols for dissection, and you can also write your dissection scripts.

### Packet Details
We can see seven distinct layer to the packet
* The Frame (Layer 1)
* Source mac (Layer 2)
* Source IP (Layer 3)
* Protocol (Layer 4)
* Application Protocol (Layer 5)

## Packet Navigation

### Go to Packet
`Go --> Go to Packet` then submit the packet number for directly navigate with packet number.

### Find Packets
Wireshark can find packets by packet content. we can use the `Edit --> Find Packet` menu to make a search inside the packets.

This functionality accepts four types of input (Display filter, Hex, String, and Regex)

### Mark Packets
You can find/point to a specific packet for further investigation by marking it.

### Packet comment
Similar to packet marking, commenting is another helpful feature for analysts.

### Export Packets
This functionality helps analysts share the only suspicious packages (decided scope) by `file --> Export specified packets`.

### Export Objects (files)
Exporting objects are available only for selected protocol's streams (DICOM, HTTP, IMF, SMB and TFTP).

### Time Display format
we can change the time format (for better view we can use the UTC format)

### Expert info
Wireshark also detects specific states of protocols to help analysts easily spot possible anomalies and problems. 

| Severity | Color  | Info                                                    |
| -------- | ------ | ------------------------------------------------------- |
| chat     | Blue   | Information on usual workflow                           |
| note     | cyan   | Notable events like application error codes             |
| Warn     | yellow | Warnings like unusual error codes or problen statements |
| Error    | red    | Protocols like malformed packets                        |

## Packet Filtering
filtering help analysts to narrow down the traffic and focus on the event of interest. wireshark has two types of filtering approaches: **capture filter and display filter**.

### Apply as Filter
you can click on the field you want to filter and use the "right-click menu" or "Analyse --> Apply as Filter" menu to filter the specific value.

### Conversation filter
suppose you want to investigate a specific packet number and all linked packets by focusing on IP addresses and port numbers. In that case, the "Conversation Filter" option helps you view only the related packets and hide the rest of the packets easily.

### Colourise Conversation
This option is similar to the "Conversation Filter" with one difference. It highlights the linked packets without applying a display filter and decreasing the number of viewed packets.

### Apply as column
we can select the packet details pane and apply as column to add columns to the packet list pane.

### Follow Stream
Wireshark displays everything in packet portion size. However, it is possible to reconstruct the streams and view the raw traffic as it is presented at the application level.

Once you follow a stream, Wireshark automatically creates and applies the required filter to view the specific stream.


