# [4\ Subnetting]

Een netwerk is gedefinieerd als twee of meer devices die met elkaar verbonden zijn zodat ze data kunnen uitwisselen. Een Local Area Network (LAN) wordt vaak uitgedrukt als een range aan IP addresses. Elk device (host) krijgt een eigen adres binnen die range.

Om dit te ondersteunen hebben netwerken een subnet mask (prefix) die definieert hoeveel bits van het IP adres onderdeel uitmaken van het netwerkadres, en hoeveel bits gereserveerd zijn voor de host.

Een subnet is een kleiner netwerk dat onderdeel is van een groter netwerk. Subnets kunnen worden gebruikt om een deel van het netwerk logisch te isoleren. Een subnet heeft per definitie een grotere prefix dan het netwerk waar het subnet in zit.

Om dit alles leesbaar te maken voor mensen maken we gebruik van CIDR notation.

## Key-terms

- Subnetting
  
  Subnetting is the process of dividing a larger network into smaller, more manageable sub-networks called subnets. It's a fundamental concept in IP networking and is used to optimize network performance, manage network traffic, and conserve IP addresses. Subnetting involves partitioning a single network into multiple smaller networks, each with its own unique subnet address range.
  
  Here's how subnetting works:
  
  1. **IP Address Classes:**
     
     - IPv4 addresses are divided into classes: A, B, and C.
     - Class A addresses have a default subnet mask of 255.0.0.0 (/8 prefix).
     - Class B addresses have a default subnet mask of 255.255.0.0 (/16 prefix).
     - Class C addresses have a default subnet mask of 255.255.255.0 (/24 prefix).
  
  2. **Subnet Masks:**
     
     - A subnet mask is a 32-bit number that defines the network portion and the host portion of an IP address.
     - It consists of a series of consecutive 1s followed by a series of consecutive 0s.
     - The number of 1s in the subnet mask determines the size of the network portion, while the number of 0s determines the size of the host portion.
  
  3. **Subnetting Process:**
     
     - To subnet a network, you borrow bits from the host portion of the IP address to create additional subnet bits.
     - By borrowing bits, you create smaller subnets with fewer host addresses per subnet.
     - The number of bits borrowed determines the number of subnets and hosts per subnet.
     - The subnet mask is adjusted accordingly to reflect the new subnet structure.
  
  4. **Benefits of Subnetting:**
     
     - Efficient Utilization of IP Addresses: Subnetting allows for more efficient use of IP address space by dividing a larger network into smaller, more manageable subnets.
     - Improved Network Performance: Smaller subnets can reduce network congestion and improve performance by limiting broadcast domains and controlling traffic flow.
     - Enhanced Security: Subnetting helps improve network security by isolating different parts of the network and controlling access between subnets using routers and access control lists (ACLs).
  
  5. **Subnetting Examples:**
     
     - For example, if you have a Class C network (e.g., 192.168.1.0) and you want to create four subnets, you would borrow two bits from the host portion of the IP address. This would result in four subnets with subnet masks of 255.255.255.192 (/26 prefix), each containing 62 usable host addresses.
  
  Overall, subnetting is a crucial aspect of IP networking that enables efficient address allocation, improved network performance, and enhanced security in large-scale networks.

- NAT
  
  NAT stands for Network Address Translation. It's a method used in computer networking to modify network address information in the IP header of packets while they are in transit across a traffic routing device.
  
  The primary purpose of NAT is to conserve IP addresses. In the early days of the internet, IP addresses were a finite resource, and NAT allowed multiple devices within a private network to share a single public IP address. This is achieved by translating the private IP addresses of devices within the local network to a single public IP address when they communicate with devices outside of the local network, and vice versa.
  
  NAT comes in different types, including:
  
  1. **Static NAT:** In this type, a one-to-one mapping is established between a private IP address and a public IP address. It's typically used when a device within the local network needs to be accessible from the internet.
  
  2. **Dynamic NAT:** With dynamic NAT, the translation of private IP addresses to public IP addresses is done dynamically as needed. A pool of public IP addresses is usually configured, and they are assigned to devices on a first-come, first-served basis.
  
  3. **NAT Overload (PAT - Port Address Translation):** This is also known as NAT with Port Address Translation (PAT). In PAT, multiple private IP addresses are mapped to a single public IP address, differentiating them by using unique port numbers. This is the most common form of NAT used in home and small office networks.
  
  NAT provides a level of security by hiding the internal IP addresses of devices from the external network, acting as a barrier between the internal network and the internet. However, it can sometimes cause issues with certain types of network traffic, such as peer-to-peer applications or IP-based protocols that embed IP addresses within the data payload.

