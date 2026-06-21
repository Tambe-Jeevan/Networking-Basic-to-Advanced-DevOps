# Day 2 – IP Address, MAC Address & How Devices Find Each Other 🌐

Welcome back, Jeevan! 🚀

Yesterday, you learned what networks are and how devices connect through routers, switches, and the internet.

Today, you'll understand **how your laptop actually communicates with another device on the network.**

As a future DevOps engineer, these concepts will help you troubleshoot:

* Server connectivity issues
* Container networking problems
* DNS failures
* Cloud networking issues
* Kubernetes communication problems

We'll follow your learning system:

* **30 minutes:** Concept
* **60 minutes:** Hands-on practice
* **30 minutes:** Mini task

---

## 1️⃣ Concept (30 Minutes)

Imagine you want to send a package to a friend in another city.

You need:

* The city address → **IP Address**
* The exact house identifier → **MAC Address**

Both are necessary for successful delivery.

---

## 2️⃣ IP Address vs MAC Address

| Feature     | IP Address                       | MAC Address                        |
| ----------- | -------------------------------- | ---------------------------------- |
| Purpose     | Identifies a device on a network | Identifies the network card itself |
| Assigned By | Router or administrator          | Manufacturer                       |
| Changes?    | Yes                              | Usually No                         |
| Layer       | Network Layer (Layer 3)          | Data Link Layer (Layer 2)          |
| Example     | 192.168.1.10                     | 00-1A-2B-3C-4D-5E                  |

### Easy Analogy

* **IP Address = Home address**
* **MAC Address = Person's fingerprint**

---

## 3️⃣ What Happens When You Open a Website?

Let's say you open:

```text
https://google.com
```

The process looks like this:

```text
Laptop → Switch/Wi-Fi → Router → ISP → Internet → Google Server
```

Your laptop knows Google's IP address using DNS.

But before sending data to the router, your laptop must know:

> "What is my router's MAC address?"

This is where ARP comes in.

---

## 4️⃣ Understanding ARP (Address Resolution Protocol)

ARP translates:

```text
IP Address → MAC Address
```

Example:

```text
192.168.1.1 → AA-BB-CC-DD-EE-FF
```

### ARP Process

1. Your laptop wants to communicate with the router.
2. It checks its ARP cache.
3. If no entry exists, it sends an ARP broadcast:

```text
Who has 192.168.1.1?
```

4. The router replies:

```text
192.168.1.1 is AA-BB-CC-DD-EE-FF
```

5. Your laptop stores this information temporarily.

---

## 5️⃣ Types of Communication

