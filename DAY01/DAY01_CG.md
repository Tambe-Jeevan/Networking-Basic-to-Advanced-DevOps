# Day 1 – Networking Fundamentals: How Devices Talk to Each Other 🌐

Welcome to **Day 1 of your Networking Mastery Journey, Jeevan!**

Since you already work as a Technical/Desktop Support Engineer, you've likely configured IP addresses, troubleshot internet issues, connected printers, and checked network cables. Today, we'll connect those daily tasks to the core networking concepts used in DevOps.

We'll follow your learning system:

* **30 minutes:** Concept
* **60 minutes:** Hands-on practice
* **30 minutes:** Mini task

---

## 1️⃣ Concept (30 Minutes)

Imagine you're sending a courier package to a friend.

For successful delivery, you need:

* Your address
* Your friend's address
* Roads to travel on
* Traffic rules
* A delivery service

Computer networks work the same way.

| Real World     | Networking                      |
| -------------- | ------------------------------- |
| House          | Device (Laptop, Server, Mobile) |
| Address        | IP Address                      |
| Local Road     | Switch                          |
| Highway        | Router                          |
| Courier Parcel | Data Packet                     |
| Post Office    | ISP                             |

When you open a website, small pieces of data called **packets** travel through multiple devices before reaching the destination.

---

## 2️⃣ Important Networking Terms

### Host

Any device connected to a network.

Examples:

* Laptop
* Mobile phone
* Server
* Printer

---

### Client

A device that requests a service.

Example:

Your laptop requests a webpage from a web server.

---

### Server

A device that provides a service.

Examples:

* Web server
* File server
* DNS server
* Database server

---

### Bandwidth

The maximum amount of data that can be transferred per second.

Example:

A **100 Mbps** internet connection.

Think of bandwidth as the width of a highway.

---

### Latency

The time taken for data to travel from source to destination.

Measured in milliseconds (ms).

Lower latency is better.

Think of latency as travel time.

---

### Throughput

The actual amount of data transferred successfully.

Example:

You have a 100 Mbps connection but only get 70 Mbps due to network congestion.

---

## 3️⃣ Types of Networks

