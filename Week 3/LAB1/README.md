# Lab 1: Install a LAMP stack on an Azure Linux VM

1. Create a resource group
2. Create a virtual machine
3. Open port 80 for web traffic
4. SSH into your VM
5. Install Apache, MySQL, and PHP
6. Install WordPress

### Notes:

Tutorial: Install a LAMP stack on an Azure Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-lamp-stack

Sample Gist
* https://gist.github.com/mikepfeiffer/96d659042f0575a617648a33c92b8f4a

Build and run a web application with the MEAN stack on an Azure Linux virtual machine
* https://docs.microsoft.com/en-us/learn/modules/build-a-web-app-with-mean-on-a-linux-vm/

MEAN Stack App
* https://github.com/MicrosoftDocs/mslearn-build-a-web-app-with-mean-on-a-linux-vm



## LAMP-STACK on an Azure Linux VM
### What is a LAMP-STACK? A LAMP-STACK is LAMP on an open source Web development platform that uses *Linux* as the operating system, *Apache* as the Web server, *MySQL* as the relational database management system and *PHP* as the object-oriented scripting language. (Sometimes *Perl* or *Python* is used instead of PHP.)      
1. To create a resource group, we use the command *'az group create --name LAMP-STACK-RG --location westus2'*
2. To create a virtual machine, we use the command *'az vm create --resource-group LAMP-STACK-RG --name WEB-SRV-01 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys'*
3.  We open port 80 with the command *'az vm open-port --port 80 --resource-group LAMP-STACK-RG --name WEB-SRV-001'*
4. To ssh into our VM *'ssh azureuser@20.69.166.155"*
5. To install Apache,MySQL and PHP
- sudo apt-get -y update && sudo apt-get install lamp-server^ -y
- we check the version of the Apache installation with the command *apache2 -v*
- sudo mysql_secure_installation
- we check the version of the MySQL with *apache2 -v*
- sudo mysql -u root -p
- we verify the version of the PHP with *php -v*
6.  To install the WordPress, we use the command 'sudo apt install wordpress-y'
