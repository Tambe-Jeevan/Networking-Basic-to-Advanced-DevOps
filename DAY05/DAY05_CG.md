# Day 4 – TCP/IP Model & TCP vs UDP 🌐

Welcome back, Jeevan! 🚀

Yesterday, you learned the **OSI Model**. Today, you'll learn the **TCP/IP Model**, which is the actual model used on the Internet.

This is one of the most important topics for:

* Technical Support Engineer
* System Administrator
* Network Engineer
* DevOps Engineer
* Cloud Engineer

Many interview questions come directly from TCP, UDP, and the TCP Three-Way Handshake.

We'll follow your learning system:

* **30 minutes:** Concept
* **60 minutes:** Hands-on practice
* **30 minutes:** Mini task

---

# 1️⃣ Concept (30 Minutes)

## What is TCP/IP?

TCP/IP stands for:

* **TCP** → Transmission Control Protocol
* **IP** → Internet Protocol

TCP/IP is the communication language of the Internet.

When you:

* Open Google
* Send an email
* Watch YouTube
* Use WhatsApp

TCP/IP is working in the background.

---

# 2️⃣ TCP/IP Model Layers

Unlike the OSI Model (7 Layers), TCP/IP has 4 layers.

| TCP/IP Layer   | OSI Equivalent |
| -------------- | -------------- |
| Application    | 7,6,5          |
| Transport      | 4              |
| Internet       | 3              |
| Network Access | 2,1            |

### Easy Diagram

```text
Application Layer
      ↓
Transport Layer
      ↓
Internet Layer
      ↓
Network Access Layer
```

---

# 3️⃣ Application Layer

User-facing protocols.

Examples:

| Protocol | Purpose              |
| -------- | -------------------- |
| HTTP     | Website              |
| HTTPS    | Secure Website       |
| DNS      | Name Resolution      |
| FTP      | File Transfer        |
| SMTP     | Email Sending        |
| SSH      | Secure Remote Access |

Example:

```text
https://google.com
```

Uses:

* HTTPS
* DNS

---

# 4️⃣ Transport Layer

This layer uses:

### TCP

and

### UDP

Most interview questions focus here.

---

# 5️⃣ TCP (Transmission Control Protocol)

TCP is:

✅ Reliable

✅ Connection-oriented

✅ Error checking

✅ Ordered delivery

Think of TCP like a courier service requiring signatures.

---

## Examples Using TCP

| Service | Port |
| ------- | ---- |
| HTTP    | 80   |
| HTTPS   | 443  |
| SSH     | 22   |
| FTP     | 21   |
| SMTP    | 25   |

---

### TCP Features

* Guaranteed delivery
* Sequence numbers
* Acknowledgments
* Retransmission

If a packet is lost:

TCP sends it again.

---

# 6️⃣ UDP (User Datagram Protocol)

UDP is:

✅ Fast

✅ Lightweight

❌ No guarantee of delivery

❌ No acknowledgment

Think of UDP like radio broadcasting.

---

## Examples Using UDP

| Service         | Port    |
| --------------- | ------- |
| DNS             | 53      |
| DHCP            | 67/68   |
| VoIP            | Various |
| Video Streaming | Various |
| Online Gaming   | Various |

---

### UDP Features

* No connection setup
* Faster than TCP
* Low overhead

---

# 7️⃣ TCP vs UDP Interview Table

| Feature         | TCP      | UDP          |
| --------------- | -------- | ------------ |
| Reliable        | Yes      | No           |
| Fast            | No       | Yes          |
| Connection      | Required | Not Required |
| Error Checking  | Yes      | Limited      |
| Acknowledgement | Yes      | No           |
| Usage           | Websites | Streaming    |

---

# 8️⃣ TCP Three-Way Handshake

This is one of the most important interview topics.

Before communication starts:

Client and Server establish a connection.

---

### Step 1 – SYN

Client says:

```text
Can we communicate?
```

---

### Step 2 – SYN-ACK

Server says:

```text
Yes, I am ready.
```

---

### Step 3 – ACK

Client says:

```text
Great, let's start.
```

---

### Diagram

```text
Client                Server

SYN      --------->

         <--------- SYN-ACK

ACK      --------->
```

Connection established ✅

---

# 9️⃣ Real Example

When you open:

```text
https://google.com
```

The browser:

1. Resolves DNS
2. Finds Google IP
3. Performs TCP Handshake
4. Starts HTTPS communication

This entire process happens in milliseconds.

---

# 🔟 Hands-On Practice (60 Minutes)

## Step 1 – Check Active TCP Connections

Open Command Prompt:

```cmd
netstat -an
```

Observe:

```text
TCP 192.168.x.x:xxxxx
```

These are active TCP sessions.

---

## Step 2 – View Listening Ports

```cmd
netstat -ano
```

Look for:

```text
LISTENING
```

---

## Step 3 – Test Connectivity

```cmd
ping google.com
```

Observe latency.

---

## Step 4 – Trace Route

```cmd
tracert google.com
```

Observe how packets travel.

---

## Step 5 – Open Browser

Visit:

```text
https://google.com
```

Then run:

```cmd
netstat -an | findstr 443
```

You should see active HTTPS connections using TCP port 443.

---

# 1️⃣1️⃣ Understanding Common Protocol Flow

Opening a website:

```text
Browser
 ↓
DNS Query
 ↓
IP Address Found
 ↓
TCP Handshake
 ↓
HTTPS Communication
 ↓
Website Loaded
```

---

# 1️⃣2️⃣ Interview Questions

### Q1. What is TCP?

A reliable, connection-oriented transport protocol.

---

### Q2. What is UDP?

A fast, connectionless transport protocol.

---

### Q3. Which is faster?

UDP.

---

### Q4. Which is more reliable?

TCP.

---

### Q5. Why does HTTPS use TCP?

Because data delivery must be guaranteed.

---

### Q6. Why does video streaming use UDP?

Because speed is more important than perfect delivery.

---

### Q7. Explain the TCP Three-Way Handshake.

1. SYN
2. SYN-ACK
3. ACK

Used to establish a TCP connection.

---

# 1️⃣3️⃣ Mini Task (30 Minutes)

Create this table in your notes:

| Service | TCP or UDP | Port |
| ------- | ---------- | ---- |
| HTTP    |            |      |
| HTTPS   |            |      |
| DNS     |            |      |
| SSH     |            |      |
| DHCP    |            |      |

---

Answer:

1. Why is TCP reliable?
2. Why is UDP faster?
3. What are the three steps of the TCP Handshake?

---

# 1️⃣4️⃣ What You Learned Today

✅ TCP/IP Model

✅ TCP vs UDP

✅ Three-Way Handshake

✅ Common protocols

✅ Active connections using `netstat`

✅ Website communication flow

---

# 📚 Homework

Memorize these ports:

```text
20,21  FTP
22     SSH
23     Telnet
25     SMTP
53     DNS
67,68  DHCP
80     HTTP
110    POP3
143    IMAP
443    HTTPS
3389   RDP
```

Also remember:

```text
TCP = Reliable
UDP = Fast
```

---

## Tomorrow – Day 5

We will start **IPv4 Addressing**:

* Public vs Private IP
* Classes A, B, C
* Network ID and Host ID
* CIDR Notation
* Real-world IP calculations

Just come back and type:

**"Day 5 Networking study"** 🚀