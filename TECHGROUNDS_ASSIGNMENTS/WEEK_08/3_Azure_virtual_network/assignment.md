# [3/ Azure Virtual Network]

Azure virtual networks (VNets) ensure that resources such as VMs, web apps, and databases can communicate with each other, with users on the internet, and with on-premises machines.

VNets have the following responsibilities:

- (Network) isolation and segmentation

- Internet communication

- Communication between Azure resources

- Communication with on-premises resources

- Routing of network traffic

- Filtering of network traffic

- Connecting to other VNets

When you create a new VNet, you determine a private IP range for your network. Within that range, you can create subnets.

There are three ways to connect your network to an on-premises network:

- Point-to-site VPNs:
  
  - The Azure VNet is accessed with a VPN from an on-premises computer.

- Site-to-site VPNs:
  
  - The on-premises VPN device or gateway is connected to the Azure VPN Gateway, effectively creating one large local network.

- Azure ExpressRoute:
  
  - This is a physical connection from your local environment to Azure.

You can also connect two Azure VNets to each other using virtual network peering. This is facilitated by user-defined Routing (UDR). Peering is possible with VNets in different regions.

An easy way to find out how traffic is routed is to look at a NIC under "effective routes". This shows the routes and the route tables associated with those routes.



### WHY?

- **<u>WHY WOULD YOU USE VPN IN AZURE?</u>**
  Using a VPN (Virtual Private Network) in Azure can serve several purposes, including:
1. **Secure Connectivity**: VPNs provide a secure connection between your on-premises network and Azure Virtual Network. This encrypted tunnel ensures that data transmitted between your on-premises environment and Azure resources remains secure and protected from unauthorized access or interception.

2. **Hybrid Cloud Connectivity**: Many organizations have a hybrid cloud setup, with some resources hosted on-premises and others in the cloud. VPNs enable seamless communication and integration between on-premises resources and Azure resources, allowing for a unified network environment.

3. **Remote Access**: Point-to-site VPNs allow individual devices or remote users to securely access Azure resources from outside the corporate network. This is particularly useful for employees working remotely or accessing resources while traveling.

4. **Site-to-Site Connectivity**: Site-to-site VPNs establish a secure connection between your on-premises data center and Azure, enabling communication between all resources as if they were on the same network. This facilitates data transfer, application access, and other interconnectivity needs between your on-premises infrastructure and Azure resources.

5. **Compliance and Regulatory Requirements**: VPNs help organizations meet compliance and regulatory requirements by ensuring data transmitted between on-premises and cloud environments is encrypted and secure. This is especially important for industries with strict data protection regulations, such as healthcare, finance, and government sectors.

6. **Cost-Effective Connectivity**: VPNs can be a cost-effective solution for establishing connectivity between on-premises and cloud environments compared to other options like Azure ExpressRoute, especially for smaller organizations or those with limited bandwidth requirements.

Overall, using VPNs in Azure provides a flexible and secure way to connect your on-premises infrastructure with Azure resources, enabling hybrid cloud scenarios, remote access, and meeting security and compliance needs.

## Key-terms

**Azure Virtual Networks (VNets)**: Azure Virtual Networks allow you to create isolated and secure networks within the Azure cloud infrastructure. They enable you to logically isolate resources, control IP address ranges, subnets, and route tables, and securely connect Azure resources and on-premises networks.

- 2. **Point-to-site VPNs**: Point-to-site VPN (Virtual Private Network) in Azure enables you to connect individual devices or clients to an Azure virtual network over the internet. It provides secure access to resources hosted in Azure from remote locations.

- 3. **Site-to-site VPNs**: Site-to-site VPN allows you to establish a secure connection between your on-premises network and an Azure virtual network. It enables seamless and secure communication between your on-premises infrastructure and resources deployed in Azure.

- 4. **Azure ExpressRoute**: Azure ExpressRoute is a dedicated private connection between your on-premises network and Microsoft Azure or Office 365. It offers higher security, reliability, and faster speeds compared to connections over the public internet. ExpressRoute enables private connectivity that doesn't go over the public internet.

- 5. **(Network) isolation and segmentation**: This refers to the ability to create isolated environments within Azure Virtual Networks to enhance security and control. It allows you to segment your network into multiple subnets and control traffic flow between them using Network Security Groups (NSGs) and route tables.

- 6. **Internet communication**: This refers to the ability of Azure resources to communicate with the internet. By default, Azure resources deployed within a virtual network can communicate with the internet unless outbound access is restricted using Network Security Groups or other methods.

- 7. **Communication between Azure resources**: Azure resources within the same virtual network can communicate with each other by default, provided there are no restrictions imposed by NSGs or other network security configurations.

- 8. **Communication with on-premises resources**: Azure resources can communicate with on-premises resources via site-to-site VPNs, point-to-site VPNs, or Azure ExpressRoute connections, depending on the network architecture and requirements.

- 9. **Routing network traffic**: Routing network traffic involves directing data packets between different networks or subnets based on routing rules and configurations. Azure provides various tools and services to manage and configure routing, such as route tables and Azure Virtual Network Gateways.

- 10. **Filtering network traffic**: Filtering network traffic involves controlling and monitoring the flow of data packets within your Azure network. This can be achieved using Network Security Groups (NSGs), which allow you to define inbound and outbound security rules to filter traffic based on source/destination IP addresses, ports, and protocols.

- 11. **Connecting to other VNets**: Azure VNets can be connected to each other either directly or through Azure Virtual Network Peering. This enables resources in one VNet to communicate securely with resources in another VNet, facilitating network integration and communication across multiple Azure environments.

- 12. **NIC: "effective routes"**: NIC stands for Network Interface Card, which is a virtual or physical network adapter used by Azure VMs to communicate over the network. "Effective routes" refer to the routing table associated with a NIC, which determines how network traffic is routed to and from the VM.

- 13. **Route tables**: Route tables in Azure VNets are used to control the flow of traffic within the virtual network. They contain a set of rules, called routes, that specify how network traffic should be directed. Route tables are associated with subnets and can be used to route traffic within the VNet, between VNets, or to on-premises networks.

- 14. **User-defined Routing (UDR)**: User-defined Routing (UDR) in Azure refers to the capability to define custom routing rules for directing traffic within virtual networks. By default, Azure automatically handles the routing of traffic between subnets within a virtual network. However, with UDR, you can override these default routes and specify your own routing preferences. This allows for more granular control over network traffic flow, enabling you to route traffic through specific network appliances or services.

- 15. **Peering**: In the context of Azure Virtual Networks, peering refers to establishing a network connection between two virtual networks (VNets) either within the same Azure region (intra-region peering) or across different Azure regions (inter-region peering). This connection enables resources in the peered VNets to communicate with each other as if they were part of the same network. Peering can help in simplifying network architecture, improving connectivity between resources, and facilitating resource sharing across different VNets.

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