# Continuous Deployment on Web Server

## Task 1: Register Deployment server as Runner Agent

## Task 2: Configure Windows Server

- Open Powershell Windows server Machine
- Run `Install-WindowsFeature -Name Web-Server -IncludManagementTools -IncludeAllSubFeatures`
- Wait for Installation to Complete 

## Task 3: Add CI Job

- Open project in VSCode
- Open CI Pipeline
- Add Below Job
  ```yaml
  deploy to iis:
    stage: publish
    script:
      - Stop-WebSite -Name "Default Web Site"
      - 'xcopy /y /s ".\publish\*.*" "C:\inetpub\wwwroot"'
      - Start-WebSite -Name "Default Web Site"
    dependencies:
      - build_the_project
   ```
- Commit and Push