![Image](https://images.openai.com/static-rsc-4/UspD0yhep5lZydRWCFORVGxL6OmXDnJgt_-7o_lvziE13_a1RPcOxeb-g6mMvgVDKxx1HtdS9KD3vBWM5_y6021ED8TCqEavgxiMwvX-lPIOlT233kkzi0AI2U0gidWvbKYf5FkAd__gJPUlDyarPnIPheg8S78a_OmbNFg63DyYbvMdFHs5VJDdnCBy7BM2?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/CdnvcDsoglsOA8Z-KmTux45trymv6UD0-fLzcOkCasGiIpbhNP8_yXw-a-PNrOSxBkEb_lqUbSUURP7L8ZSc8zGsYw9lGi6Lb1PLdfOADFCY6nvduwhmZKzKwIp3eSlVU12nSa8uxfSg2l7tytrBH4k6R9UpzC9pZv_FDa6wc93clLKDMSouinoJM0CK2l9w?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/f3fRkCT-0CWHphR-UrKu-pk8EBWSxL3qJNk8nNLISHaXz96C1ecspmtFLdAK_qKmIhfvBr7PEnWSHXUwwHg18lu62pYbX-jg4fe7z0MPf93ASr7lL3z1Pk6zC54b3UBTSoQpRpKz6uqqKLy5eBJ4VcCC56gT5sVJCNwUXwp2kvwJKUS9bwLK_PC4hXzxWMrJ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pZOFPx3DNoXZ7nJu0TBa3pT5PzBQGpf4QhldgRy56hHQ_npBiOc-04McOJGfB925Oj37hrB2tilVm6XEVJo7OF651PQc7_uyq0a6Iv-RZ53OB_osT99hF8-oZG4_UkY0P2d2M-PIM7Vu3Pn-0oWG4leAEL6txhSaA_t-dIv4I-G9ilrfRk86g7HBIWQkNuts?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/yNuhC_NTQ_UzZo_-XiAy1zeUWpH3sUtPRJuBWNpYcJP10dqFpJ1fHLiEc7p4vrhlLNvXGcJBwBSJ5Yij0fpnSSsbabTsOtrdtXcY7m1IoeTPGx-WFaL7dUmRj6JO3rQUKJQCOfOFSEx211V2y-h_wOYVyXVGOVsPOFN5hraJEjCCNAS9sOkL3UBh4VY0cwgf?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Fdq5zHT_8JB1sZm1LNxuLtAGGhqBaTiCqORVVgXdUrX2Aemv8luYOnBbEMeWvO9Cvwy08K9jw6d27j8amrmMzF7hDxG2F-h01xR-l0nGEpx7guyThtnjtjEH979CWoa8AtwY19LBjAJSTAMqS0QzQ8bolG9lLpIov0SYASMZT2frgBrsK5chZlwrKyCMmG8f?purpose=fullsize)

### Unicast

One sender → One receiver

Example:

* Opening a website

---

### Broadcast

One sender → All devices in the network

Example:

* ARP request

---

### Multicast

One sender → Multiple selected receivers

Examples:

* Live video streaming
* Online meetings

---

## 6️⃣ Setup Environment

Open **Command Prompt as Administrator**.

You will use these commands throughout your networking journey.

---

## 7️⃣ Hands-On Practice (60 Minutes)

### Step 1: Find your MAC address

Run:

```cmd
getmac
```

OR:

```cmd
ipconfig /all
```

Look for:

```text
Physical Address
```

Example:

```text
00-1A-2B-3C-4D-5E
```

---

### Step 2: View your ARP table

Run:

```cmd
arp -a
```

Example output:

```text
Internet Address      Physical Address      Type
192.168.1.1           aa-bb-cc-dd-ee-ff     dynamic
```

This shows the IP-to-MAC mappings your system already knows.

---

### Step 3: View your routing table

Run:

```cmd
route print
```

Look for:

```text
0.0.0.0
```

This represents your **default route**.

You should see your default gateway IP address.

---

### Step 4: Clear the ARP cache

Run:

```cmd
arp -d *
```

Now test connectivity:

```cmd
ping 8.8.8.8
```

Check the ARP table again:

```cmd
arp -a
```

Notice how new entries are created automatically.

---

## 8️⃣ Mini Task (30 Minutes)

Create the following table in your notes:

| Parameter           | Value |
| ------------------- | ----- |
| IPv4 Address        |       |
| MAC Address         |       |
| Default Gateway     |       |
| Gateway MAC Address |       |

Answer these questions:

1. Why do we need both IP and MAC addresses?
2. Which protocol converts an IP address into a MAC address?
3. Which communication type does ARP use?
4. What is the purpose of the default gateway?

---

## 9️⃣ What You Learned Today

* Difference between IP address and MAC address
* How devices communicate within a network
* What ARP does
* How unicast, broadcast, and multicast work
* How to view ARP and routing tables

---

## 🔟 Homework

Draw this communication flow in your notebook:

```text
Your Laptop → Router → ISP → Internet → Website Server
```

Label:

* Source IP
* Destination IP
* Source MAC
* Destination MAC

Try explaining the process aloud in your own words.

If you can explain it simply, you've understood it.

---

### Tomorrow – Day 3

We will learn the most important networking topic for interviews and DevOps:

* OSI Model
* Seven layers explained simply
* Real-world examples
* Troubleshooting using OSI layers

Just come back and type:

**"Day 3 Networking study"** 🚀
