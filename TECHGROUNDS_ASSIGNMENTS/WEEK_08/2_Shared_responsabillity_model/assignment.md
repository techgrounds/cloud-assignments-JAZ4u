# [2/ Shared responsabillity model]

Since all resources in the cloud are always online, it's important to protect them against both intentional and unintentional harmful traffic. Azure Firewall can protect VNets against this traffic.

You can use the Firewall in different configurations within a subnet, or in a hub-and-spoke network. A Firewall always has a public IP address where all incoming traffic should be directed. And a private IP address where all outgoing traffic should be directed.

As you've previously learned, there are two types of firewalls: stateless and stateful. Azure Firewall is a stateful firewall.

Because Azure Firewall monitors all traffic in detail, it is a relatively expensive service. During the training, we won't use Azure Firewall, but the cheaper variant: Network Security Group (NSG).

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Study:

- The difference between Basic and Premium Firewall.

- The difference between a Firewall and a Firewall Policy.

- That Azure Firewall is much more than just a firewall.

- The difference between Azure Firewall and NSG.
  
  Task:
  Turn on a web server. Ensure that the ports for both SSH and HTTP are open.
  Create an NSG in your VNET. Ensure that your web server is still accessible via HTTP, but that SSH is blocked.
  Test if your NSG works.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

Study:

1. **The difference between Basic and Premium Firewall**:
   
   - Basic Firewall provides essential network security features for simple security requirements, while Premium Firewall offers advanced capabilities such as threat intelligence-based filtering, TLS inspection, and application-level filtering.

2. **The difference between a Firewall and a Firewall Policy**:
   
   - A firewall is a network security device or software that monitors and controls incoming and outgoing network traffic. A firewall policy, on the other hand, is a set of rules and configurations that dictate how a firewall should handle network traffic.

3. **That Azure Firewall is much more than just a firewall**:
   
   - Azure Firewall provides not only traditional firewall capabilities but also advanced features like application-level filtering, URL filtering, threat intelligence-based filtering, and integration with other Azure services for comprehensive network security.

4. **The difference between Azure Firewall and NSG**:
   
   - Azure Firewall is a fully managed, cloud-based network security service that operates at the application and network layer, providing centralized network security policy enforcement. NSG (Network Security Group) is a basic network security feature in Azure that acts as a distributed firewall for controlling traffic to and from Azure resources within a VNet.
- Task:
  
  1. **Turn on a web server. Ensure that the ports for both SSH and HTTP are open**:
     
     - First, deploy a virtual machine (VM) or an Azure App Service to host your web server.
     - Configure the VM's network security group (NSG) or the Azure App Service's network settings to allow incoming traffic on ports 22 (SSH) and 80 (HTTP).
  
  2. **Create an NSG in your VNET. Ensure that your web server is still accessible via HTTP, but that SSH is blocked**:
     
     - Create a new NSG in the same virtual network (VNet) where your web server resides.
     - Configure inbound security rules in the NSG to allow traffic on port 80 (HTTP) and block traffic on port 22 (SSH).
     - Associate the NSG with the subnet containing your web server.
  
  3. **Test if your NSG works**:
     
     - Access your web server using a web browser to ensure that HTTP traffic is still allowed.
     - Attempt to SSH into your web server from a remote location to verify that SSH traffic is blocked.