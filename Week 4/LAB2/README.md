# Lab 2: Build and store container images with Azure Container Registry

1. Deploy Azure Container Registry
2. Build container images with Azure Container Registry Tasks
3. Deploy images from Azure Container Registry
4. Replicate a container image to different Azure regions

### Notes:

Build and store container images with Azure Container Registry
* https://docs.microsoft.com/en-us/learn/modules/build-and-store-container-images/

To deploy an Azure container registry, I :
1.Created a group using the 'az group create' command.
- Named my registry. It was quite a lot of back and forth on this one as I had to choose a name that hasnt been previously used. I eventually used 'ACR_NAME=deeACR'
- Created a new container registry

2. To build container images
- Firsty, I ran the 'code' on my terminal and pasted some configurations into the cloud shell editor after which I was prompted to save my file.
- I then ran the command "az acr build" 
- To verify the container image has been created successufully, use the command "az acr repository list"

3. To deploy images from Azure container registry, we need to enable the registry admin account using the following commands
- 'az act update -n deeACR --admin-enabled true'. Here a username and password for the created admin account is generated.
- 'az acr credential show --name deeACR' This command shows you the generated username and password. 
Now to deploy a container instance, we use the command 'az container create' ,we then input the username and password that was shown previously and the location. We took note of the IP address shown. 
- I then inputed the IP address shown in my web browser and it gave me the below result

![image](https://user-images.githubusercontent.com/94450478/148606128-ad165a7b-819a-404f-9aa3-9ae61a7097aa.png)

4. To replace a container image to a different region, I used the command 'az acr replication create --registry deeACR --location eastus' 
- Also, to see a list of the container image replicas, we used the command 'az acr replication list --registry deeACR --output table'

![image](https://user-images.githubusercontent.com/94450478/148608128-e6431230-2e70-401b-87ed-9acd319e1eac.png)
