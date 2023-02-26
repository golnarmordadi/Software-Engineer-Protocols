# Protocols Web

#### What is Hypertext?
Hypertext is text which contains links to other texts.

---

#### What is Hypermedia? 
Hypermedia is a term used for hypertext which is not constrained to be text, it can include graphics, video and sound, for example.

---

#### What is a Protocols? 
Protocols are vendor specification which means private companies offer them on their software and operating systems. They are part of operations of a system that would implement on them.

---

#### Internet Protocols:
TCP/IP Suit, HTTP, HTTPS, SMTP, FTP, UDP (User Datagram Protocol), Telnet, Gopher, PPTP (Point To Point Tunnelling Protocol), SCTP, RPC (Remote Procedure Calls in distributed systems), gRPC (gRPC remote procedure calls), TLS (Transport Layer Security)

---

#### TCP/IP Suite: 
TCP/IP is connecting protocol. TCP is a communication protocol which is used for communicating over a network. It divides any messages into series of packages that are sent from source to destination and there is get assembled at the destination. IP is designed as addressing protocol. IP helps in routing the packets through different nodes in a network until it reaches the destination. TCP is used by HTTP, HTTPs, FTP, SMTP and Telnet. TCP doesn’t support Broadcasting. Transmission Layer.

---

#### HTTP: 
HTTP is a application layer protocol built upon the TCP. Designed for transferring a hypertext among two or more systems. HTTP is designed on client-server principles which allows a client system for establishing a connection with the server machine for making a request. The server acknowledges the request initiated by the client and response accordingly. Application Layer. Without Message encryption.

---

#### HTTPS: 
It is secure HTTP. Is designed to create secure communication among two computer, one using the browser and other fetching data from web server. HTTPS expect transferring of is done in an encrypted format. So we can say HTTPS thwart hackers from interpretation or modification of data throughout the transfer of packets. Encrypt messages. HTTP is stateless but not sessionless, usually HTTP cookies allow the use of stateful sessions. Using header extensibility, HTTP Cookies are added to the workflow, allowing session creation on each HTTP request to share the same context, or the same state.

---

#### RPC: 
RPC is a powerful technique for constructing distributed, client-server based applications. RPC is an interprocess communication technique. The Full form of RPC is Remote Procedure Call. It is used for client-server applications. RPC mechanisms are used when a computer program causes a procedure or subroutine to execute in a different address space, which is coded as a normal procedure call without the programmer specifically coding the details for the remote interaction.

---

#### Services which are using RPC protocol:
* XML-RPC 
* JSON-RPC
* Google Toolkit
* Google Protocol Buffers Buffers
* Microsoft .NET Remoting 
* Microsoft DCOM
* Open Software Foundation
* Directory Service Remote Procedure Call ( DS-RPC)

---

#### gRPC: 
gRPC is a modern, open source, high-performance remote procedure call (RPC) framework that can run anywhere. gRPC enables client and server applications to communicate transparently, and simplifies the building of connected systems. gRPC uses Protocol Buffers to encode data. Contrary to Rest APIs with Json, they have a more strict specification. Due to having a single specification, gRPC eliminates debate and saves developer time because gRPC is consistent across platforms and implementations.

---

#### TSL: 
Formerly known as Secure Socket Layer (SSL). It used by application to communicate securely accross a network preventing tampering with and eavesdropping on email, web browsing, messaging and other protocols. Both SSL and TSL are client-server protocol and provide security over a network. All modern browsers support the TSL protocol, requiring the server to provide a valid digital certificate confirming its identity in order to establish a secure connection. It is possible for both the client and server to mutually authenticate each other, if both parties provide their own individual digital certificates.

---

