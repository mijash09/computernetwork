## 1. How long is IPV6 header?
   :IPV6 header is 40 bytes long consisting 8 fields

## 2. What are different fields on header? What are different purposes?
   The IPv6 header contains several fields, each serving a specific purpose to facilitate the functioning and management of network traffic. Here’s a breakdown of the fields and their purposes:

   1. **Version (4 bits)**

   - **Purpose:** Indicates the IP version number. For IPv6, this value is set to 6.

   2. **Traffic Class (8 bits)**

   - **Purpose:** Used to specify the priority of the packet. It helps in traffic management and quality of service (QoS) by distinguishing different types of data (e.g., voice, video, data).

   3. **Flow Label (20 bits)**

   - **Purpose:** Used for labeling packets belonging to the same flow, allowing routers to handle packets with the same flow label in a consistent manner. This is useful for real-time services requiring consistent handling, like streaming or VoIP.

   4. **Payload Length (16 bits)**

   - **Purpose:** Specifies the length of the payload (the data carried after the header) in bytes. The maximum payload length is 65,535 bytes.

   5. **Next Header (8 bits)**

   - **Purpose:** Identifies the type of header immediately following the IPv6 header. It can indicate an upper-layer protocol (such as TCP or UDP) or an extension header used for optional internet-layer information.

   6. **Hop Limit (8 bits)**

   - **Purpose:** Indicates the maximum number of hops a packet can take before being discarded. Each router that forwards the packet decrements this value by 1. When the value reaches 0, the packet is discarded to prevent it from looping indefinitely.

   7. **Source Address (128 bits)**

   - **Purpose:** Contains the IPv6 address of the originator of the packet. It is used for identifying the sender of the packet.

   8. **Destination Address (128 bits)**

   - **Purpose:** Contains the IPv6 address of the intended recipient of the packet. It is used for routing the packet to its final destination.

Headers present in IPV6 packet in wireshark:

1. Version (4 bits):
   Value: 0110
   Description: This field indicates the version of the Internet Protocol. For IPv6, the value is 6 (0110 in binary).
2. Traffic Class (8 bits):
   Value: 00
   Description: This field is used to identify the class or priority of the IPv6 packet, similar to the Type of Service (ToS) field in IPv4. It's generally used for Quality of Service (QoS) purposes.
3. Flow Label (20 bits):
   Value: 0x56af
   Description: The flow label is used to identify a flow of packets that require special handling by routers. This field is used for purposes like ensuring packets from the same flow are processed in a similar manner.
4. Payload Length (16 bits):
   Value: 107
   Description: This field specifies the length of the payload, i.e., the data following the IPv6 header, in bytes. In this case, the payload length is 107 bytes.
5. Next Header (8 bits):
   Value: 17
   Description: This field identifies the type of header immediately following the IPv6 header. The value 17 corresponds to the User Datagram Protocol (UDP).
6. Hop Limit (8 bits):
   Value: 255
   Description: This field is similar to the Time-to-Live (TTL) field in IPv4. It specifies the maximum number of hops (routers) the packet can pass through. Each router that forwards the packet decreases the hop limit by one. If the hop limit reaches zero, the packet is discarded. In this packet, the hop limit is set to 255.
7. Source Address (128 bits):
   Value: fe80::a4be:e675:39a2:3632
   Description: This field contains the IPv6 address of the sender. The address fe80::/10 is a link-local address, which means it is used for communication within the local network segment.
8. Destination Address (128 bits):
   Value: ff02::fb
   Description: This field contains the IPv6 address of the intended recipient. The address ff02::fb is a multicast address used for MDNS (Multicast DNS), which is used to resolve hostnames to IP addresses within the same local network.
