# Create Kubernetes Cluster on Azure & Deploy Container Image via GitLab

## Task 1: Create Kubernetes Cluster on Azure

- Goto `portal.azure.com`
- Search Kubernetes Services
  
  ![sc](images/L12-1.jpg)

- Click Add
- In Create Kubernetes Cluster Page enter below details
    - Resource Group: _(YourName)_
    - Kubernetes Cluster Name: _kubecluster-(your initials)_
    - Region: _East US_
    - Version : _Default_
    - Node Size : _Standard B2ms_
    - Node Count : 1

    ![sc](images/L12-2.jpg)

- Next **Node Pools**
  - Virtual Nodes : Disabled
  - VM Scale Sets : Disabled
- Next **Authentication*
  - Role based Access control : Disabled
    
    ![sc](images/L12-3.jpg)

- Next **Networking** Nothing to changes
- Next **Integrations**
  - Disable Container Monitoring

- Click Review + Create ![sc](images/L12-4.jpg)
- After Validation Passes, Click Create ![sc](images/L12-5.jpg)


## Connect to Cluster

- Goto Kubernetes Cluster you have Created
- Click View Dashboard Tile in Overview Page
  
  ![sc](images/L12-6.jpg)
- Follow the Instruction as shown 
- After Running all commands you will connect to Cluster and it will take you to Cluster Landing page

    


---
## Task 2 : Deploy Container Images in Cluster

- Goto Gitlab Project > Package & Registry > Container Registries
- Select the Image Repository Shown
  
  ![sc](images/L12-7.jpg)
- Copy the registry url
  
  ![sc](images/L12-8.jpg)

- Goto to Kubernetes Cluster and Click Create button
  
  ![sc](images/L12-9.jpg)

- Click Create and App Tab
- ENter Detail as shown
  
  ![sc](images/L12-10.jpg)

    - Note: _Enter Registry Url copied from GitLab in Container Image_


- Click Deploy
- Goto Services
  
  ![sc](images/L12-11.jpg)

- Note External IP and enter in Web Browser
  
  ![sc](images/L12-12.jpg)