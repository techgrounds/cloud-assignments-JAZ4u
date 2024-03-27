# [4\ Subnetting]

Een netwerk is gedefinieerd als twee of meer devices die met elkaar verbonden zijn zodat ze data kunnen uitwisselen. Een Local Area Network (LAN) wordt vaak uitgedrukt als een range aan IP addresses. Elk device (host) krijgt een eigen adres binnen die range.

Om dit te ondersteunen hebben netwerken een subnet mask (prefix) die definieert hoeveel bits van het IP adres onderdeel uitmaken van het netwerkadres, en hoeveel bits gereserveerd zijn voor de host.

Een subnet is een kleiner netwerk dat onderdeel is van een groter netwerk. Subnets kunnen worden gebruikt om een deel van het netwerk logisch te isoleren. Een subnet heeft per definitie een grotere prefix dan het netwerk waar het subnet in zit.

Om dit alles leesbaar te maken voor mensen maken we gebruik van CIDR notation.

# Key-terms

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
  
  

- CIDR notation
  
  CIDR notation, which stands for Classless Inter-Domain Routing notation, is a compact representation of an IP address and its associated network prefix. It's used to specify a range of IP addresses and their subnet masks in a concise format.
  
  In CIDR notation, an IP address is followed by a slash ("/") and a number representing the number of significant bits in the network prefix. This number indicates the number of bits that are fixed for the network portion of the IP address.
  
  For example:
  
  - `192.168.1.0/24`: This represents the IPv4 address range from `192.168.1.0` to `192.168.1.255`, where the first 24 bits (the first three octets) represent the network portion, and the last 8 bits (the fourth octet) represent the host portion.
  
  - `2001:0db8:85a3::/48`: This represents the IPv6 address range from `2001:0db8:85a3:0000:0000:0000:0000:0000` to `2001:0db8:85a3:ffff:ffff:ffff:ffff:ffff`, where the first 48 bits represent the network portion, and the remaining bits represent the host portion.
  
  CIDR notation is commonly used in networking for routing purposes, as it allows for more flexible allocation of IP addresses compared to the traditional class-based IP addressing (Class A, B, and C) which had fixed subnet masks associated with each class. With CIDR notation, networks can be subdivided into smaller or larger subnets as needed, providing more efficient use of IP address space.
  
  

- ## Opdracht

- Maak een netwerkarchitectuur die voldoet aan de volgende eisen:

  - 1 subnet dat alleen van binnen het LAN bereikbaar is. Dit subnet moet minimaal 15 hosts kunnen plaatsen.

  - 1 subnet dat internet toegang heeft via een router met NAT-functionaliteit. Dit subnet moet minimaal 30 hosts kunnen plaatsen (de 30 hosts is exclusief de router).

  - 1 subnet met een network gateway naar het internet. Dit subnet moet minimaal 5 hosts kunnen plaatsen (de 5 hosts is exclusief de internet gateway).

- Plaats de architectuur die je hebt gemaakt inclusief een korte uitleg in de Github repository die je met de learning coach hebt gedeeld.

- Zie hier een voorbeeld van hoe je een netwerkarchitectuur kan visualiseren:
![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/b5c66c5ee828179643b0a492b59ae637.png)

### Gebruikte bronnen

- [Beer:30 - Network Architecture Review - YouTube](https://www.youtube.com/watch?v=oopkClg1kxM)
- https://www.calculator.net/ip-subnet-calculator.html

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Resultaat

Opdracht:

- Maak een netwerkarchitectuur die voldoet aan de volgende eisen:

  - 1 subnet dat alleen van binnen het LAN bereikbaar is. Dit subnet moet minimaal 15 hosts kunnen plaatsen.

  - 1 subnet dat internet toegang heeft via een router met NAT-functionaliteit. Dit subnet moet minimaal 30 hosts kunnen plaatsen (de 30 hosts is exclusief de router).

  - 1 subnet met een network gateway naar het internet. Dit subnet moet minimaal 5 hosts kunnen plaatsen (de 5 hosts is exclusief de internet gateway).

- Plaats de architectuur die je hebt gemaakt inclusief een korte uitleg in de Github repository die je met de learning coach hebt gedeeld.

- Zie hier een voorbeeld van hoe je een netwerkarchitectuur kan visualiseren:
![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/b5c66c5ee828179643b0a492b59ae637.png)
