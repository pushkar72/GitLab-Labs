# Setup Native License Compliance in Existing Pipelines


## Setup Compliance Job

- Open `.gitlab-ci.yml` file in Project
- Add/Append below stage to yaml
  ```yaml
   stages:
     - test
  ```

## Download & Add Compliance Check file in Project

- Visit `https://gitlab.com/gitlab-org/gitlab/blob/master/lib/gitlab/ci/templates/Security/License-Scanning.gitlab-ci.yml`
- Download the FIle & Add to your project at root location
    
     ![Screenshot1](./images/L6-1.jpg)

- Rename file to License-Scanning.gitlab-ci.yml

- Visit `https://gitlab.com/gitlab-org/gitlab/blob/master/lib/gitlab/ci/templates/Security/Dependency-Scanning.gitlab-ci.yml`
- Download the FIle & Add to your project at root location
- Rename file to Dependency-Scanning.gitlab-ci.yml

## Make changes in `.gitlab-ci.yml` CI File

- Open `.gitlab-ci.yml` file in Project 
- Add below yaml snippet after stage section
  ```yaml
  include:
  - template: SAST.gitlab-ci.yml
  - template: License-Scanning.gitlab-ci.yml
  - template: Dependency-Scanning.gitlab-ci.yml
  ```
- Perform Commit & Push