- CIDR notation
  
  CIDR notation, which stands for Classless Inter-Domain Routing notation, is a compact representation of an IP address and its associated network prefix. It's used to specify a range of IP addresses and their subnet masks in a concise format.
  
  In CIDR notation, an IP address is followed by a slash ("/") and a number representing the number of significant bits in the network prefix. This number indicates the number of bits that are fixed for the network portion of the IP address.
  
  For example:
  
  - `192.168.1.0/24`: This represents the IPv4 address range from `192.168.1.0` to `192.168.1.255`, where the first 24 bits (the first three octets) represent the network portion, and the last 8 bits (the fourth octet) represent the host portion.
  
  - `2001:0db8:85a3::/48`: This represents the IPv6 address range from `2001:0db8:85a3:0000:0000:0000:0000:0000` to `2001:0db8:85a3:ffff:ffff:ffff:ffff:ffff`, where the first 48 bits represent the network portion, and the remaining bits represent the host portion.
  
  CIDR notation is commonly used in networking for routing purposes, as it allows for more flexible allocation of IP addresses compared to the traditional class-based IP addressing (Class A, B, and C) which had fixed subnet masks associated with each class. With CIDR notation, networks can be subdivided into smaller or larger subnets as needed, providing more efficient use of IP address space.

- Subnet Mask
  
  The subnet mask is a 32-bit number used in IPv4 networking to divide an IP address into two parts: the network address and the host address. It is represented in either dotted decimal notation (e.g., 255.255.255.0) or in CIDR notation (e.g., /24).
  
  Here's what the subnet mask does:
  
  1. **Defines the Network Portion:** The subnet mask determines which portion of an IP address identifies the network. Bits set to "1" in the subnet mask represent the network portion, while bits set to "0" represent the host portion.
  
  2. **Determines the Size of the Network:** By altering the number of bits set to "1" in the subnet mask, you can control the size of the network. A larger number of "1" bits creates smaller subnets with fewer host addresses, while a smaller number of "1" bits creates larger subnets with more host addresses.
  
  3. **Identifies the Host Portion:** The portion of the IP address not covered by the subnet mask is used to identify individual hosts within the network. These bits are available for assigning unique addresses to devices within the same subnet.
  
  For example, let's consider the subnet mask 255.255.255.0 (or /24 in CIDR notation). In binary, it looks like this: 11111111.11111111.11111111.00000000. In this subnet mask, the first 24 bits represent the network portion, and the last 8 bits represent the host portion.
  
  So, in the IP address 192.168.1.100 with the subnet mask 255.255.255.0:
  
  - The network portion is 192.168.1.0 (the first 24 bits).
  - The host portion is 0.0.0.100 (the last 8 bits), which identifies the specific host within the network.
  
  Understanding the subnet mask is essential for subnetting, routing, and configuring IP addresses within a network. Different subnet masks can create different-sized subnets, allowing network administrators to efficiently allocate IP addresses based on their network requirements.
  
  ## Opdracht

- Maak een netwerkarchitectuur die voldoet aan de volgende eisen:
  
  - 1 subnet dat alleen van binnen het LAN bereikbaar is. Dit subnet moet minimaal 15 hosts kunnen plaatsen.
  
  - 1 subnet dat internet toegang heeft via een router met NAT-functionaliteit. Dit subnet moet minimaal 30 hosts kunnen plaatsen (de 30 hosts is exclusief de router).
  
  - 1 subnet met een network gateway naar het internet. Dit subnet moet minimaal 5 hosts kunnen plaatsen (de 5 hosts is exclusief de internet gateway).

- Plaats de architectuur die je hebt gemaakt inclusief een korte uitleg in de Github repository die je met de learning coach hebt gedeeld.

