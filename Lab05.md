# Setup Dotnet Core Build Pipeline

## Setup Build Jobs

- Create `.gitlab-ci.yml` file in Project
- Add below stages
  ```yaml
  stages:
    - build
    - codeanalysis
    - dockerbuild
    - deploytovm
  ```

 - Add Below Build Job
    ```yaml
    build_application:
      image: mcr.microsoft.com/dotnet/core/sdk:3.1
      stage: build
      script:
        - dotnet build GitLabWebApp.csproj
        - dotnet publish GitLabWebApp.csproj -c Release -o publish 
      artifacts: 
        paths:
          - publish/
        expire_in: 1 week 
    ```
- Open Terminal Run
  ```shell
    git commit -a -m "Added CI Pipeline in Project"
    git push
  ``` 
