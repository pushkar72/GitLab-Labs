# Integrate SonarCloud in GitLab CI

## Task 1  : Create and Setup Sonar Cloud Account

- Goto www.sonarcloud.io
- SignIn **GitLab**

     ![Screenshot](images/L7-1.jpg)

- Authorize
    
     ![Screenshot](images/L7-2.jpg)

- Analyze your repo > Select Import projects from GitLab

     ![Screenshot](images/L7-3.jpg) 

- Create Organization

     ![Screenshot](images/L7-4.jpg)

- Generate Access Token from GitLab with _api_ scope checked and enter here
  
     ![Screenshot](images/L7-5.jpg)

- Setup Organization name, Enter your name or Leave the default option shown

     ![Screenshot](images/L7-6.jpg)

- In Next Page select free plan, if free plan in greyed out go to project settings in gitlab and make your project visibility public and save chnages

     ![Screenshot](images/L7-7.jpg)
    
    - Refresh SonarCloud Page, select free plan and click create organization

     ![Screenshot](images/L7-8.jpg)

---
## Task 2 : Analyze Project

- Analyze new Project

     ![Screenshot](images/L7-9.jpg)

- Select Project You would like to Analyze

     ![Screenshot](images/L7-10.jpg)



- Click _With Gitlab CI/CD Pipeline_ and follow the instruction show further

     ![Screenshot](images/L7-11.jpg)


---
## Task 3 : Configure Gitlab and Project

- After you have configured Environment variables as directed by Instruction on Sonar Platform
- Select Other and copy paste the code snippet shown in your CI Pipeline file after the build job and click continue

     ![Screenshot](images/L7-12.jpg)


- Add `sonar-project.properties` file in your project in root location and code snippet shown as in Sonar Platform

     ![Screenshot](images/L7-13.jpg)