#### SCTP: 
SCTP stands for Stream Control Transmission Protocol. It is a connection-oriented protocol on computer networks that provides a full-duplex association, i.e., transmitting multiple streams of data between two endpoints at the same time that have established a connection in the network. It is sometimes referred to as next-generation TCP or TCPng. SCTP makes it easier to support telephonic conversation on the Internet. A telephonic conversation requires the transmitting of the voice along with other data at the same time on both ends. The SCTP protocol makes it easier to establish a reliable connection.SCTP is also intended to make it easier to establish connections over the wireless networks and managing the transmission of multimedia data. SCTP is a standard protocol (RFC 2960) and is developed by the Internet Engineering Task Force (IETF).

---

#### SMTP: 
Is designed to send and distribute outgoing E-Mail.

---

#### FTP: 
Allows users to send files from one machine to another. Types of files may include program files, multimedia files, text files and documents, etc.

---

#### UDP: 
UDP is an alternative to Transmission Control Protocol. UDP is connectionless protocol but TCP is connection-oriented protocol, which means UDP doesn't provide any guarantees that the data will be delivered or offer special features to retransmit lost or corrupted messages. It allows packets to be dropped and received in a different order than they were transmitted, making it suitable for real-time applications where latency might be a concern. It can be used where a large number of clients are connected and where real-time error correction isn't necessary, such as gaming, voice or video conferencing, and streaming media. Unlike TCP, UDP doesn't guarantee the packets will get to the right destinations. This means UDP doesn't connect to the receiving computer directly, which TCP does. For example, an application that is configured to manage the process of retransmitting lost packets and correctly arrange received packets might use UDP. This approach can help to improve the data transfer rate of large files compared to TCP. UDP is used by DNS, DHCP, TFTP, SNMP, RIP, and VoIP. UDP supports Broadcasting.

---

#### Usecases for UDP: 

* Gaming, voice and video
* Services that don't need fixed packet transmission
* Multicasting and routing update protocols
* Fast applications

---

#### Telnet: 
Telnet is a set of rules designed for connecting one system with another. The connection process here is termed as remote login. The connection will be local computer and remote computer.

---

#### Gopher: 
Gopher is a collection of rules implemented for searching, retrieving as well as displaying documents from isolated sites. Gopher also works on the client/server principle.

---

#### PPTP: 
The Point-to-Point Tunneling Protocol (PPTP) is an obsolete method for implementing virtual private networks. PPTP has many well known security issues. PPTP uses a TCP control channel and a  Generic Routing Encapsulation tunnel to encapsulate PPP packets. Many modern VPNs use various forms of  UDP for this same functionality.

---

#### HTTP and Connections: 
A connection is controlled at the transport layer, and therefore fundamentally out of scope for HTTP. HTTP doesn't require the underlying transport protocol to be connection-based; it only requires it to be reliable, or not lose messages (at minimum, presenting an error in such cases). Among the two most common transport protocols on the Internet, TCP is reliable and UDP isn't. HTTP therefore relies on the TCP standard, which is connection-based.

Before a client and server can exchange an HTTP request/response pair, they must establish a TCP connection, a process which requires several round-trips. The default behavior of HTTP/1.0 is to open a separate TCP connection for each HTTP request/response pair. This is less efficient than sharing a single TCP connection when multiple requests are sent in close succession.

In order to mitigate this flaw, HTTP/1.1 introduced pipelining (which proved difficult to implement) and persistent connections: the underlying TCP connection can be partially controlled using the connection header. HTTP/2 went a step further by multiplexing messages over a single connection, helping keep the connection warm and more efficient.

Experiments are in progress to design a better transport protocol more suited to HTTP. For example, Google is experimenting with QUIC which builds on UDP to provide a more reliable and efficient transport protocol.


# Qestions


#### Explain the error control mechanismTCP protocol has methods for finding out corrupted 
segments, missing segments, out-of-order segments, and duplicated segments.

Error control in TCP is mainly done through the use of three simple techniques :

* Checksum 
* Acknowledgment 
* Retransmissionision

---

