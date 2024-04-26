# [7/ Azure Disk Storage]

Azure Disk Storage can be seen as a virtual hard drive in the cloud. A disk can be an OS disk (where the OS is located) or a Data Disk (comparable to an external hard drive). You have a choice between Managed Disks and Unmanaged Disks. Unmanaged Disks are cheaper, but you need a Storage Account for them (and you have to manage the disk yourself). Managed Data Disks can be shared between multiple VMs, but that's a relatively new feature and there are some caveats to it. Backups of a Managed Disk can be made with Incremental Snapshots that only store the changes since the last snapshot. For an Unmanaged Disk, you can only take a 'regular' snapshot.

There are 5 managed disk types. Generally, more performance results in higher costs. See https://learn.microsoft.com/en-us/azure/virtual-machines/disks-types for an up-to-date overview of the available disk types.

A disk can be encrypted for security. Disks can be enlarged, but not reduced in size.

If you want to use an external device (including a Data Disk) on Linux, you must first mount it.

## Key-terms

- ## Assignment

Task:

- Start 2 Linux VMs. Ensure that you have SSH access to both.
- Create an Azure Managed Disk and attach it to both VMs simultaneously.
- On your first machine, create a file and place it on the Shared Disk.
- Check on the second machine if you can read the file. (Note: you may need to remount the disk on your 2nd VM)
- Take a snapshot of the disk and try creating a new Disk from it.
- Mount this new Disk and view the file.

### Used sources

- learn.techgrounds.nl

- CHAT-GPT

### Encountered problems

- no problems

### Result

Task:

- Start 2 Linux VMs. Ensure that you have SSH access to both.
- Create an Azure Managed Disk and attach it to both VMs simultaneously.
- On your first machine, create a file and place it on the Shared Disk.
- Check on the second machine if you can read the file. (Note: you may need to remount the disk on your 2nd VM)
- Take a snapshot of the disk and try creating a new Disk from it.
- Mount this new Disk and view the file.

  SOLUTION:

  To solve the task, follow these steps:

1. **Start 2 Linux VMs and ensure SSH access:**
   
   - In the Azure Portal, create two Linux VMs.
   - Make sure to configure SSH access during VM creation or after provisioning.
   - Note down the public IP addresses or hostnames of both VMs.

2. **Create an Azure Managed Disk and attach it to both VMs:**
   
   - In the Azure Portal, navigate to the Disks service.
   - Create a new Managed Disk with the desired specifications.
   - Once the disk is created, attach it to both VMs. Ensure that both VMs are running when attaching the disk.

3. **Create a file on the Shared Disk from the first machine:**
   
   - SSH into the first VM.
   - Mount the Shared Disk to a directory on the first VM.
   - Create a file and place it on the Shared Disk.

4. **Check if you can read the file from the second machine:**
   
   - SSH into the second VM.
   - If necessary, mount the Shared Disk to a directory on the second VM.
   - Check if you can read the file placed on the Shared Disk from the second VM.

5. **Take a snapshot of the disk and create a new Disk:**
   
   - In the Azure Portal, navigate to the Disks service.
   - Select the Shared Disk and create a snapshot.
   - Once the snapshot is created, use it to create a new Managed Disk.

6. **Mount the new Disk and view the file:**
   
   - Attach the new Disk to one of the VMs.
   - SSH into the VM where the new Disk is attached.
   - Mount the new Disk to a directory on the VM.
   - View the file placed on the Shared Disk from the first VM to verify that it is accessible from the new Disk.
   
   By following these steps, you'll be able to complete the task and verify that the file placed on the Shared Disk can be accessed from both VMs, as well as from the new Disk created from the snapshot.