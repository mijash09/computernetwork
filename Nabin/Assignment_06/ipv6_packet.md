## IPV6 packet in WIRESHARK

1. **Source Address: fd00::f:5678:abcd:1e5f:a2b5**

   - **Description**: This is the IPv6 address of the sender. The address is a unique identifier for the source device in the network.

2. **Destination Address: ff02::fb**

   - **Description**: This is the IPv6 address of the receiver. In this case, `ff02::fb` is a multicast address used for mDNS (Multicast DNS) queries, meaning the packet is intended for multiple devices that subscribe to this multicast group.

3. **Version: 6 (indicated by 0110)**

   - **Description**: This field specifies the version of the IP protocol. In this case, the version is 6, indicating an IPv6 packet.

4. **Traffic Class: 0x00 (DSCP: CS0, ECN: Not-ECT)**

   - **Description**: This field is used for Quality of Service (QoS) purposes. The first 6 bits are the Differentiated Services Code Point (DSCP), and the last 2 bits are the Explicit Congestion Notification (ECN). Here, DSCP is set to CS0 (default) and ECN is set to Not-ECT (no ECN support).

5. **Flow Label: 0xbde**

   - **Description**: This 20-bit field is used to identify flows of packets that require special handling by routers, such as packets that belong to the same communication stream. In this case, the flow label is set to `0xbde`.

6. **Payload Length: 51 bytes**

   - **Description**: This field specifies the length of the payload, i.e., the data following the IPv6 header. Here, the payload length is 51 bytes.

7. **Next Header: UDP (17)**

   - **Description**: This field identifies the type of header immediately following the IPv6 header. In this case, the value is 17, which indicates that the next header is a UDP header.

8. **Hop Limit: 1**
   - **Description**: This field specifies the maximum number of hops (i.e., intermediate routers) that the packet can pass through before being discarded. It is similar to the TTL (Time to Live) field in IPv4. Here, the hop limit is set to 1, meaning the packet can only be forwarded by one router.
