Unsafe Network Design:

Internet

|

[Router]

|

[Switch]

/ | \

WS WS WS

| | 
\

Printer AD Server

|

File Server

|

Database

|

Web Server

In an unsafe network
design, we'll disregard best practices for security and create a
setup that leaves the network vulnerable to various threats.

1. **Single Flat
   Network**:

We'll set up a
single flat network without any segmentation or access controls.

2. **IP Range**:

Assign all
devices to the same IP range (e.g., 192.168.1.0/24).

3. **Connectivity**:
- All devices
  connect directly to a switch, which then connects to a single router
  for internet access.

- No VLAN
  segregation or subnetting is implemented.
4. **No Firewall**:
- There's no
  dedicated firewall in place to monitor or control traffic between
  devices.
5. **No
   Encryption**:
- Data
  transmission between devices is not encrypted, leaving it susceptible
  to interception.
6. **No Access
   Control**:
- All devices
  have unrestricted access to each other, increasing the risk of
  unauthorized access.
7. **No Intrusion
   Detection/Prevention Systems (IDS/IPS)**:
- Without these
  systems, there's no proactive monitoring or defense against potential
  attacks.
8. **No User
   Authentication**:
- No user
  authentication mechanisms are implemented, leaving resources
  vulnerable to unauthorized access.
9. **No Patch
   Management**:
- Devices are not
  regularly updated with security patches, leaving them vulnerable to
  known exploits.
10. **No Backup
    Strategy**:
- There's no
  backup strategy in place, making it difficult to recover from data
  loss or system compromises.
  
  ![network_webstore.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\00_includes\WEEK_03_screenshots\5_Networking_case_study\network_webstore.png)

---

SAFE Network Design:

*

For a safer network
design, we'll implement segmentation, access controls, and firewall
configurations.

1. **Subnets**:
- Web Server
  subnet

- Database subnet

- Workstation
  subnet

- Server subnet
  (AD server and file server)
2. **Firewall
   Configuration**:
- **Web Server
  Subnet**:

- Allow
  incoming HTTP (port 80) and HTTPS (port 443) traffic.

- Restrict all
  other inbound and outbound traffic.

- **Database
  Subnet**:

- Only allow
  incoming traffic on the port used for database connections (e.g.,
  port 3306 for MySQL).

- Restrict all
  other inbound and outbound traffic.

- **Workstation
  Subnet**:

- Allow
  outgoing HTTP, HTTPS, and DNS traffic.

- Restrict
  incoming traffic to necessary services like SSH for remote
  administration.

- Block
  incoming traffic from external sources unless explicitly allowed for
  specific purposes.

- **Server
  Subnet**:

- Allow incoming
  traffic for Active Directory services (e.g., LDAP, Kerberos)

KERBEROS

**-
TCP/UDP 88**: This is the default port for Kerberos
authentication traffic. It's used for communication between the
Kerberos client and the Kerberos KDC (Key Distribution Center). This
port is used for the initial authentication process and subsequent
ticket requests.

**-** **TCP/UDP 464**: This port is used for
the Kerberos Change/Set Password Protocol. It's used for changing or
setting passwords within the Kerberos realm.

LDAP

LDAP (Lightweight Directory Access Protocol) primarily operates
over TCP, and the default port it uses is:

- **TCP
   389**: This is the standard port for LDAP non-secure
   communication. It's used for querying and modifying directory
   services data.

Additionally,
for LDAP over SSL/TLS (LDAPS), the default port is:

- **TCP
   636**: This port is used for LDAP communication
   secured by SSL/TLS encryption.

- Allow necessary
  file sharing protocols (e.g., SMB for Windows, NFS for Linux).
1. **SMBv2
   and later**:
   
   - Port 445
     (TCP/UDP): This is the default port for SMB file sharing in modern
     implementations, including SMBv2 and SMBv3. It's used for direct
     host-to-host communication and doesn't rely on NetBIOS.

**2.** **NFSv4**:

- Port 2049
   (TCP/UDP): NFSv4 also primarily uses port 2049. However, NFSv4 has
   additional features and uses various other ports for specific
   purposes, such as mounting, locking, and callback.

