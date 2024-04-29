# [4/ ALB&Auto_scaling]

One of the biggest advantages of the cloud is that you don't have to guess how much capacity you need. You can always scale up and down with on-demand services. One of the services that enables this is called Autoscaling.

When running applications with a spiky workload, you can create a VM Scale Set instead of a single server. When the demand for the application is high, Autoscaling can automatically add VMs to your Scale Set. When the demand decreases, it can also remove instances.

To ensure that all VMs are the same, you need to specify an image when configuring a VM Scale Set. You can later modify this image using the reimage option. Auto Scaling utilizes Azure Monitor to determine whether VMs should be added or removed.

In a traditional architecture, a client connects to a single server with a single public IP address. When you have a fleet of servers, this approach no longer works. Therefore, you can use a load balancer as an endpoint for the client. The load balancer will forward the request to one of the servers in your fleet and return the response to the client.

Azure offers two managed solutions for load balancing to a fleet of servers:

Azure Load Balancer: You get this for free with a VM Scale Set. The ALB operates at layer 4 of the OSI stack (TCP/UDP). An ALB can only route to Azure resources.
Application Gateway: This load balancer operates at layer 7 of the OSI stack (HTTP/HTTPS). It also supports features such as SSL termination and Web Application Firewall (WAF). An Application Gateway can route to any routable IP address.

## Key-terms



1. **Azure Autoscaling**: Azure Autoscaling allows you to automatically adjust the number of compute resources (such as virtual machines) in your Azure environment based on predefined conditions or metrics. This helps to ensure optimal performance and cost efficiency by scaling resources up during periods of high demand and down during periods of low demand.

2. **VM Scale Set**: A Virtual Machine Scale Set (VMSS) is an Azure service that allows you to deploy and manage a set of identical virtual machines. VMSS automatically scales the number of VM instances in response to demand or based on predefined scaling rules. This enables you to build and manage large-scale applications with ease, ensuring high availability and scalability.

3. **Azure Monitor**: Azure Monitor is a comprehensive monitoring service that provides insights into the performance and health of your Azure resources and applications. It collects and analyzes telemetry data from various sources, including Azure services, applications, and infrastructure components, allowing you to monitor performance, diagnose issues, and take proactive actions to optimize your Azure environment.

4. **Azure Load Balancer**: Azure Load Balancer is a Layer 4 (TCP/UDP) load balancing service that distributes incoming network traffic across multiple backend resources, such as virtual machines or virtual machine scale sets. It helps to improve the availability and scalability of your applications by evenly distributing incoming traffic and providing high availability through fault tolerance.

5. **SSL termination**: SSL termination refers to the process of decrypting encrypted SSL/TLS traffic at the load balancer or gateway before forwarding it to the backend servers. This allows the backend servers to process the traffic in plain text, reducing the computational overhead of encryption and improving performance. Azure services like Azure Application Gateway and Azure Load Balancer support SSL termination.

6. **Web Application Firewall (WAF)**: Azure Web Application Firewall (WAF) is a security feature that helps protect web applications from common web-based attacks, such as SQL injection, cross-site scripting (XSS), and HTTP header injection. It acts as a reverse proxy, inspecting incoming HTTP requests and responses and filtering out malicious traffic based on predefined security rules. Azure Application Gateway integrates with Azure WAF to provide layer 7 (HTTP/HTTPS) protection for web applications.

7. **Application Gateway**: Azure Application Gateway is a Layer 7 (HTTP/HTTPS) load balancing service that provides advanced traffic management and security features for web applications. It offers features such as SSL termination, URL-based routing, session affinity, and Web Application Firewall (WAF) integration, making it ideal for hosting and scaling web applications with high availability, performance, and security requirements.



## Assignment



Task 1:
Create a Virtual Machine Scale Set with the following requirements:
Ubuntu Server 20.04 LTS - Gen1
Size: Standard_B1ls
Allowed inbound ports:
SSH (22)
HTTP (80)
OS Disk type: Standard SSD
Networking: defaults
Boot diagnostics are not needed
Custom data:

```
#!/bin/bash
sudo su
apt update
apt install apache2 -y
ufw allow 'Apache'
systemctl enable apache2
systemctl restart apache2
```


Initial Instance Count: 2
Scaling Policy: Custom
Number of VMs: minimum 1 and maximum 4
Add a VM at 75% CPU usage
Remove a VM at 30% CPU usage

Task 2:
Check if you can reach the web server via the endpoint of your load balancer.
Perform a load test on your server(s) to activate auto scaling. There may be a delay in creating new VMs depending on the settings in your VM Scale Set. Note: the Azure Load Testing service can be expensive. You can also log in to the VM to perform a manual stress test.

### Used sources

- chat_gpt

### Encountered problems

- no problems

### Result



**Task 1: Create a Virtual Machine Scale Set (VMSS)**

1. Go to the Azure portal (https://portal.azure.com).
2. Click on "Create a resource" and search for "Virtual Machine Scale Set".
3. Click on "Virtual Machine Scale Set" from the search results, then click "Create".
4. Fill in the necessary details:
   - Resource group: Choose an existing resource group or create a new one.
   - Virtual machine scale set name: Enter a name for your VMSS.
   - Region: Choose the desired region.
   - Availability options: Keep the default.
   - Image: Choose "Ubuntu Server 20.04 LTS - Gen1".
   - Size: Select "Standard_B1ls" from the dropdown menu.
   - Authentication type: Choose SSH public key or password and provide the necessary credentials.
   - Inbound port rules: Add SSH (22) and HTTP (80) to the list of allowed inbound ports.
   - OS disk type: Choose "Standard SSD".
   - Networking: Leave the default networking settings.
   - Boot diagnostics: Disable boot diagnostics.
   - Custom data: Paste the provided custom script:
     
     ```
     #!/bin/bash
     sudo su
     apt update
     apt install apache2 -y
     ufw allow 'Apache'
     systemctl enable apache2
     systemctl restart apache2
     ```
   - Initial instance count: Set it to 2.
   - Scaling policy: Choose "Custom".
   - Number of VMs: Set the minimum to 1 and the maximum to 4.
   - Add a VM at 75% CPU usage and remove a VM at 30% CPU usage.
5. Review the configuration settings and click "Review + create".
6. After validation, click "Create" to provision the VMSS.

**Task 2: Check Web Server Reachability and Perform Load Test**

1. Once the VMSS is created, navigate to the "Overview" page.
2. Locate the public IP address of the load balancer associated with your VMSS.
3. Open a web browser and enter the public IP address of the load balancer to check if you can reach the web server.
4. To perform a load test, you can use various tools like Apache JMeter, Siege, or Microsoft's own Azure Load Testing service.
5. Configure the load test tool to simulate a high workload on your web server.
6. Monitor the CPU usage of the VM instances in the VMSS. When the CPU usage exceeds 75%, the scaling policy should automatically add more VM instances to handle the increased load.
7. After the load test, verify that new VM instances were added to the VMSS.
8. Similarly, if the CPU usage drops below 30%, VM instances should be removed from the VMSS.