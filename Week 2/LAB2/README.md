# Lab 2: Manage Linux VMs with the AWS CLI

1. Create virtual machine
2. Connect to VM
3. Understand VM images
4. Understand VM sizes
5. VM power states
6. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Using a custom Amazon machine image (AMI)
* https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.customenv.html

Quickstart: Restart VM via CLI
* https://docs.aws.amazon.com/cli/latest/reference/ec2/reboot-instances.html

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html

# Answers

1.  A virtual machine can be created either through the AWS CLI or the AWS Console. I launched an instance using the command 'aws ec2 run-instances \
    --image-id ami-0ed9277fb7eb570c9 \
    --instance-type t2.micro \
    --key-name aws-linux'
 
2. I was able to connect to the Virtual machine using the ssh client. I located where my pem file was on my bash terminal and connected straight ahead.
3. Understanding VM Images/Amazon Machine Image(AMI): An Amazon Machine Image (AMI) is a master image for the creation of virtual servers -- known as EC2 instances -- in the Amazon Web Services (AWS) environment. The machine images are like templates that are configured with an operating system and other software that determine the user's operating environment. AMI types are categorized according to region, operating system, system architecture -- 32- or 64-bit -- launch permissions and whether they are backed by Amazon Elastic Block Store (EBS) or backed by the instance store.
4. Understanding VM Sizes:
