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