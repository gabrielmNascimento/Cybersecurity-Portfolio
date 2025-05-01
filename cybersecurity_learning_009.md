Room Title: Networking Concepts
Difficulty: Easy
Time to Complete: 60 minutes
Skills Covered:

    OSI Model
    TCP/IP Model
    IP Addresses
    UDP and TCP
    Encapsulation
    Telnet
    
🏛️ Key Concepts and Lessons Learned
🔹 OSI Model

     The OSI (Open Systems Interconnection) model is a conceptual model developed by the International Organization for Standardization (ISO) that describes how communications should occur in a computer network. 
     In other words, the OSI model defines a framework for computer network communications. Although this model is theoretical, it is vital to learn and understand as it helps grasp networking concepts on a deeper level. 
     The OSI model is composed of seven layers:

    Physical Layer
    Data Link Layer
    Network Layer
    Transport Layer
    Session Layer
    Presentation Layer
    Application Layer

    ![image](https://github.com/user-attachments/assets/45d3c0b7-2a16-4afd-95d5-f9af96d8420c)

🔹 TCP/IP Model

    TCP/IP stands for Transmission Control Protocol/Internet Protocol and was developed in the 1970s by the Department of Defense (DoD). 
    I hear you ask why DoD would create such a model. One of the strengths of this model is that it allows a network to continue to function as parts of it are out of service, for instance, due to a military attack. 
    This capability is possible in part due to the design of the routing protocols to adapt as the network topology changes.

    ![image](https://github.com/user-attachments/assets/6141dcb5-f18e-48cb-b528-4ae70aedf291)


    In our presentation of the ISO OSI model, we went from bottom to top, from layer 1 to layer 7. In this task, let’s look at things from a different perspective, from top to bottom. From top to bottom, we have:

    Application Layer: The OSI model application, presentation and session layers, i.e., layers 5, 6, and 7, are grouped into the application layer in the TCP/IP model.
    Transport Layer: This is layer 4.
    Internet Layer: This is layer 3. The OSI model’s network layer is called the Internet layer in the TCP/IP model.
    Link Layer: This is layer 2.

    
🔹 UDP and TCP

    UDP (User Datagram Protocol) allows us to reach a specific process on this target host. UDP is a simple connectionless protocol that operates at the transport layer, i.e., layer 4. 
    Being connectionless means that it does not need to establish a connection. UDP does not even provide a mechanism to know that the packet has been delivered.

    An IP address identifies the host; we need a mechanism to determine the sending and receiving process. This can be achieved by using port numbers. 
    A port number uses two octets; consequently, it ranges between 1 and 65535; port 0 is reserved. (The number 65535 is calculated by the expression 216 − 1.)

    A real-life example similar to UDP is the standard mail service, with no delivery confirmation. 
    In other words, there is no guarantee that the UDP packet has been received successfully, similar to the case of sending a parcel using standard mail with no confirmation of delivery. 
    In the case of standard mail, it means a cheaper cost than the mail delivery options with confirmation. In the case of UDP, it means better speed than a transport protocol that provides “confirmation.”

    But what if we want a transport protocol that acknowledges received packets? The answer lies in using TCP instead of UDP.

    TCP

    TCP (Transmission Control Protocol) is a connection-oriented transport protocol. It uses various mechanisms to ensure reliable data delivery sent by the different processes on the networked hosts. Like UDP, it is a layer 4 protocol. 
    Being connection-oriented, it requires the establishment of a TCP connection before any data can be sent.

    In TCP, each data octet has a sequence number; this makes it easy for the receiver to identify lost or duplicated packets. 
    The receiver, on the other hand, acknowledges the reception of data with an acknowledgement number specifying the last received octet.

    A TCP connection is established using what’s called a three-way handshake. Two flags are used: SYN (Synchronise) and ACK (Acknowledgment). The packets are sent as follows:

    SYN Packet: The client initiates the connection by sending a SYN packet to the server. This packet contains the client’s randomly chosen initial sequence number.
    SYN-ACK Packet: The server responds to the SYN packet with a SYN-ACK packet, which adds the initial sequence number randomly chosen by the server.
    ACK Packet: The three-way handshake is completed as the client sends an ACK packet to acknowledge the reception of the SYN-ACK packet.

    ![image](https://github.com/user-attachments/assets/19382314-acac-401f-97fa-2b9e664de6bb)


🔹 IP Addresses

    Every host on the network needs a unique identifier for other hosts to communicate with him. Without a unique identifier, the host cannot be found without ambiguity. 
    When using the TCP/IP protocol suite, we need to assign an IP address for each device connected to the network.

    One analogy of an IP address is your home postal address. Your postal address allows you to receive letters and parcels from all over the world. 
    Furthermore, it can identify your home without ambiguity; otherwise, you cannot shop online!

    As you might already know, we have IPv4 and IPv6 (IP version 6). IPv4 is still the most common, and whenever you come across a text mentioning IP without the version, we expect them to mean IPv4.

    So, what makes an IP address? An IP address comprises four octets, i.e., 32 bits. Being 8 bits, an octet allows us to represent a decimal number between 0 and 255. 

🔹 Encapsulation

    Encapsulation refers to the process of every layer adding a header (and sometimes a trailer) to the received unit of data and sending the “encapsulated” unit to the layer below.

    Encapsulation is an essential concept as it allows each layer to focus on its intended function. In the image below, we have the following four steps:

    Application data: It all starts when the user inputs the data they want to send into the application. For example, you write an email or an instant message and hit the send button. 
    The application formats this data and starts sending it according to the application protocol used, using the layer below it, the transport layer.
    Transport protocol segment or datagram: The transport layer, such as TCP or UDP, adds the proper header information and creates the TCP segment (or UDP datagram). This segment is sent to the layer below it, the network layer.
    Network packet: The network layer, i.e. the Internet layer, adds an IP header to the received TCP segment or UDP datagram. Then, this IP packet is sent to the layer below it, the data link layer.
    Data link frame: The Ethernet or WiFi receives the IP packet and adds the proper header and trailer, creating a frame.

    We start with application data. At the transport layer, we add a TCP or UDP header to create a TCP segment or UDP datagram. 
    Again, at the network layer, we add the proper IP header to get an IP packet that can be routed over the Internet. Finally, we add the appropriate header and trailer to get a WiFi or Ethernet frame at the link layer.

  🔹 Telnet

    The TELNET (Teletype Network) protocol is a network protocol for remote terminal connection. In simpler words, telnet, a TELNET client, allows you to connect to and communicate with a remote system and issue text commands. 
    Although initially it was used for remote administration, we can use telnet to connect to any server listening on a TCP port number.

    On the target virtual machine, different services are running. We will experiment with three of them:

    Echo server: This server echoes everything you send it. By default, it listens on port 7.
    Daytime server: This server listens on port 13 by default and replies with the current day and time.
    Web (HTTP) server: This server listens on TCP port 80 by default and serves web pages.


🔍 Reflection

This room helped me to know about how the network works and its main protocols and layers.
