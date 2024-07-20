## TCP header caught in WIRESHARK

1. **Source Port: 51004**
   - This is the port number on the sender's side. It identifies the application or process sending the data. Ports range from 0 to 65535, and ports above 1023 are often dynamically assigned.

2. **Destination Port: 443**
   - This is the port number on the receiver's side. Port 443 is commonly used for HTTPS traffic, which means the data is likely being sent to a web server over a secure connection.

3. **Sequence Number: 1**
   - This number indicates the position of the first byte of data in this segment within the overall data stream. The sequence number is crucial for reassembling the data in the correct order on the receiving side.

4. **Acknowledgment Number: 1**
   - This field is used when the ACK flag is set. It indicates the next byte that the sender of this segment expects to receive. In this case, the sender is acknowledging that it has received all bytes up to and including byte 0, and is now expecting byte 1.

5. **Header Length: 20 bytes (5 words)**
   - This field specifies the length of the TCP header in 32-bit words. Since each word is 4 bytes, a header length of 5 words means the header is 20 bytes long. This field is necessary because the TCP header can vary in size due to optional fields.

6. **Flags: ACK (Acknowledgment)**
   - The flags field contains 9 control bits. The ACK flag, when set, indicates that the acknowledgment number is valid. Other common flags include SYN (synchronize), FIN (finish), RST (reset), PSH (push), URG (urgent), and others.

7. **Window Size: 513**
   - This field specifies the size of the sender's receive window (the amount of data the sender is willing to accept). It is used for flow control, helping to prevent the receiver from being overwhelmed by too much data too quickly.

8. **Checksum: 0xc2c7 (unverified)**
   - The checksum field is used for error-checking the header and data. It is calculated by the sender and verified by the receiver to ensure data integrity.

9. **Urgent Pointer: 0**
   - The urgent pointer is only significant if the URG flag is set. It points to the sequence number of the byte following urgent data. In this case, the value is 0, indicating no urgent data is present.

10. **TCP Payload: 1 byte**
    - This is the actual data being carried by the TCP segment. In this example, the payload is just 1 byte long. The payload can vary in size, but it is typically larger than 1 byte.

The TCP header provides all the necessary information to manage the transmission of data between sender and receiver, ensuring reliable and ordered delivery, error checking, and flow control.