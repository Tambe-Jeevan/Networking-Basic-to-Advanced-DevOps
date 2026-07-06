Day 5 – IPv4 Addressing 🌐

As a DevOps engineer, you will constantly be architecting networks in the cloud (AWS VPCs, Azure VNETs). To do this securely, you absolutely must know the difference between Private and Public IP addresses.

🧠 1️⃣ Concept (30 minutes)

An IPv4 address is a 32-bit number, formatted as four numbers separated by dots (e.g., 192.168.1.10).

Because there are only about 4.3 billion possible IPv4 addresses, we ran out of them years ago. To solve this, engineers split IP addresses into two distinct categories:

1. Private IPs (For LANs / Internal VPCs)

These addresses are free to use, but they cannot route over the internet.
Every home, office, and cloud VPC uses these exact same IP ranges internally.
There are three standard ranges reserved exclusively for Private use (known as RFC 1918):

Class A: 10.0.0.0 – 10.255.255.255 (Massive networks, standard for Cloud VPCs)

Class B: 172.16.0.0 – 172.31.255.255 (Medium networks, Docker containers default to this)

Class C: 192.168.0.0 – 192.168.255.255 (Small networks, standard for home Wi-Fi routers)

DevOps Rule: Database servers and backend API servers should always be assigned Private IPs so hackers on the internet cannot reach them directly.

2. Public IPs (For WAN / Internet)

These are globally unique and cost money. They are reachable directly from anywhere on the internet.
Any IP address that does not fall into the three Private ranges above is generally considered a Public IP.

Examples: 8.8.8.8 (Google), 142.250.190.46 (Google), 54.210.X.X (AWS EC2 instances)

How do Private IPs access the Internet? NAT!

If a Private IP cannot route over the internet, how are you reading this on your private 192.168.x.x laptop?
Through Network Address Translation (NAT).
Your home router has two IP addresses. An internal Private one, and an external Public one assigned by your ISP. When your laptop asks for a webpage, the router intercepts the packet, erases your private IP, stamps its own Public IP on it, and sends it to the internet. When the reply comes back, it reverses the process.

(You will use NAT Gateways extensively in AWS to let your private servers download security updates).

💻 2️⃣ Hands-on Practice (60 minutes)

Let's investigate your own network to see this dual-IP setup in action.

Step A: Find your Private IP

Open your terminal/command prompt:

ipconfig


(Look for your "IPv4 Address". It will almost certainly start with 192.168. or 10., proving it is private).

Step B: Find your Public IP

Since this IP belongs to your router (or your company's firewall), ipconfig cannot see it. We have to ask an external server what IP it sees us coming from.

Open a web browser and go to:
https://whatismyipaddress.com
OR, for a DevOps approach, use curl in your terminal:

curl ifconfig.me


This returns the Public IP assigned to your home by your ISP.

🎯 3️⃣ Mini Task (30 minutes)

Review the following 5 IP addresses. Based on the ranges you learned today, categorize them as Public or Private, and explain where they are typically used.

10.0.5.50

8.8.8.8

192.168.1.254

54.120.30.5

172.17.0.2

(Write your answers down in your notes!)

🏁 Wrap Up

Understanding the 10.x.x.x vs 192.x.x.x distinction is massive. When you spin up an EC2 instance in AWS, you will put it in a private 10.x network for security, and attach an Elastic IP (Public IP) to a Load Balancer so the public can access it.

Tomorrow is a big one: Subnetting Basics and CIDR notation (the /24 stuff you see everywhere).