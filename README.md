# GitHub-Action-CI-CD-YAML

>Objectives  
1. Set up build sets in Github action  
2. Run test as part of the CI process  
3. Integrate code quality checks (ESLint)  
4. Use dependency caching for faster builds  

---

## **Detailed Explanation of the CI/CD & Code Quality Process (with Screenshots)**

### 1. **Repository Creation**

![Repository Creation](./img/1.%20git%20repo.jpg)

- I started by creating a new GitHub repository for my Node.js project.  
- This is the foundation for version control and collaboration.

---

### 2. **Workflow Setup**

![Workflow Setup](./img/2.%20step%201.jpg)

- I navigated to the **Actions** tab in my repository to set up a new GitHub Actions workflow.
- This workflow automates my CI/CD process.

---

### 3. **Script Configuration**

![Script Configuration](./img/3.%20script.jpg)

- I configured my workflow YAML file (`main.yml`) to define the steps for my CI pipeline.
- The workflow includes steps to check out code, set up Node.js, install dependencies, build, and run tests.

---

### 4. **Advanced Workflow Settings**

![Advanced Workflow Settings](./img/4.%20advanced.jpg)

- I customized the workflow to fit my project’s needs, such as specifying the Node.js version and the branch to run on.
- This ensures the workflow only runs in the correct environment and on the correct branch (e.g., `main`).

---

### 5. **Pushing Code**

![Pushing Code](./img/5.%20push.jpg)

- I pushed my code and workflow configuration to GitHub.
- This triggers the GitHub Actions workflow automatically.

---

### 6. **Initial Error**

![Initial Error](./img/6.%20error.jpg)

- The workflow ran but failed during the test step.
- The error message indicated that `jest` was not found, meaning the test runner was missing from my dependencies.

---

### 7. **Fixing the Error**

![Fixing the Error](./img/6a.%20fix.jpg)

- I fixed the error by adding Jest to my `devDependencies` in package.json and ensuring it was installed.
- I also made sure that `NODE_ENV` was not set to `production` during dependency installation, so devDependencies would be installed.

---

### 8. **Workflow Re-run**

![Workflow Re-run](./img/7.%20fix.jpg)

- After fixing the dependencies, I pushed the changes and the workflow ran again.
- This time, the workflow progressed further, indicating the fix was successful.

---

### 9. **Final Fixes**

![Final Fixes](./img/8.%20fixx.jpg)

- I addressed any remaining issues, such as version compatibility between Jest and Node.js.
- I ensured the workflow only used compatible versions or downgraded Jest as needed.

---

### 10. **Successful Workflow**

![Successful Workflow](./img/9.%20success.jpg)

- The workflow completed successfully!
- All steps (install, build, test) passed, confirming my CI/CD pipeline is working as intended.

---

## **Integrating Code Quality Checks and Caching**

### 11. **Installing Dependencies**

![NPM Install](./img/10.%20npm%20install.jpg)

- I installed all necessary dependencies, including ESLint for code quality checks.

---

### 12. **Running ESLint Initialization**

![ESLint Init](./img/11.%20npx.jpg)

- I initialized ESLint in my project using `npx eslint --init` and selected the appropriate options for my environment.

---

### 13. **ESLint Configuration**

![ESLint Config](./img/12.%20config.jpg)

- ESLint created a configuration file (`eslint.config.mjs`) tailored to my project setup.

---

### 14. **Adding Lint and Cache Steps to Workflow**

![YAML Script 1](./img/13.%20yaml%20script%201.jpg)
![YAML Script 2](./img/14.%20Yaml%20script%202.jpg)

- I updated my GitHub Actions workflow to include steps for running ESLint and caching dependencies for faster builds.

---

### 15. **Pushing Updated Workflow**

![Push Updated Workflow](./img/15.%20push.jpg)

- I pushed the updated workflow and configuration files to GitHub.

---

### 16. **Encountering and Fixing Lint Errors**

![Lint Error](./img/16.%20error.jpg)
![Lint Solution](./img/17.%20solution.jpg)

- The workflow caught some lint errors, which I fixed by updating my ESLint config and code.

---

### 17. **Final Success**

![Final Success](./img/18.%20success.jpg)

- After resolving all issues, my workflow now runs all steps (install, lint, build, test) successfully on every push.

---

## **Summary**

- **I automated my Node.js project’s build, lint, and test process using GitHub Actions.**
- **I troubleshooted and fixed errors related to missing dependencies, version compatibility, and code quality.**
- **I integrated ESLint for code quality checks and used caching for faster CI builds.**
- **My workflow now ensures that every code push is automatically checked and tested, improving code quality and reliability.**






