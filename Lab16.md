# Deploy To Kubernetes wit CD Job

## (SKIP THIS) Task 1 : Get Configurations of Kubernetes CLuster

- Get CA Base64 value for
- Get API URL
- Get Token
- GoTo CI/CD Settings > Variables
- Add Variable **CERTIFICATE_AUTHORITY_DATA** value _Base64 Cert Value_ from step 1
- Add Variable **SERVER** value _APIURL_ from step 2
- Add Variable **USER_TOKEN** value _TokenValue_ from step 3
## Task 2 : Add Yaml in Lab12.2

- Create `deployment.yaml` file at root folder in your project
- Copy Paste the YAML Code from Lab 12.2

## Task 3: Add Kube Job

- Add below code snippet in Pipeline file
  ```yaml
  deploycontainer:
    stage: deploytokube
    image: dtzar/helm-kubectl
    environment:
      name: azure
    script:
      - kubectl apply -f deployment.yaml
      - kubectl expose deployment rss-site --type=LoadBalancer --name=gitlabappservice
  ```