- Restrict all
  other inbound and outbound traffic.
3. **Access
   Control**:
- Implement
  role-based access control (RBAC) to restrict access to sensitive
  resources based on user roles and permissions.
4. **Encryption**:
- Use protocols
  like HTTPS for web traffic, SSH for remote administration, and VPNs
  for secure remote access.
5. **Intrusion
   Detection/Prevention Systems (IDS/IPS)**:
- Deploy IDS/IPS
  systems to monitor network traffic and detect/prevent suspicious
  activities.
6. **User
   Authentication**:
- Enforce strong
  password policies.

- Implement
  multi-factor authentication (MFA) for added security.
7. **Patch
   Management**:
- Establish
  regular patching schedules to ensure all devices are up-to-date with
  security patches.
8. **Backup
   Strategy**:
- Implement regular
  backups of critical data and systems to ensure quick recovery in case
  of data loss or system compromises.

Certainly! Here's a
more detailed design of the safe network with four subnets, along
with their CIDR notation:

```
SAFE Network Design:
              +--------------------------------------+
              |                Internet              |
              +-----------------|--------------------+
                                |
              +-----------------|--------------------+
              |             Router/Firewall          |
              +-----------------|--------------------+
                                |
+--------------------------+----------------+---------------------+------------------------+
|                          |                         |            |                        |
+--------+-----------+     +-------+--------+ +------+----------+ +------+----------+ +--------+
|    DMZ Subnet      |     |    Web Server  | | Database Subnet | |   Internal LAN| | Printers |         
| (Public-Facing)    |     +----------------+ +-----------------+ +-----------------+ +--------+
|     192.168.10.0/24|     192.168.10.10                            192.168.20.0/24       
+---------------------+
              |                  |                                               |
              +------------------|-----------------------------------------------+
                                 |
              +------------------+-------------------------+
              |                   Router/Firewall          |
              +------------------+-------------------------+
                                 |
  +---------------+-------------------+---------+--------------------+---------------------------------+
  |                    |                 |                   |                |
  +------+-----++-----+---------++-----+--------++-----+--------++-----+-------++-------------+
  |Workstation1|| Workstation5  ||   AD Server  || File Server  ||   Printer   ||File Server  |
192.168.30.0/24||192.168.30.0/24|| 192.168.30.10|| 192.168.40.10||192.168.30.20||192.168.30.30|
  +------------++---------------++-----+--------++-----+--------++-------------++-------------+
                                        |                      |       |
                                        +------+---------+     |      +------+----------------------+
                                        |                |     |       |                    |
                                +-------+-----+  +-------+----+|   +--+-----+----------+  +------+--------+
                                | File Server |  | Database   ||   |Web Application    |    |  Management |
                                | Backup      |  | Replica    ||   |Server             |  |  System         |
                                |192.168.40.0 |  |192.168.40.5||   |192.168.40.20     |  |192.168.40.30  |
                                +-------------+  +------------+|   +--------------------+ +-----------------+
                                                               |
                                                       +----+----------+
                                                       |Backup         |
                                                       |Database       |
                                                       |192.168.40.40  |
                                                       +---------------+
For a safer network design, we'll implement segmentation, access controls, and firewall 
configurations.
1. **Subnets**:
   - Web Server subnet
   - Database subnet
```

In this detailed
design:

1. **DMZ Subnet
   (192.168.10.0/24)**: This subnet houses the public-facing services
   like the Web Server.

2. **Database Subnet
   (192.168.20.0/24)**: Isolates the database server, allowing only
   necessary traffic from the Web Server.

3. **Internal LAN
   (192.168.30.0/24)**: This is where office workstations, servers, and
   printers reside.

4. **Backup Subnet
   (192.168.40.0/24)**: Hosts backup servers for file server and
   database systems.

The CIDR notations
for the subnets are as follows:

- DMZ Subnet:
  192.168.10.0/24

- Database Subnet:
  192.168.20.0/24

- Internal LAN:
  192.168.30.0/24

- Backup Subnet:
  192.168.40.0/24

Each subnet is
appropriately segmented and secured. Traffic between subnets is
controlled by the firewall/router, enforcing security policies to
allow only necessary communication.