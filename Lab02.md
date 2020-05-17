# Working with Branches

## Create New Branch Dev based on Master

- Open Terminal at Project Location
- Check Existing Branch `git branch`
- Create New Branch `git branch dev`
- Set **Dev** as active Branch `git checkout dev'
- ---
- #### Make Changes to Active Branch
   1. Goto Project > Views > Home > Index.cshtml
   2. Delete Existing HTML Code
   3. Add
    ```html
        <h1>Welcome to GitLab DevOps</h1>
    ```
   4. Run 
    ```git
        git add .
        git commit -m "Dev Branch Changes - Modified HTML File"
        git push --set-upstream origin dev
    ```
---
- ### **Protect Branches**
- Disable _Push_ in Master and Dev Branch
- Go to GitLab Project Settings >> Repository
- Pass below Options in Protected Branch
  1. Branch : _dev_
  2. Allow to Merge : _Maintainers_
  3. Allow to Push : _No One_
  4. Click Protect
  5. **Repeat Same Activity for Master Branch**
  
  
    ![Screenshot3](./images/L2-1.jpg)

