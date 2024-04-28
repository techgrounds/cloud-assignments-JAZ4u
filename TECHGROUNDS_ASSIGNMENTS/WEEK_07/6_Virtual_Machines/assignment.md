# [6/ Virtual Machines]

The service for creating VMs in Azure is aptly named Azure Virtual Machines. You can use these VMs for anything you would use a physical server for. Since they reside in a Microsoft data center, you can only connect to them via the internet. Connection to a remote Linux machine is made using the Secure Shell (SSH) protocol. For connecting to Windows machines, you use the Remote Desktop Protocol (RDP).

To create a VM, you must select an image. An image is a kind of blueprint for your machine. It includes, among other things, a template for the OS.

VMs come in various sizes. Each size has a different amount of vCPUs, RAM, data disks, Max IOPS, temp storage, premium disk support, and price.

For the OS disk (the root volume), you can choose from Premium SSD, Standard SSD, and Standard HDD. You also have the option to add additional data disks.

You can optionally secure your VM with a NIC network security group. It is recommended to configure network security groups at the subnet level (and thus not at the instance level) where possible, but sometimes you need an allow/deny rule on a specific instance, so the option is there. In any case, you can manage firewalls outside the instance, and you don't need to configure an additional firewall within the VM.

With Custom Data, you can pass a cloud-init script, config file, or other data during VM startup. This allows you to automatically configure servers without logging in yourself. User data is a newer version of Custom data. The main difference is that User Data remains available throughout the VM's entire lifespan.

The price of an Azure VM depends on the size, image, region it's located in, the number of minutes it's running, and the type of payment you choose.

- Pay-as-you-go is the most expensive option but also the most flexible.
- Reserved Instances are cheaper, but you're committed to a reservation for 1 or 3 years.
- Spot instances are generally the cheapest, but availability depends on the demand for VMs at that time, so they're not always reliable.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Exercise:

- Log in to your Azure Console.

- Create a VM with the following requirements:
  
  - Ubuntu Server 20.04 LTS - Gen1
  
  - Size: Standard_B1ls
  
  - Allowed inbound ports:
    
    - HTTP (80)
    
    - SSH (22)
  
  - OS Disk type: Standard SSD
  
  - Networking: defaults
  
  - Boot diagnostics are not needed
  
  - Custom data:

> > `#!/bin/bash`
> 
> > `sudo su`
> 
> > `apt update`
> 
> > `apt install apache2 -y`
> 
> > `ufw allow 'Apache'`
> 
> > `systemctl enable apache2`
> 
> > `systemctl restart apache2`

- Check if your server is working.
- Note! Don't forget to delete everything after completing the task. You can delete each component individually, or you can delete the entire resource group at once.

### Used sources

- learn.techgrounds.nl

- CHAT-GPT

### Encountered problems

- no problems

### Result

Exercise:

- Log in to your Azure Console.

- Create a VM with the following requirements:
  
  - Ubuntu Server 20.04 LTS - Gen1
  
  - Size: Standard_B1ls
  
  - Allowed inbound ports:
    
    - HTTP (80)
    
    - SSH (22)
  
  - OS Disk type: Standard SSD
  
  - Networking: defaults
  
  - Boot diagnostics are not needed
  
  - Custom data:

> > `#!/bin/bash`
> 
> > `sudo su`
> 
> > `apt update`
> 
> > `apt install apache2 -y`
> 
> > `ufw allow 'Apache'`
> 
> > `systemctl enable apache2`
> 
> > `systemctl restart apache2`

- Check if your server is working.

- Note! Don't forget to delete everything after completing the task. You can delete each component individually, or you can delete the entire resource group at once.
  
  SOLUTION:
  
  To solve the exercise, follow these steps:
  
  1. **Log in to your Azure Console:**
     
     - Open a web browser and navigate to the Azure Portal ( https://portal.azure.com ).
     - Sign in with your Azure account credentials.
  
  2. **Create a Virtual Machine with the specified requirements:**
     
     - In the Azure Portal, click on the "Create a resource" button (+) in the upper-left corner.
     - Search for "Virtual machine" in the search bar and select "Virtual machine" from the search results.
     - Fill in the required details:
       - Subscription: Choose your subscription.
       - Resource group: Create a new resource group or select an existing one.
       - Virtual machine name: Enter a name for your VM.
       - Region: Choose the desired Azure region.
       - Image: Select "Ubuntu Server 20.04 LTS - Gen1" from the list of available images.
       - Size: Choose "Standard_B1ls" from the available sizes.
       - Authentication type: Select "SSH public key" and provide the necessary SSH public key for authentication.
     - In the Networking tab, ensure that ports 80 (HTTP) and 22 (SSH) are allowed.
     - Leave other settings at their defaults.
  
  3. **Custom data:**
     
     - In the "Management" tab, scroll down to the "Custom data" section.
     
     - Enter the provided custom data script:
       
       ```bash
       #!/bin/bash
       sudo su
       apt update
       apt install apache2 -y
       ufw allow 'Apache'
       systemctl enable apache2
       systemctl restart apache2
       ```
     
     - This script will install Apache web server on the VM.
  
  4. **Create the VM:**
     
     - Review the configurations to ensure they match the exercise requirements.
     - Click on the "Review + create" button.
     - After validation passes, click on the "Create" button to deploy the VM.
  
  5. **Check if your server is working:**
     
     - Once the VM deployment is complete, navigate to its public IP address using a web browser.
     - If Apache is installed and running correctly, you should see the default Apache welcome page.
  
  6. **Delete Resources:**
     
     - After completing the task, ensure to delete all resources to avoid unnecessary charges.
     - You can delete each component individually or delete the entire resource group at once.