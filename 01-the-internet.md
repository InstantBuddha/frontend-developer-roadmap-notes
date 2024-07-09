# 01. The Internet
- [01. The Internet](#01-the-internet)
  - [Protocols](#protocols)
  - [IP](#ip)
  - [IP addresses (IPv4)](#ip-addresses-ipv4)
  - [IPv6](#ipv6)
  - [DNS spoofing](#dns-spoofing)
  - [Routers and packets](#routers-and-packets)
  - [TCP](#tcp)

Notes from here: [roadmap.sh what is the internet](https://roadmap.sh/guides/what-is-internet)
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

## TCP

TCP manages the sending and receiving of all your data as packets.  Think of it like a guaranteed mail service. When you request a song on your device, Spotify  sends a song broken up into many packets.  When your packets arrive, TCP does a full  inventory and sends back acknowledgments of each packet received. If all packets are there, TCP  signs for your delivery and you’re done. The missing packets will be resent.