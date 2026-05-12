# Socket Programming and Networking Concepts

## 1. Sockets

- Sockets are an **abstraction provided by operating systems** to enable communication between different processes, either **on the same machine** or **over a network**.
- A **socket** is **one end-point of a two-way communication link** between two programs running on the network.

---

## 2. Java Networking (`java.net` package)

- **Socket**  
  - Implements the **client side** of a connection.
- **ServerSocket**  
  - Implements the **server side** of a connection.

---

## 3. Port Numbers

- Each **socket is bound to a port number** to identify the application that data is to be sent to.
- A **server waits on the listening socket** for incoming connections.
- The **client** knows the **hostname** and **port** of the server it wants to connect to.
- The client also needs to **identify itself to the server** by binding to a **local port number** that it will use during this connection.

---

## 4. Endpoints

- An **endpoint** consists of:  
  - **TCP / UDP protocol**  
  - **IP address**  
  - **Port number**

- Each host has **65,536 ports** (0–65535).

### Port Ranges

| Range       | Description          | Typical Use                               |
|------------:|-------------------  |-----------------------------------------|
| 0–1023      | Well-known ports     | HTTP (80), FTP (21), SSH (22)           |
| 1024–49151  | Registered ports     | Applications/services that need specific ports |
| 49152–65535 | Ephemeral/dynamic    | Client-side connections, OS-assigned automatically |

### Common Well-Known Ports

| Port | Service |
|------|---------|
| 20, 21 | FTP |
| 23     | Telnet |
| 80     | HTTP |

---

## 5. TCP vs UDP

- **TCP (Transmission Control Protocol)**
  - Connection-oriented
  - Reliable data transfer
  - Uses **handshake** to establish connection
  - Guarantees delivery and order of packets

- **UDP (User Datagram Protocol)**
  - Connectionless
  - Unreliable, no guarantee of delivery or order
  - Lower overhead, faster
  - Used for applications like streaming or gaming where speed is more important than reliability
