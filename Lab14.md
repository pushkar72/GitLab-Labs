# Downstream Pipeline Trigger

## Task 1 : Configure Trigger


- Create a new project by name GitlabTrigger
- Create `.gitlab-ci.yml` file
- Add below code snippet
  ```yaml
  samplejob:
    script:
      - echo "I am Triggered"
  ```
- Goto Project Settings > CI/CD > Pipeline Trigger
- In Description add a Trigger Name `PipeTrigger`
- Add Trigger
- Note Trigger Token Value
- Note Trigger Url 

## Task 2 : Add Trigger Job 

- Goto GitLabWebApp Project 
- Open Project in VSCode
- Open `.gitlab-ci.yml`
- Add a new stage `triggerdemo` in stages section
- Add a new Job
  ```yaml
  triggerjob:
    stage: triggerdemo
    script:
      - "curl -X POST -F token=TOKEN -F ref=REF_NAME https://gitlab.com/api/v4/projects/18843993/trigger/pipeline"
  ```
- Enter Token value in `token=Token` part
- In `ref` enter `master`
- In Url enter the Trigger url
- Commit & Checkin
- Observe Pipeline Execution in Both project

