# Lab 1: Create a Linux virtual machine with the Azure CLI

1. Launch Azure Cloud Shell
2. Create a resource group
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart


## Azure Cloud Shell is a browser-based shell experience to manage and develop Azure resources

1. I launched the Azure cloud Shell by opening *https://shell.azure.com/bash* in a web browser
2. I then created a resource group using the command *az group create --name NewRG --location eastus*
3. A Virtual machine was created using the following command *az vm create \
  --resource-group NewRG \
  --name NewVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys*
  
  I noted my PublicIPAddress in the output of my VM *20.124.246.50*
  
  4. To open port 80 using *az vm open-port --port 80 --resource-group NewRG --name NewVM*
  
  5. Connect to Vm using the IP Address that was previously noted. *ssh azureuser@20.124.246.50*
6. To install the web server, *sudo apt-get -y update    
sudo apt-get -y install*
7. To view the web server in action I posted my PublicIPAddress of my VM as the web address.