#### Define each of these layers of protocol stack?
The Service Transport layer transfer messages between different applications, such as HTTP, SMTP, FTP, and Blocks Extensible Exchange Protocol (BEEP). The XML Messaging layer encodes messages in XML format so that messages can be understood at each end, such as XML-RPC and SOAP. The Service Description layer describes the user interface to a web service, such as WSDL. The Service Discovery layer centralizes services to a common registry and offer simple publish functionality, such as UDDI.

---

#### What is the significance of TCP acknowledgments?

TCP acknowledgments are used to acknowledge packets that are successfully received by the host. The flag is set if the acknowledgment number field contains a valid acknowledgment number.

---

#### What is Retransmission?

The TCP retransmission means resending the packets over the network that have been either lost or damaged. Here, retransmission is a mechanism used by protocols such as TCP to provide reliable communication. Here, reliable communication means that the protocol guarantees the packet’s delivery even if the data packet has been lost or damaged. The networks are unreliable and do not guarantee the delay or the retransmission of the lost or damaged packets. The network, which uses a combination of acknowledgment and retransmission of damaged or lost packets, offers reliability.

---

#### Write down features of TCP?

Connection-oriented: An application requests a “connection” to the destination and uses the connection to transfer data
Stream Data transfer: It is the duty of TCP to pack this byte stream into packets, known as TCP segments, which are passed to the IP layer for transmission to the destination device.
* Reliable: It recovers data from the network layer if data is damaged, duplicated, or corrupted.
* Point to Point: TCP connection provides end-to-end delivery.
* Interoperability: It eliminates cross-platform boundaries.
* Error and flow control: Error-checking, flow-control, and acknowledgment functions.
 Name resolution: It helps in solving human-readable names into IP addresses.
* Routability: TCP/IP is a routable protocol,
* It helps in resolving logical addresses.
* Full Duplex: It provides connection in both directions.

---

#### Explain the process of TCP three-way handshaking protocol?

Process of TCP three-way handshaking protocol.

* Step one (SYN): In the first step, the client wants to establish a connection with the server, so it sends a segment with SYN(Synchronize Sequence Number) which informs the server that the client is likely to start communication and with what sequence number it starts segments.
* Step two (SYN + ACK): Server responds to the client request with the SYN-ACK signal bits set. Acknowledgment (ACK) signifies the response of the segment it received and SYN signifies with what sequence number it is likely to start the segment.
* Step three (ACK): In the final part, the client acknowledges the response of the server and they both establish a reliable connection with which they will start the actual data transfer.
Steps one, two establish the connection parameter (sequence number) for one direction and it is acknowledged. Steps two, three establish the connection parameter (sequence number) for the other direction and it is acknowledged. With these, full-duplex communication is established.

---

#### What are the TCP connections phases?

In TCP, connection-oriented transmission requires three phases: 

* Connection establishment
* Data Transfer
* Connection termination

---

#### What is the maximum size of the TCP header?

Maximum size of the TCP header = 60 bytes
Minimum size of the TCP header = 20 bytes
Write down the name of services provided by TCP?

Process to process communication
Stream orientation
Full duplex service
Multiplexing
Reliability

---

#### Write the name of all TCP “Flag”?

A TCP Flag field contains 6 different flags, namely:

* URG: Urgent pointer is valid
* ACK: Acknowledgement number is valid( used in case of cumulative acknowledgment)
* PSH: Request for push
* RST: Reset the connection
* SYN: Synchronize sequence numbers
* FIN: Terminate the connection

---

#### What is the role of the TCP checksum field?

One of the important fields of TCP protocol format. It is 16 bits long. This field holds the checksum for error control. It is mandatory in TCP as opposed to UDP. 

---

#### Write the name of the Well-Known Port used by TCP?

Well-Known Ports. Port numbers can run from 0 to 65353. Port numbers from 0 to 1023 are reserved for common TCP/IP applications and are called well-known ports. The use of well-known ports allows client applications to easily locate the corresponding server application processes on other hosts. The most common well-known port is 80, which identifies HTTP traffic for a Web server.

---

#### Define the term Endpoint in TCP?

