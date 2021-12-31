# Lab 1: Deploy a container instance in Azure using the Azure CLI

1. Create a resource group
2. Create a container
3. Pull the container logs
4. Attach output streams
5. Clean up resources

### Notes:

Quickstart: Deploy a container instance in Azure using the Azure CLI
* https://docs.microsoft.com/en-us/azure/container-instances/container-instances-quickstart


# Notes
1. Create a resource group: This we already know is to run the command 'az group create --name Lab4 --location eastus'

2. Create a container: I encountered an error here when I tried to launch a container and associate a DNS name with it upon creation. It failed because the DNS name was already used. I had to choose another label to proceed. I checked the status of my Container using the 'az container show' command, the output in the Provisioning state stated 'Succeeded'. I then inputed my IP in the Web browser which gave me the below web page.
![Docker](https://user-images.githubusercontent.com/94450478/147675960-3176fda5-f180-44dd-a169-fa5f7983c859.png)



3. Pull the container logs: Docker logs are the console output of running containers. They provide the stdout (standard output) and stderr (standard error) streams of processes that run inside a container. To pull the Docker logs, I use the command 'az container logs --resource-group Lab4 --name container1'
4. Attach output streams: I used the command 'az container attach --resource-group lab4 --name container1'
5. Clean up resources: To clean up resources deletes the container created earlier to prevent it from accruing charges. we use the command 'az container delete --resource-group lab4 --name container1'
To be very sure the container has been deleted, we check using 'az container list --resource-group lab4 --name container1'
