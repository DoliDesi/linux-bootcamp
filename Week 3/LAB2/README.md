# Lab 2: Install a LAMP stack on an Azure Linux VM

1. Prepare the LAMP server
2. Test your Lamp server
3. Secure the database server
4. (Optional) Install phpMyAdmin

### Notes:

Tutorial: Install a LAMP web server on the Amazon Linux AMI
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-LAMP.html

Tutorial: Host a WordPress blog on Amazon Linux 2
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/hosting-wordpress.html

Sample Gist
* https://gist.github.com/mikepfeiffer/c079608703e604224e58a3d40d0fa043#file-lamp-linux-aws-sh


# Notes
1. Prepare the LAMP server:
To prepare the LAMP server, we create an instance using the Amazon Linux AMI, after which we configure the security group to allow both ssh(port22) and HTTP(port 80) for web traffic. 
- We check for the latest security update on our instance using the command ' sudo yum update -y' 
-  We then install the LAMP- APACHE2 Web server, MYSQL, PHP software packages using a command that installs them simulteneously
' sudo yum install -y httpd24 php72 mysql57-server php72-mysqlnd'
I got an error message at this point and had to troubleshoot. 
- To start the Apache server, we use the 
'sudo systemctl start server' command

2. Test the LAMP server:
