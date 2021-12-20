# Lab 3: Manage Azure disks with the Azure CLI

1. Default Azure disks
2. Azure data disks
3. VM disk types
4. Launch Azure Cloud Shell
5. Create and attach disks
6. Prepare data disks
7. Take a disk snapshot

### Notes:

Quickstart: Manage Azure disks
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-disks

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart


# 1. Default Azure Disk
At every point when a virtual machine is created, two disks are automatically created with it. They are: 
- Operating system disk
- Temporary system disk
# 2. Azure Data Disk
Depending on the number of applications to be installed or data to be stored, data disks can be added additionally to the previous automatically supplied. The size of the virtual machine determines how many data disks can be attached to a VM.
# 3. VM Disk Types
The Azure VM disk types are: 
- Standard disks are backed by HDDs and ideal for a cost effective dev and test workload, while
- Premium disks are backed by SDD and are high-performnce, low-latency disk.

# 4. Launch a Cloud Shell
I launched a cloud shell using, https://shell.azure.com/bash

# 5. Create and Attach Disks
 We can either attach disk at VM creation or create one with an existing VM. We use the command ' az vm disk attach'

 # 6. Prepare Data Disks
 To prepare my data disk, I SSH into my Virtual Machine using the IP address that was generated earlier. 

 # 7. Take a disk Snapshot 
 Azure VM Snapshots are used to save the state of a particular VM before any configuration changes are made, in the case of an error, VM can be restored using a Snapshot. We use the command 'az snapshot create'
 
