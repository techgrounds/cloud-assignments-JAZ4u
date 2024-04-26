# [5/ Azure Storage Account]

Om data op te slaan in Azure heb je een Azure Storage Account nodig. In een Storage Account staan alle Azure Storage data objects als blobs, files, disks en tables.

Data in een Storage Account is secure, highly available, durable en massively scalable. Alle data in een Storage Account is bereikbaar via het internet met HTTP en HTTPS. Omdat het makkelijk te bereiken is moet je goed opletten dat alleen de juiste identiteiten permissies hebben om bij de data te komen. Azure Storage explorer is een gratis GUI om je data te beheren in Azure. Veel IaaS en PaaS services van Azure maken ook gebruik van Azure Storage Accounts. Naast het opslaan van data kan Blob Storage ook gebruikt worden voor het hosten van statische websites.

Note: AWS heeft met Techgrounds een statische demo-website gedeeld. Omdat het niks meer dan HTML, CSS en JavaScript is, werkt het ook als je het host in Azure Blob Storage.

## Key-terms

- https://portal.azure.com/)

- AWS Demo Website

## Assignment

Exercise 1:
Create an Azure Storage Account. Ensure that only you have access to the data. Place data in a storage service of your choice via the console (for example, a cat photo in Blob storage). Retrieve the data to your own computer using the Azure Storage Explorer.

Exercise 2:
Create a new container. Upload the 4 files that together form the AWS Demo Website. (note: this is an Azure task, but we are using the demo website from AWS. It is a simple combination of HTML, CSS, and JavaScript and does not have any cloud-specific features). Ensure that Static Website Hosting is enabled. Share the URL with a teammate. Ensure that your teammate can view the website.

### Used sources

- CHAT-GPT

- learn.techgrounds.nl

### Encountered problems

- no problems

### Result

**Exercise 1:**
Create an Azure Storage Account. Ensure that only you have access to the data. Place data in a storage service of your choice via the console (for example, a cat photo in Blob storage). Retrieve the data to your own computer using the Azure Storage Explorer.

    

1. **Create an Azure Storage Account:**
   
   - Log in to the Azure Portal.
   - Navigate to the Storage Accounts service.
   - Click on "Create" to create a new storage account.
   - Choose a subscription, resource group, storage account name, location, and performance tier.
   - Set the "Secure transfer required" option to enabled for enhanced security.
   - Set the "Allow access from" option to "Selected networks" and add your IP address for access restriction.
   - Review and create the storage account.

2. **Place data in Blob storage:**
   
   - Navigate to the created storage account.
   - Go to the Blob service.
   - Create a new container if one doesn't exist already.
   - Upload a cat photo or any desired data to the container.

3. **Retrieve data using Azure Storage Explorer:**
   
   - Download and install Azure Storage Explorer on your computer.
   - Open Azure Storage Explorer and sign in with your Azure account.
   - Connect to your Azure subscription and navigate to the storage account.
   - Locate the Blob container where you uploaded the data.
   - Download the desired data (cat photo) to your computer.

**Exercise 2:**
Create a new container. Upload the 4 files that together form the AWS Demo Website. (note: this is an Azure task, but we are using the demo website from AWS. It is a simple combination of HTML, CSS, and JavaScript and does not have any cloud-specific features). Ensure that Static Website Hosting is enabled. Share the URL with a teammate. Ensure that your teammate can view the website.

1. **Create a new container:**
   
   - Navigate to the Azure Storage Account created earlier.
   - Go to the Blob service.
   - Create a new container named "demo-website" or similar.

2. **Upload the 4 files for the AWS Demo Website:**
   
   - Upload the HTML, CSS, JavaScript, and any other necessary files to the "demo-website" container.

3. **Enable Static Website Hosting:**
   
   - Go to the "Static website" setting in the storage account.
   - Enable static website hosting and specify the default document name (e.g., index.html).
   - Note down the primary endpoint URL provided after enabling static website hosting.

4. **Share the URL with a teammate:**
   
   - Share the primary endpoint URL (e.g., https://yourstorageaccountname.z6.web.core.windows.net) with your teammate.

5. **Ensure teammate can view the website:**
   
   - Ask your teammate to open the shared URL in a web browser to verify that they can view the AWS Demo Website hosted on Azure Blob storage.