- Zie hier een voorbeeld van hoe je een netwerkarchitectuur kan visualiseren:
  ![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/b5c66c5ee828179643b0a492b59ae637.png)

### Gebruikte bronnen

- https://www.calculator.net/ip-subnet-calculator.html

- [subnetting is simple - YouTube](https://www.youtube.com/watch?v=ecCuyq-Wprc)

- https://www.youtube.com/watch?v=aVTEZHC2wdA&t=12s&ab_channel=SunnyClassroom
  
   Subnetting a subnet

- [Subnetting Made Simple - YouTube](https://www.youtube.com/watch?v=nFYilGQ-p-8&ab_channel=CarlOliver)

- [IP Subnetting from CIDR Notations - YouTube](https://www.youtube.com/watch?v=POPoAjWFkGg&ab_channel=JoshuaButcher)

- [What is subnetting ? How subnetting works ? What is subnet mask? | Explained with real-life exmples - YouTube](https://www.youtube.com/watch?v=qulRjRFavJI)

- [Subnetting a Class C IP Address: 192.168.100.154/27 - YouTube](https://www.youtube.com/watch?v=i5jcfbj_TrI)

- [IPv4 Addressing Simplified ➕➖ - YouTube](https://www.youtube.com/watch?v=Hv4epEIP3Mk)

- 

### Ervaren problemen

- IPv4 is explained in different ways 

- The fact that HEXADECIMAL IPv6 adresses are just too much for me to claculate

# Resultaat

Opdracht:

Maak een netwerkarchitectuur die voldoet aan de volgende eisen:

- 1 subnet dat alleen van binnen het LAN bereikbaar is. Dit subnet moet minimaal 15 hosts kunnen plaatsen.

```
    LAN Subnet (Private Subnet):


Subnet Range: 192.168.0.0/28
Beschikbare Hostadressen: 192.168.0.1 - 192.168.0.14
Subnet Mask: 255.255.255.240 (/28)
Dit subnet is alleen bereikbaar van binnen het LAN en kan minimaal 15 hosts plaatsen.
```

-     1 subnet dat internet toegang heeft via een router met NAT-functionaliteit. Dit subnet moet minimaal 30 hosts kunnen plaatsen (de 30 hosts is exclusief de router).

```
NAT Subnet (Private Subnet met NAT-router):

Subnet Range: 192.168.0.16/27
Beschikbare Hostadressen: 192.168.0.17 - 192.168.0.46
Subnet Mask: 255.255.255.224 (/27)
Een router met NAT-functionaliteit verbindt dit subnet met het internet.
Dit subnet heeft internettoegang en kan minimaal 30 hosts plaatsen.
```

-     1 subnet met een network gateway naar het internet. Dit subnet moet minimaal 5 hosts kunnen plaatsen (de 5 hosts is exclusief de internet gateway).

```
Internet Gateway Subnet (Public Subnet):
Subnet Range: Public IP-adres
Beschikbare Hostadressen: Public IP-adres van de internetgateway
Subnet Mask: N/A (afhankelijk van het gebruikte IP-adres)
Deze subnetfunctie omvat de internetgateway die verbinding maakt met het internet.
Het heeft minimaal 5 hosts, die kunnen worden gebruikt voor netwerkapparatuur zoals routers, firewalls, enz.

In deze configuratie fungeert de NAT-router als een barrière tussen de LAN-subnetten en het internet, waarbij het verkeer van de private subnets wordt omgezet naar het publieke IP-adres van de internetgateway. Het LAN-subnet is volledig gescheiden van het internet en alleen bereikbaar vanuit het lokale netwerk, terwijl het NAT-subnet toegang heeft tot internet via de NAT-router. De internetgateway subnet fungeert als de gateway naar het internet en biedt connectiviteit voor het NAT-subnet en eventuele andere externe services.  
```

- Plaats de architectuur die je hebt gemaakt inclusief een korte uitleg in de Github repository die je met de learning coach hebt gedeeld.

```
https://github.com/techgrounds/cloud-assignments-JAZ4u/blob/main/TECHGROUNDS_ASSIGNMENTS/WEEK_03/4_Subnetting/opdracht.md
```