TcpEndpoint allows you to easily establish and communicate over TCP/IP network connections between client and server processes, possibly residing on different hosts. The TcpEndpoint class follows a telephone-like model of networking: clients “call” servers and servers “answer” clients. Once a network connection is established between a client and a server, the two can “talk” to each other by reading from and writing to the connection.

---

#### How HTTP protocol works?

Clients and servers communicate by exchanging individual messages (as opposed to a stream of data). The messages sent by the client, usually a Web browser, are called requests and the messages sent by the server as an answer are called responses.  HTTP can also be used to fetch parts of documents to update Web pages on demand.

On the opposite side of the communication channel is the server, which serves the document as requested by the client. A server appears as only a single machine virtually; but it may actually be a collection of servers sharing the load (load balancing), or a complex piece of software interrogating other computers (like cache, a DB server, or e-commerce servers), totally or partially generating the document on demand.

A server is not necessarily a single machine, but several server software instances can be hosted on the same machine. With HTTP/1.1 and the host header, they may even share the same IP address. 

---

#### What can be controlle by HTTP?

* Caching: 
The server can instruct proxies and clients about what to cache and for how long. The client can instruct intermediate cache proxies to ignore the stored document.
Relaxing the origin constraint
* Authentication: 
Some pages may be protected so that only specific users can access them. Basic authentication may be provided by HTTP, either using the www-authenticate and similar headers, or by setting a specific session using HTTP cookies
* Proxy and Tunneling: 
Servers or clients are often located on intranets and hide their true IP address from other computers. HTTP requests then go through proxies to cross this network barrier. Not all proxies are HTTP proxies. The SOCKS protocol, for example, operates at a lower level. Other protocols, like ftp, can be handled by these proxies.
* Sessions:  
Using HTTP cookies allows you to link requests with the state of the server. This creates sessions, despite basic HTTP being a state-less protocol. This is useful not only for e-commerce shopping baskets, but also for any site allowing user configuration of the output.

---

#### HTTP Flow: 

* Open a TCP connection
* Send an HTTP message
* Read the response sent by the server
* Close or reuse the connection for further requests
* What are HTTP Request and Response headers?

Follow This Link

---

#### What is HTTP Caching? 
Prevent to send many unnecessary request to the server. The basic cache mechanisms in HTTP/1.1 are implicit directives to caches where server-specifies expiration times and validators. We use the Cache-Control header for this purpose. This Link contains values of cache header.

Types of Caching: The type of cache is defined according to where the content is stored.

Browser cache - this storage is done in the browser. All browsers have a local storage, which is usually used to retrieve previously accessed resources. This type of cache is private since stored resources are not shared.
Proxy cache - this storage, also called intermediate caching, is done on the proxy server, between the client and the origin server. This is a type of shared cache as it’s used by multiple clients and is usually maintained by providers.
Gateway cache - also called reverse proxy, it’s a separate, independent layer, and this storage is between the client and the application. It caches the requests made by the client and sends them to the application and does the same with the responses, sending from the application to the client. If a resource is requested again, the cache returns the response before reaching the application. It’s also a shared cache, but by servers not users.
Application cache - this storage is done in the application. It allows the developer to specify which files the browser should cache and make them available to users even when they are offline.
Caching: Solution for having Super High Speed and Powerful Performance
Edge Caching is the best solution for those who want a super fast website with high performance. And how is that possible? One of the main reasons is because caching is done at the network edge, closer to the end-users. The other reason is because it supports thousands of simultaneous requests without compromising  infrastructure.

In addition, caching service delivers all HTTP and HTTPS-based content types, including static files and live or on-demand videos, even if your origin server is unavailable. It improves the performance and reliability when delivering content to any size of audience, reducing failures and latency while increasing transfer rates.

Edge Caching has a reverse proxy architecture whereby clients connect to the edge nodes of highly distributed global network. In it, you can cache your content and even expand its versatility with the L2 Caching add-on, an additional layer of caching between Azion’s edge and its origin, which helps to reduce the load on your infrastructure.
