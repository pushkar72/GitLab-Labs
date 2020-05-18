# Design your First Build Pipeline

## Create CI Pipeline
- Open Your Project on VS Code
- Run in Terminal `git checkout dev`
- Create file by name **_.gitlab-ci.yml_**
- Add a stage `build_the_car`
  ```yaml
  build_the_car:
    script:
      - mkdir build
      - cd build
      - echo "Chasis" > car.txt
      - echo "Engine" >> car.txt
  ```
- Run
  ```git
  git commit -a -m "Added CI Pipeline"
  git push
    ```
- Goto Gitlab > CI/CD > Pipelines
- Check Pipeline Execution Logs


## Working with Stages

- Open VS Code
- Open _.gitlab-ci.yaml_
- At the top of the file add below code snippet
    ```yaml
    stages:
     - build
     - test
    ```
- Add one more job after _build the car stage_
- Add below code Snippet
    ```yaml
        test_the_car:
          script:
            - test -f publish/car.txt
    ```
- Add **stage** key to both build job so that both job executes in sequence. You snippet should look like this:
  ```yaml
    stages:
     - build
     - test
    
    build_the_car:
      stage: build
      script:
        - mkdir build
        - cd build
        - echo "Chasis" > car.txt
        - echo "Engine" >> car.txt
     
    test_the_car:
      stage: test
      script:
            - test -f publish/car.txt
  ```

- Push Changes to Repository and Notice Changes in Pipeline Execution


## Add Artifacts Information

- Open CI Pipeline file in VS Code
- Add below code snippet at the end `build_the_car` job
    ```yaml
    artifacts:
      paths:
        - build/
    ```
- Push Changes  to Repository and Check Pipeline Execution
