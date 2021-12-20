# Lab 4: Create and use an SSH public-private key pair for Linux VMs in Azure

1. Supported SSH key formats
2. Create an SSH key pair
3. Provide an SSH public key when deploying a VM
4. SSH into your VM

### Notes:

Quickstart: SSH for Linux VMs
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/mac-create-ssh-keys

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart

# Supported SSH Key Formats
Azure currently supports SSH protocol 2 (SSH-2) RSA public-private key pairs with a minimum length of 2048 bits. Other key formats such as ED25519 and ECDSA are not supported. 

# Create an SSH Key pair
Use the ssh-keygen command to generate SSH public and private key files. By default, these files are created in the ~/.ssh directory. The command 'ssh-keygen -m PEM -t rsa -b 4096' is used to create an ssh key pair using RSA encryption and a bit length of 4096.


# Provide an SSH public key when deploying a VM 
For example, when deploying a VM the public key that you place on your Linux VM in Azure is by default stored in ~/.ssh/id_rsa.pub, unless you specified a different location when you created the key pair. 

# SSH into your VM

We SSH into the VM using the IP address of the VM, the command 'ssh dolidesi@20.127.96.84'
