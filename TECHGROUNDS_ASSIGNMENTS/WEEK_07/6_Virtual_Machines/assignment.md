# [6/ Virtual Machines]

De Service waarmee je VMs kan maken in Azure heet (zeer toepasselijk) Azure Virtual Machines. Je kan deze VMs gebruiken voor alles waar je een fysieke server voor zou gebruiken. Omdat ze in een datacenter van Microsoft staan, kan je er alleen verbinding mee maken via het internet. Verbinding met een remote Linux-machine maak je met het Secure Shell (ssh) protocol. Voor een verbinding met Windows machines gebruik je het Remote Desktop Protocol (RDP).

Om een VM aan te maken moet je een image selecteren. Een image is een soort blauwdruk voor je machine. Het bevat onder andere een template voor het OS.

VMs komen in verschillende sizes. Elke size heeft een andere hoeveelheid vCPUs, RAM, Data disks, Max IOPS, Temp storage, Premium disk support en prijs.

Voor de OS disk (de root volume) kan je kiezen uit Premium SSD, Standard SSD en Standard HDD. Je hebt ook de optie om extra Data disks toe te voegen.

Je kan optioneel je VM beveiligen met een NIC network security group. Het wordt aangeraden om network security groups te configureren op subnet niveau (en dus niet op instance niveau) waar mogelijk, maar soms heb je een allow/deny rule nodig op een specifieke instance, dus de optie is er. In elk geval kan je firewalls dus buiten de instance regelen, en hoef je niet binnen de VM nog een extra firewall te configureren.

Met Custom Data kan je een cloud-init script, config file of andere data meegeven tijdens het opstarten van de VM. Hiermee kan je automatisch servers configureren zonder zelf in te loggen. User data is een nieuwe versie van Custom data. Het grootste verschil is dat User Data beschikbaar blijft gedurende de hele levensduur van de VM.

De prijs van een Azure VM hangt af van de size, de image, de regio waar hij in staat, het aantal minuten dat hij aan staat, en het type betaling dat je doet.

- Pay-as-you-go is de duurste optie, maar ook het meest flexibel.
- Reserved Instances zijn goedkoper, maar je zit vast aan een reservatie van 1 of 3 jaar.
- Spot instances zijn over het algemeen het goedkoopst, maar de availability hangt af van de vraag naar VMs op dat moment, dus ze zijn niet altijd betrouwbaar.

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
     
     - Open a web browser and navigate to the Azure Portal (https://portal.azure.com).
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