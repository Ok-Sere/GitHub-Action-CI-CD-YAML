# GitHub-Action-CI-CD-YAML

>Objectives
1. Set up build sets in Github action

2. Run test as part of th CI process



## **Detailed Explanation of the CI/CD Process (with Screenshots)**

### 1. **Repository Creation**

![1](./img/1.%20git%20repo.jpg)

- You started by creating a new GitHub repository for your Node.js project.  
- This is the foundation for version control and collaboration.



### 2. **Workflow Setup**

![1](./img/2.%20step%201.jpg)

- You navigated to the **Actions** tab in your repository to set up a new GitHub Actions workflow.
- This workflow will automate your CI/CD process.



### 3. **Script Configuration**

![1](./img/3.%20script.jpg)

- You configured your workflow YAML file (`main.yml`) to define the steps for your CI pipeline.
- The workflow includes steps to check out code, set up Node.js, install dependencies, build, and run tests.



### 4. **Advanced Workflow Settings**

![1](./img/4.%20advanced.jpg)

- You customized the workflow to fit your project’s needs, such as specifying the Node.js version and the branch to run on.
- This ensures the workflow only runs in the correct environment and on the correct branch (e.g., `main`).



### 5. **Pushing Code**

![1](./img/5.%20push.jpg)

- You pushed your code and workflow configuration to GitHub.
- This triggers the GitHub Actions workflow automatically.



### 6. **Initial Error**

![1](./img/6.%20error.jpg)

- The workflow ran but failed during the test step.
- The error message indicated that `jest` was not found, meaning the test runner was missing from your dependencies.

---

### 7. **Fixing the Error**

![1](./img/6a.%20fix.jpg)

- You fixed the error by adding Jest to your `devDependencies` in package.json and ensuring it was installed.
- You also made sure that `NODE_ENV` was not set to `production` during dependency installation, so devDependencies would be installed.



### 8. **Workflow Re-run**


![1](./img/7.%20fix.jpg)


- After fixing the dependencies, you pushed the changes and the workflow ran again.
- This time, the workflow progressed further, indicating the fix was successful.



### 9. **Final Fixes**

![1](./img/8.%20fixx.jpg)

- You addressed any remaining issues, such as version compatibility between Jest and Node.js.
- You ensured the workflow only used compatible versions or downgraded Jest as needed.

---

### 10. **Successful Workflow**

![1](./img/9.%20success.jpg)

- The workflow completed successfully!
- All steps (install, build, test) passed, confirming your CI/CD pipeline is working as intended.

---

## **Summary**

- **I automated your Node.js project’s build and test process using GitHub Actions.**
- **I troubleshooted and fixed errors related to missing dependencies and version compatibility.**
- **My workflow now ensures that every code push is automatically tested, improving code quality and reliability.**






