# Lab 2: Build and store container images with Azure Container Registry

1. Deploy Azure Container Registry
2. Build container images with Azure Container Registry Tasks
3. Deploy images from Azure Container Registry
4. Replicate a container image to different Azure regions

### Notes:

Build and store container images with Azure Container Registry
* https://docs.microsoft.com/en-us/learn/modules/build-and-store-container-images/

To deploy an Azure container registry, I :
- Created a group using the 'az group create' command.
- Named my registry. It was quite a lot of back and forth on this one as I had to choose a name that hasnt been previously used. I eventually used 'ACR_NAME=deeACR'
- Created a new container registry
