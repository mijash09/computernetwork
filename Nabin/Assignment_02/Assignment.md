1. Differentiate between client-server network and peer to peer network.

| Feature             | Client-Server Network                                                                | Peer-to-Peer Network                                                            |
| ------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| **Structure**       | Centralized: Server provides services to clients.                                    | Decentralized: All nodes have equal status.                                     |
| **Management**      | Centralized administration. Server manages resources.                                | Distributed management. Each node manages itself.                               |
| **Security**        | Higher security due to centralized control.                                          | Lower security, as each node manages its own security.                          |
| **Performance**     | Scalable by upgrading the server; potential bottlenecks if the server is overloaded. | More robust as load is distributed; performance can degrade as more nodes join. |
| **Examples**        | Websites, email servers, corporate networks.                                         | File sharing networks, blockchain, Skype.                                       |
| **Cost**            | Higher cost due to server infrastructure and maintenance.                            | Lower cost, as there is no need for dedicated servers.                          |
| **Reliability**     | High reliability if the server is maintained properly.                               | Can be less reliable due to dependence on individual nodes.                     |
| **Data Management** | Centralized data storage. Easier to back up and restore.                             | Data is distributed across nodes. More complex data management.                 |
     



2. What are the seven layers of OSI model?What is the function of each layer?

Open Systems Interconnection model is a conceptual framework used to understand and implement standardized communication between diverse systems.It divides communication process into seven distinct layers,each with specific functions.The seven layers of OSI model are as follows:

1. Physical Layer: This layer deals with physical connection between devices which means they are responsible for the transmission and reception of raw bitstreams over a physical medium. Eg:cables,switches.
   Its key functions are: bit by bit data transmission,signal encoding and decoding.

2. Data Link Layer: This layer provides node to node data transfer ie a link between two directly connected nodes.The data link layer divides the stream of bits received from the network layer into manageable data units called frames. MAC (Media Access Control) addressing is used to identify devices within a local network segment.
3. Network Layer: The network layer is responsible for the source-to-destination delivery of a packet,possibly across multiple networks (links).Also its key function is logical addressing,packet forwarding and internetworking.
4. Transport Layer: This ensures complete data transfer and reliability,manages end-to-end communication between devices and provides error checking and data flow control.

5. Session Layer: The Session layer establishes, maintains, and synchronizes the interaction among communicating systems. The session layer allows a process to add checkpoints,synchronization points, to a stream of data.

6. Presentation Layer:This layer translates data between the application layer and network format,ensures that data is in a usable format and is correctly encrypted/decrypted if necessary and handles data compression and decompression.

7. Application Layer: It provides user interfaces and support for services such as electronic mail, remote file access and transfer, shared database management, and other types of distributed information services.

3.What are the principals behind OSI model?

The OSI model is based on the following principle :

1. A layer should be created where a different abstraction is needed.
2. Each layer should perform a well-defined function.
3. The function of each layer should be chosen with an eye toward defining internationally standardized protocols.
4. The layer boundaries should be chosen to minimize the information flow across the interfaces.
5. The number of layers should be large enough that distinct functions need not be thrown together in the same layer out of necessity and small enough that the architecture does not become unwieldy.

4.Differentiate between OSI reference model and TCP/IP reference model.

| Feature                    | OSI Reference Model                                                         | TCP/IP Reference Model                                    |
| -------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------- |
| **Full Name**              | Open Systems Interconnection Model                                          | Transmission Control Protocol/Internet Protocol Model     |
| **Layers**                 | 7 layers                                                                    | 4 layers                                                  |
| **Layer Names**            | Application, Presentation, Session, Transport, Network, Data Link, Physical | Application, Transport, Internet, Network Interface       |
| **Protocol Specification** | General model, not specifying protocols in each layer                       | Specifies standard protocols in each layer                |
| **Abstraction Level**      | High-level abstraction; more theoretical                                    | Practical implementation; more straightforward            |
| **Reliance**               | Does not rely on a specific protocol suite                                  | Built around the TCP/IP protocol suite                    |
| **Layer Functionality**    | Each layer has a distinct function                                          | Some layers combine multiple functions                    |
| **Flexibility**            | More flexible; can work with various network protocols                      | Specifically designed for the TCP/IP suite                |
| **Standardization**        | ISO standards, widely used as a reference model                             | De facto standard for internet and network communications |
| **Error Handling**         | Detailed error handling in multiple layers                                  | Error handling mainly in the Transport layer              |
| **Ease of Implementation** | More complex to implement due to seven distinct layers                      | Easier to implement due to fewer layers                   |
| **Examples of Protocols**  | Protocols like HTTP, FTP (Application); IP (Network)                        | HTTP (Application); TCP, UDP (Transport); IP (Internet)   |