![Image](https://images.openai.com/static-rsc-4/OZPe4rWPz2_N2UbXv2NOJYKGI9cynwSVQgCJzpJVyjbVABs555TNaeab55pfa7GFB9ok7zxbe1LXuyG66teDzdaQKQPQpZecw1FAGKTI5oWYZlep9B1hGPKxAHId8roWf0RNhDgMwHlvYXEuLmxwIF7X4mwwn5a0XrEYQIYDe2H9nQSExXPsTA7BR5Ysw5Ho?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/4wcIb2ZHJ52evJOlUPpdYVwAZ73slvkb0iTT6G6MQUHLEo0qDQjiR-yS6bHe1yQJGpL-bLm5lPYARB6U7MUxO1GWJMWRpQ13kQLPiZpbzKWEUGoLZDz7s15zDVupF9-atHRGpfE27_B-Jirsawk1wkNuVPTGODxUC4F-YEReResl_b5cx6K0FIOXjw4nDBln?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/IJ4_0iGNHN_t4XYcNb6LoiswmcRYuXe9H_fBcRBI8zSYu-b-mRixr8sNs0q7-bsnKBIQ9J6rW9CIfeVleMuNlbBSsTPWSud-6VsEF3spxnvvI9AR7FmvqNSfDDyici8IXSMnxYMnOeghvEbXPsSTFywPczxjPlYsWWAEHrLlI7DNVw41Di5FYubI5IJ7VDk9?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/n-lv7NX2pD1p6NtAANIuDtNlmFM5KOr4Nl56WBvGYGAIE_-iRrYotbrMhfXf8-90mvktnoHfrxh3cucg1RgUhNv49i98Onmkv1iF5Kfq8_zS14AdQeFecPobyc3VUPc-SO1FCihrW5VFv_kP6HaJaRmAoKmbmFzyFc1EKz90e68I6DtSkNrCb0v3rPhYxxaa?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Lp2iUxIXvKJlbXjIPKAzUJtzs1rz8_J6WsdiYSIvZCdW13pTe4dnaBbxnEYFM1-lr47hK3Vw3fKntznpCTinvdKKBTl297415od7eUDTsg2cdYCSbLXi2ILrqeiiF6-yGrDEnVMYg47REI0eqoyqyx_74swjQSc8nsb7NBCTkgnDo20jLHp1H3cIdlKRDouj?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UP3bTBY9CJgIPORuREcEBOh1MYXVyEN_4GAKXLDwyJt0nn_lcSOwQJwNRGeEPv4S6-rlaBhcL08HguEO_gsyIvB2vn4ykFCD12-ta-3DBQJbLJPxl3IaTN5AhVu-KaodHxT1Ek6T9jd-T-vNLBCx7fTynWIUY7a61Q-qoy3-HEWGR6cVXNUclIFz9bFYf7kb?purpose=fullsize)

### PAN (Personal Area Network)

Short-range network around a person.

Examples:

* Bluetooth headset
* Smartwatch

---

### LAN (Local Area Network)

Network inside a home, office, or building.

Examples:

* Office Wi-Fi
* Home router network

---

### MAN (Metropolitan Area Network)

Connects networks across a city.

Example:

City-wide internet service.

---

### WAN (Wide Area Network)

Connects networks over large geographical areas.

Example:

The Internet.

---

## 4️⃣ Essential Network Devices

![Image](https://images.openai.com/static-rsc-4/5j6I0G9WjzgJ8pOtX_qeFBDDRLXJ_SDBv4LVnKYQ7SkD-fEEnDzLEXncGS7ubD96XwxqZgqP7Aq_6sunKbG7xUPEeYOa29nKDcrZiiMLigdrq-UcfRDOXltnV0x1_mPtuQBcNHgjzJ4Qm1AkBC7lcHQFqJM1wVl-MDXfgDNQKJEGUDAlNMH6HwqULT91URw2?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/LSjK27nskSkHf85ZFbgaFOon3pM7-42iscOLwMbxBwDvCcDERJyfdiAXKwgNM4EwTKg1hGc8tShmWCqyTmJG38DCXWWiDDMprZF0W5DVddU8yL08-DPK09BkL80lPR1Rwd1xh-UdFlyrY8wgGM2SsqKnIs63oF8gHwhARP8x8G2Yl1mlHw5VQ6A8IPfCSPVf?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/2xrNDGrxxZgeTwbw7WfUEH6-Cj4UgT_Auz-K-NdNHw4Qtj4ovxbzHc8ae_DcGAECKhliWw6fTIg8wpe7prKByJgRAGIJPcs3KuLSDbqJZLMhEHza3b_XYSyGabzqS4sHYsYxCB6w4A21L73A29--0KhzhxQRSek2c0xasMJFMR68rcxySMXX1jDVrjhQkEJm?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/cAeYtcEzGRZgoepvMRmxiq5_cYluKnlJBo1K1kAexq6j36j7E09kmw65I70AHRYEBCMLn5PptNT85WhrMrRhuCfGddiJaY5LapD-0suLbzzB7HTQRk0VsikCsjPfuTa_qKu2sAGCd3ss-IqOSPrS4Yhju4z-mT5_6sTjbXY69Wvl8tDvpUe78w1zf5Qkn1v2?purpose=fullsize)

### Modem

Connects your home or office to your Internet Service Provider (ISP).

---

### Router

Connects different networks together.

Example:

Your home router connects your LAN to the internet.

---

### Switch

Connects devices within the same network.

Examples:

* PCs
* Printers
* Servers

---

### Access Point (AP)

Provides wireless connectivity.

---

### Firewall

Filters network traffic based on security rules.

DevOps engineers frequently work with firewall configurations.

---

## 5️⃣ Setup Environment (Important)

Open **Command Prompt** as Administrator.

You'll use it throughout this networking journey.

Press:

```text
Windows + R
```

Type:

```text
cmd
```

Press **Ctrl + Shift + Enter**.

---

## 6️⃣ Hands-On Practice (60 Minutes)

### Step 1: Check your network configuration

Run:

```cmd
ipconfig /all
```

Identify:

* IPv4 Address
* Subnet Mask
* Default Gateway
* DNS Server
* Physical Address (MAC)

Example:

```text
IPv4 Address . . . . . . : 192.168.1.10
Subnet Mask . . . . . . : 255.255.255.0
Default Gateway . . . . : 192.168.1.1
DNS Servers . . . . . . : 8.8.8.8
Physical Address . . . : 00-1A-2B-3C-4D-5E
```

---

### Step 2: Test internet connectivity

Run:

```cmd
ping 8.8.8.8
```

If this works, your internet connection is active.

Observe:

* Reply time (ms)
* Packet loss

---

### Step 3: Test DNS resolution

Run:

```cmd
ping google.com
```

If this works, DNS is functioning correctly.

---

### Step 4: View network adapters

Press:

```text
Windows + R
```

Type:

```text
ncpa.cpl
```

You will see all available network adapters:

* Ethernet
* Wi-Fi
* VPN adapters

Identify which adapter is currently active.

---

## 7️⃣ Mini Task (30 Minutes)

Create a simple table in your notes:

| Parameter       | Value |
| --------------- | ----- |
| IPv4 Address    |       |
| Subnet Mask     |       |
| Default Gateway |       |
| DNS Server      |       |
| MAC Address     |       |

Then answer these questions:

1. Are you connected via Wi-Fi or Ethernet?
2. Is your IP address public or private?
3. What device is acting as your default gateway?

---

## 8️⃣ What You Learned Today

* What a network is
* Types of networks (PAN, LAN, MAN, WAN)
* Difference between client and server
* Bandwidth, latency, and throughput
* Router, switch, modem, access point, and firewall
* How to check your network configuration
* How to test internet connectivity using `ping`

---

## 9️⃣ Homework

1. Find the model number of your home router.

2. Login to your router dashboard by entering your **default gateway IP address** in a browser.

Examples:

```text
http://192.168.1.1
http://192.168.0.1
```

Explore these sections only:

* Connected devices
* DHCP settings
* Wi-Fi settings

⚠️ Do not change any settings yet.

---

### Tomorrow – Day 2

We will learn:

* IP Address vs MAC Address
* How devices find each other
* ARP (Address Resolution Protocol)
* Broadcast, Unicast, and Multicast communication

Just come back and type:

**"Day 2 Networking study"** 🚀
