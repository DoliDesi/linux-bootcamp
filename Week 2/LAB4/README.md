# Lab 4: Manage Packages and Services on a Linux VM (Azure or AWS)

1. Create a Linux VM
2. Install the Apache Web Server
3. Start the service status via command line
4. Investigate the service status via command line
5. Stop the service 

Challenge: Create a boostrapping script that will install and start this service on new EC2 VMs

### Notes:

Install and Configure Apache (Ubuntu)
* https://ubuntu.com/tutorials/install-and-configure-apache#1-overview

How to install Apache on RHEL 8 / CentOS 8 Linux
* https://linuxconfig.org/installing-apache-on-linux-redhat-8

How to use cloud-init to customize a Linux virtual machine in Azure on first boot
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-automate-vm-deployment

Create bootstrap actions to install additional software
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-bootstrap.html

# Notes

1. I created a VM with the Azure CLI using the following commands
'az group create --name RG01 --location eastus'
az vm create --resource-group Rg01 --name VM01 --image ubuntults --admin-username 
dollypee --generate-ssh-keys'
2. To connect to the Apache2 Web server, I used the following commands 
'az vm open-port --port 80 --resource-groupRG01 --name VM01' 
'ssh dollypee@20.127.38.189'   
'sudo apt-get -y update && sudo apt-get -y install Apache2'
3. To start the service status: We use the command  'az vm start -g NewResourceGroup -n NewVM'

4. To investigate the service status: W use the command 'az vm show --resource-group RG1 --name VM1'

5. To stop the service: ' az vm stop --resource-group RG1 --name VM1'
