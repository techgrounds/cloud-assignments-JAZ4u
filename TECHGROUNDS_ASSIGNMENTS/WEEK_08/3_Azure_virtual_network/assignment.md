# [3/ Azure Virtual Network]

Azure virtual networks (VNets) ensure that resources such as VMs, web apps, and databases can communicate with each other, with users on the internet, and with on-premises machines.

VNets have the following responsibilities:

(Network) isolation and segmentation
Internet communication
Communication between Azure resources
Communication with on-premises resources
Routing of network traffic
Filtering of network traffic
Connecting to other VNets
When you create a new VNet, you define a private IP range for your network. Within that range, you can create subnets.

There are three ways to connect your network to an on-premises network:

Point-to-site VPNs:
The Azure VNet is accessed with a VPN from an on-premises computer.
Site-to-site VPNs:
The on-premises VPN device or gateway is connected to the Azure VPN Gateway, effectively creating one large local network.
Azure ExpressRoute:
This is a physical connection from your local environment to Azure.
You can also connect two Azure VNets to each other using virtual network peering. This is facilitated by user-defined Routing (UDR). Peering is possible with VNets in different regions.

An easy way to find out how traffic is routed is to look at a NIC under "effective routes". This shows the routes and the route tables associated with those routes.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Task 1:
Create a Virtual Network with the following requirements:
Region: West Europe
Name: Lab-VNet
IP range: 10.0.0.0/16
Requirements for subnet 1:
Name: Subnet-1
IP Range: 10.0.0.0/24
This subnet should have no route to the internet
Requirements for subnet 2:
Name: Subnet-2
IP Range: 10.0.1.0/24

Task 2:
Create a VM with the following requirements:
An apache server must be installed with the following custom data:

```
#!/bin/bash
sudo su
apt update
apt install apache2 -y
ufw allow 'Apache'
systemctl enable apache2
systemctl restart apache2
```

No SSH access is required, only HTTP
Subnet: Subnet-1
Public IP: Enabled
Check if your website is accessible

### Used sources

- chat-gpt

### Encountered problems

- no problems

### Result

**Task 1: Create a Virtual Network**

1. Go to the Azure portal (https://portal.azure.com).
2. Navigate to "Create a resource" and search for "Virtual Network".
3. Click on "Virtual Network" from the search results, then click "Create".
4. Fill in the following details:
   - Name: Lab-VNet
   - Region: West Europe
   - Address space: 10.0.0.0/16
5. Click "Subnets" and then "Add".
6. Fill in the details for Subnet-1:
   - Name: Subnet-1
   - Address range: 10.0.0.0/24
7. Click "Add" to create Subnet-1.
8. Repeat step 5 and 6 to create Subnet-2 with the following details:
   - Name: Subnet-2
   - Address range: 10.0.1.0/24
9. Ensure that Subnet-1 has no route to the internet by not associating it with a Network Security Group (NSG) that allows internet traffic.

**Task 2: Create a VM**

1. Navigate to "Create a resource" and search for "Virtual machine".

2. Click on "Virtual machine" from the search results, then click "Create".

3. Fill in the necessary details:
   
   - Resource group: Choose an existing resource group or create a new one.
   - Virtual machine name: Choose a name for your VM.
   - Region: West Europe
   - Image: Choose an Ubuntu image.
   - Size: Choose an appropriate size for your VM.
   - Authentication type: Password (enter username and password).
   - Public inbound ports: Select "None".

4. In the "Networking" tab, select "Lab-VNet" as the Virtual Network and "Subnet-1" as the Subnet.

5. Enable the "Public IP" option and leave other settings as default.

6. In the "Management" tab, paste the following custom script into the "Custom data" field:
   
   ```
   #!/bin/bash
   sudo su
   apt update
   apt install apache2 -y
   ufw allow 'Apache'
   systemctl enable apache2
   systemctl restart apache2
   ```

7. Click "Review + create" and then "Create" to provision the VM.

After the VM is provisioned, you can check if your website is accessible by navigating to the public IP address of the VM in a web browser. Since SSH access is not enabled, you won't be able to access the VM via SSH.