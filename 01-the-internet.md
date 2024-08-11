# 01. The Internet
- [01. The Internet](#01-the-internet)
  - [Protocols](#protocols)
  - [IP](#ip)
  - [IP addresses (IPv4)](#ip-addresses-ipv4)
  - [IPv6](#ipv6)
  - [DNS spoofing](#dns-spoofing)
  - [Routers and packets](#routers-and-packets)
  - [TCP (Transmission Control Protocol)](#tcp-transmission-control-protocol)
  - [UDP (User Datagram Protocol)](#udp-user-datagram-protocol)
  - [URL](#url)
  - [HTTP](#http)
    - [Key Features of HTTP:](#key-features-of-http)
    - [HTTP Methods:](#http-methods)
    - [Example of an HTTP Request and Response:](#example-of-an-http-request-and-response)
      - [Request:](#request)
      - [Response:](#response)
  - [HTTPS](#https)
    - [Three-way Handshake](#three-way-handshake)
    - [Pipelining](#pipelining)
  - [SSL/TLS](#ssltls)
  - [Ports](#ports)
  - [Sockets](#sockets)
    - [How Sockets Work:](#how-sockets-work)
    - [Sockets in Practice:](#sockets-in-practice)
    - [WebSockets](#websockets)
    - [How WebSockets Differ from Regular Sockets:](#how-websockets-differ-from-regular-sockets)

##  Protocols

A protocol is a well##known set of rules and standards that, if all parties agree to use it,  will allow them to communicate without trouble.

##  IP

IP means internet protocol.

##  IP addresses (IPv4)

Traditional IP addresses are 32  bits long with 8 bits for each part of the address. The earlier numbers usually identify  the country (network) and regional (subnetwork) network of the device. Then come the subnetworks, and then finally the  address of the specific device. This version of IP addressing is called IPv4. It was designed  in 1973 and widely adopted in the early 80s and provides for more than 4 billion unique  addresses for devices connecting to the internet. 
![IPv4](<images/01-the-internet/Screenshot from 2024-07-09 22-54-57.png>)

##  IPv6 

IPv6 uses 128 bits per address and provides over 340 undecillion unique  addresses (2^128 addresses).
An IPv6 address is represented as eight groups of four hexadecimal digits, separated by colons. Here’s an example:
```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```
For convenience, leading zeros in each group can be omitted, and consecutive groups of zeros can be replaced with a double colon (::), but this can be done only once in an address. The above address can be shortened to:
```
2001:db8:85a3::8a2e:370:7334
```
This address identifies a unique device on the IPv6 network, similar to how an IPv4 address identifies a device on an IPv4 network.

## DNS spoofing

DNS spoofing, also known as DNS cache poisoning, is a type of cyber attack where an attacker introduces false information into a DNS resolver's cache, causing it to return an incorrect IP address. This leads users to be redirected to malicious sites without their knowledge.

## Routers and packets

As part of the Internet Protocol, every router keeps track of  multiple paths for sending packets, and it chooses the cheapest available path for each piece of data  based on destination IP address for the packet. 

## TCP (Transmission Control Protocol)

TCP manages the sending and receiving of all your data as packets.  Think of it like a guaranteed mail service. When you request a song on your device, Spotify  sends a song broken up into many packets.  When your packets arrive, TCP does a full  inventory and sends back acknowledgments of each packet received. If all packets are there, TCP  signs for your delivery and you’re done. The missing packets will be resent.

## UDP (User Datagram Protocol)

**Connectionless**: No connection setup required, data is sent in individual packets (datagrams). 
**Unreliable**: Does not guarantee delivery of data packets.  
**Unordered delivery:** Data packets may arrive out of sequence.
**No error checking:** Does not detect or correct errors.  
**Faster:** Less overhead, making it suitable for real-time applications.  
**Ideal for:** Online gaming, video streaming, voice communication, and other applications where speed is prioritized over reliability. 


## URL

A URL (Uniform Resource Locator) is a reference or address used to access resources on the internet. It specifies the location of a resource as well as the protocol used to retrieve it.

**Components of a URL:**
1. **Protocol**: Indicates the method used to access the resource. Common protocols include HTTP (`http://`), HTTPS (`https://`), FTP (`ftp://`), etc.
2. **Host**: The domain name or IP address of the server where the resource is located (e.g., `www.example.com`).
3. **Port (optional)**: Specifies the port number on the server to connect to. If omitted, the default port for the protocol is used (e.g., port 80 for HTTP).
4. **Path**: The specific location or directory of the resource on the server (e.g., `/path/to/resource`).
5. **Query (optional)**: A string of key-value pairs separated by `&` that provides additional parameters (e.g., `?key1=value1&key2=value2`).
6. **Fragment (optional)**: A section within the resource, indicated by a `#` followed by an identifier (e.g., `#section1`).

**Example of a URL:**
```
https://www.example.com:443/path/to/resource?key1=value1&key2=value2#section1
```
- **Protocol**: `https`
- **Host**: `www.example.com`
- **Port**: `443`
- **Path**: `/path/to/resource`
- **Query**: `?key1=value1&key2=value2`
- **Fragment**: `#section1`

This URL points to a specific resource on a web server using the HTTPS protocol, including query parameters and a fragment identifier.

## HTTP

HTTP (HyperText Transfer Protocol) is the foundational protocol used for transmitting data on the World Wide Web. It defines how messages are formatted and transmitted, and how web servers and browsers should respond to various commands.

### Key Features of HTTP:
1. **Client-Server Model**: HTTP operates on a request-response model where the client (e.g., a web browser) sends a request to a server, which then sends back a response.
2. **Stateless**: Each HTTP request and response pair is independent; the server does not retain any information about previous requests from the same client.
3. **Text-Based**: HTTP messages are human-readable and include methods like GET, POST, PUT, and DELETE, which indicate the desired action to be performed.

### HTTP Methods:
- **GET**: Requests data from a server (e.g., loading a web page).
- **POST**: Submits data to a server (e.g., form submission).
- **PUT**: Updates existing data on a server.
- **DELETE**: Removes data from a server.

### Example of an HTTP Request and Response:
#### Request:
```
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
```

#### Response:
```
HTTP/1.1 200 OK
Content-Type: text/html

<!DOCTYPE html>
<html>
<head>
<title>Example Page</title>
</head>
<body>
<h1>Welcome to Example.com!</h1>
</body>
</html>
```

- **Request Line**: Specifies the method (GET), the resource path (/index.html), and the HTTP version (HTTP/1.1).
- **Headers**: Provide additional information such as the host (www.example.com) and user-agent.
- **Response Line**: Indicates the HTTP version (HTTP/1.1), status code (200 OK), and a message.
- **Headers**: Detail the type of content being returned (text/html).
- **Body**: Contains the actual content of the web page.

## HTTPS

HTTPS is a more secure version of HTTP, which encrypts the data being transmitted between the client and server using SSL/TLS (Secure Sockets Layer/Transport Layer Security) encryption. This provides an additional layer of security, helping to protect sensitive information such as login credentials, payment information, and other personal data.

### Three-way Handshake

The Three-way Handshake is a process used in the Transmission Control Protocol (TCP) to establish a reliable connection between a client and a server over a network. This handshake ensures that both the client and server are ready to communicate and that the connection is set up correctly.

  - SYN - Client picks up a random number, let’s say x, and sends it to the server.
  - SYN ACK - Server acknowledges the request by sending an ACK packet back to the client which is made up of a random number, let’s say y picked up by server and the number x+1 where x is the number that was sent by the client
  - ACK - Client increments the number y received from the server and sends an ACK packet back with the number y+1

### Pipelining

Pipelining, where the client could send multiple requests to the server without waiting for the response from server on the same connection and server had to send the response in the same sequence in which requests were received.


## SSL/TLS

 The Secure Sockets Layer and Transport Layer Security protocols are used to provide secure communication over the internet.

 **SSL (Secure Sockets Layer)** and **TLS (Transport Layer Security)** are cryptographic protocols designed to secure communication over a computer network. They ensure that data transmitted between a client (like a web browser) and a server (like a website) remains private and integral.

 SSL/TLS are protocols that secure communication over the internet by encrypting data, verifying the identity of communicating parties, and ensuring data integrity. **TLS has largely replaced SSL due to improved security features.**

1. **Encryption**: 
   - SSL/TLS encrypts the data transmitted between a client and server, making it unreadable to anyone who might intercept it. This protects sensitive information, like passwords and credit card numbers.

2. **Authentication**:
   - SSL/TLS uses digital certificates to authenticate the identity of the server (and sometimes the client). This ensures that the client is communicating with the legitimate server, not an imposter.

3. **Data Integrity**:
   - SSL/TLS ensures that the data has not been tampered with during transmission. If any data is altered, the connection will be terminated.

- SSL/TLS is commonly used in securing web traffic (HTTPS), email (SMTPS), instant messaging, and other internet-based communications.

## Ports

Ports are used to identify the application or service running on a device. Each application or service is assigned a unique port number, allowing data to be sent to the correct destination.

A port is a logical endpoint in a network connection. When data is transmitted over the internet or any network, it is sent to an IP address. Ports help determine which application or service on the device should receive that data.

Each port is identified by a number, ranging from 0 to 65535.

Well-Known Ports:

    Range from 0 to 1023.
    These are reserved for common protocols and services. For example:
        HTTP: Port 80
        HTTPS: Port 443
        FTP: Port 21
        SMTP: Port 25

Registered Ports:

    Range from 1024 to 49151.
    These ports are assigned to specific applications or services by organizations, but they are not as universally recognized as well-known ports. For example:
        MySQL: Port 3306
        PostgreSQL: Port 5432

Dynamic or Private Ports:

    Range from 49152 to 65535.
    These are usually used temporarily by applications to communicate with a server or another device. They are often chosen at random and are used for the duration of a session.

**Multiple Services on One IP:** A single device with one IP address can run multiple services or applications simultaneously, each using a different port. This allows a server to host a web page (on port 80), an email service (on port 25), and a file transfer service (on port 21), all at the same time.

**Firewalls and Security:** Firewalls use port numbers to control traffic. By allowing or blocking specific ports, a firewall can permit certain types of traffic while denying others, helping secure the network.

**Port Forwarding:** In home networks, routers use port forwarding to send incoming traffic on specific ports to the correct device on the local network. This is often used in gaming, remote desktop access, or hosting a server at home.

## Sockets

**Definition**: A socket is an endpoint for sending or receiving data across a computer network. It allows two devices to communicate with each other over a network, typically using TCP (Transmission Control Protocol) or UDP (User Datagram Protocol).

- **Sockets** are the fundamental building blocks for network communication, enabling two devices to exchange data using TCP or UDP.
- **WebSockets** are a specialized type of communication protocol designed for real-time, bi-directional communication over a single, persistent connection in web applications. While related to the concept of sockets, WebSockets are specifically tailored for use in web environments and differ in how they establish and manage connections.

### How Sockets Work:

1. **Creation**:
   - A socket is created by a program (an application or service) that needs to send or receive data. This is done using the operating system's networking API, typically through system calls like `socket()`.

2. **Binding**:
   - The socket is bound to a specific IP address and port number. The IP address identifies the device on the network, while the port number identifies the specific application or service on that device.

3. **Listening and Connecting**:
   - In the case of TCP:
     - **Server Side**: The socket can listen for incoming connections from other devices. This involves calling `listen()` and `accept()`.
     - **Client Side**: The socket can initiate a connection to a server by specifying the server’s IP address and port number, using `connect()`.

   - In the case of UDP:
     - Since UDP is connectionless, the socket simply sends or receives data packets to or from a specified IP address and port without establishing a connection.

4. **Data Transmission**:
   - Once a connection is established (in TCP) or a target address is specified (in UDP), data can be sent or received through the socket using functions like `send()`, `recv()`, `sendto()`, and `recvfrom()`.

5. **Closing**:
   - After the communication is complete, the socket is closed using `close()`. This frees up the resources and ends the communication.

### Sockets in Practice:

- **Web Browsing**: When you visit a website, your browser creates a socket to connect to the web server’s IP address on port 80 (HTTP) or 443 (HTTPS).
- **Email**: Your email client uses sockets to connect to an email server on ports like 25 (SMTP) or 993 (IMAP).
- **Gaming**: Online games use sockets to connect players’ devices to game servers, enabling real-time interaction.

### WebSockets

**Definition**: WebSockets are a protocol that provides full-duplex communication channels over a single, long-lived connection between a client (like a web browser) and a server. This allows for real-time communication in web applications.

### How WebSockets Differ from Regular Sockets:

1. **Purpose**:
   - **Sockets**: General-purpose endpoints used in network communication for various protocols like TCP and UDP.
   - **WebSockets**: Specifically designed to enable real-time communication in web applications. They are built on top of HTTP but allow for a persistent connection that can send and receive messages in both directions.

2. **Connection Establishment**:
   - **Sockets**: In TCP, a connection is established through a handshake process (SYN, SYN-ACK, ACK), and the connection remains until it’s explicitly closed.
   - **WebSockets**: Begin with an HTTP handshake. If the server supports WebSockets, it upgrades the connection from HTTP to WebSocket, establishing a persistent, bi-directional communication channel.

3. **Communication**:
   - **Sockets**: Data is typically sent in a stream (TCP) or individual packets (UDP). The application must manage the format and protocol of the data.
   - **WebSockets**: Data is sent as messages, which can be either text or binary. WebSockets automatically manage the framing of messages, making it easier to handle structured data like JSON in web applications.

4. **Use Cases**:
   - **Sockets**: Used in a wide range of applications, from file transfers to streaming services and beyond.
   - **WebSockets**: Ideal for web applications that require real-time updates, such as live chat, online gaming, live sports scores, financial tickers, and collaborative editing.

