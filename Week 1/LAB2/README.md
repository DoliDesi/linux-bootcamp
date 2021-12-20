# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
2. Create virtual machine
3. Connect to VM
4. Understand VM images
5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart


## Azure Resources Groups are logical collections of virtual machines, storage accounts, virtual networks, web apps, databases, and/or database servers.
# 1. Create a resource group
To create a resource group, I used the command 'az group create --name NewRg01 --location eastus'
# 2. Create a Virtual Machine
 A VM was then created using 'az vm create \ --resource-group NewRg01 --name NewVM \ --image ubuntults \ --admin-username azureuser \ --generate-ssh-keys
# 3. Connect to the VM
We then connect to the VM with the ssh given above i.e 'ssh azureuser@20.127.96.84'

# 4. Understand VM Images: 
The Azure marketplace includes many images that can be used to create VMs. To see a list of the most commonly used images, use the 'az vm image list' command. When specifying the image, the image version number can be replaced with “latest”, which selects the latest version of the distribution.

# 5. Understanding VM Sizes: 
 Virtual machines need to be sized appropriately for the expected work load. If workload increases, an existing virtual machine can be resized.To see a list of VM sizes available in a particular region, use the az vm list-sizes command.

# 6. Power States:
 Azure VM (virtual machines) have various power states available which are related to each VM’s lifecycle. To retrieve the state of a particular VM, use the az vm get-instance-view command. 

# 7. Management Task: 
Using the Azure CLI, many common management tasks can be run from the command line or in scripts.  While working on a virtual machine, you may want to run management tasks such as *starting*, *stopping*, or *deleting* a virtual machine. Also, you may want to create scripts to automate repetitive or complex tasks. 
