# **S3**

* Web Hosting
* Redirection
* EBS -> S3 ? 

* Size => Unlimited size limit ; 5TB is maximum for a file ; as a student 5GB is free for 1 year ; It is region independent
* Bucket => Like a folder; and bucket should be unique globally
---

# **NAAS (Network As a Service)**
* Give same environment of network to another place which is originally is at different place

**Types:-**
---
* VPC
* Route53

**Need to understand these before understanding NAAS:-**
* IP 
* NetMask -> IP with NetMask is IP Address
* SubNet -> Dividing 4th part of IP into different parts equally
* Gateway
* DNS
* Router
* Switch
* DHCP (Dynamic Host Configuration Protocol)
* Firewall
* NAT (Network address translation)
* Routing Table

## IP Address:-

There are 4 parts :-    **-.-.-.-**
* Network Name is First 3 parts of IP Address
* if 1st part is 0-127 (Class A) then Netmask is always 255.0.0.0
* if 1st part is 128-191 (Class B) then Netmask is always 255.255.0.0
* if 1st part is 192-223 (Class C) then Netmask is always 255.255.255.0

**Prefix Length ->** IP-> 192.168.1.10 , Adding binary no of Netmask (255.255.255.0) -> 11111111.11111111.11111111.00000000 -> 192.168.1.10/24 => here 24 is prefix length (adding binary no's). Used for short forming Subnet instead of 255.255.255.0 we write "/24"

# **VPC (Virtual Private Cloud)**

Whenever we create a VPC, these are automatically created
* Router
* Security Group
* ACL
* Route Table


* 192.168.0.0/16 => 2 power (16) => 65536 connections

Amazon bydefault reserve these 5 IP's after creating a Subnet in VPC => 192.168.1.0(Network IP), 1.1(Gateway), 1.2(DNS), 1.3(Future), 1.255(Breadcast)

0.0.0.0/0 => Anywhere in this world (Route Table)