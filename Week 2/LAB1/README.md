# Lab 1: Create a Linux virtual machine with the AWS CLI

1. Launch AWS Cloud Shell
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:

Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html




# Answers



 # 1. The AWS Cloud shell can be launched directly from the AWS management console.
 # 2. Create a Virtual Machine: 
We open an amazon EC2 console and click on the launch instance tab to create and configure the virtual machine. An Instance can also be called a virtual machine. Amazon EC2(Amazon Elastic Compute Cloud) is a web service that provides secure,resizable compute capacity in the cloud. 
- The first step is to create an Amazon Machine Image for software configuration.

- Secondly, we choose an instance size out of a wide selection of instance sizes to fit different purposes/applications. The AMI is a combination of CPU, memory, Storage, and networking capacity. Here, we chose 't2' under the Free tier eligible, it consists of 1 CPU and 1GB memory.


- Configure Instance to match the requirements. Here we can choose the preferred number of instances, network and a number of other configurations. We chose 1 under number of instances, and the default network.
- Add Storage: No changes made here, just the default 8 giB Os disk.
- Add Tags: Tags hepls to categorise AWS resources in different ways
- Configure Security group i.e a set of firewall rules that control the traffic for the instance. We SSH into port 22 using my IP address as the source. We then added an HTTP port 80 rule, leave it under custom for accesibility to the public.

- Review Instance Launch: Before the instance is launched we need to review our options in case of mistakes. A private key is downloaded. The Private key helps to ssh securly into the instance. 



# 3. Opening port 80 for Web traffic
Opening port 80 for web traffic means that the site is open to the public for viewing, normally it is not open until you decide to make it public. To do this, I opened the security group -- Inbound rule -- Edit inbound rule-- Add HTTP -- save changes.

# 4. Connect to Virtual Machine
I used the EC2 Instance Connect to connect my instance. To achieve this I had to go to the AWS General Reference to download the AWS IP Address ranges. I then located the IP Address under the EC2 Instance Connect to my specific region 'us east2' which is  '3.16.146.0/29'. I made some changes in my Inbound rule and saved. 

# 5. Install web server
To install the Apache2 web server, I ran the commands below
'sudo yum update -y'
'sudo yum install -y httpd'


# 6. View Web Server in action
To view my web server, I used the Public IP address of my Instance
