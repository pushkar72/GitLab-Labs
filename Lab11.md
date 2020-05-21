# Working with Environment Variables

## Setup Variables

-  Goto Project Settings > CI/CD > **Variables**
-  **_Note Variable names are case sensitive_**
-  Add Variable
-  In Key Enter Secret
-  In Value Enter _This is secret message for Release Environment_
-  In Environment Scope Enter `Release` (Create Wildcard)
-  Add Variable
  ---
-  Add New Variable Again
-  In Key Enter Secret
-  In Value Enter _This is secret message for Beta Environment_
-  In Environment Scope Enter `Beta` (Create Wildcard)
-  Add Variable

## Access Variable in CI Pipeline

- Open Project in VSCode
- Add 2 New Jobs
  ```yaml
  releasejob:
    environment: Release
    script:
     - echo $Secret

  betajob:
    environment: Beta
    script:
      - echo $Secret
  ```
- Commit & Push
- Observe Pipeline Execution