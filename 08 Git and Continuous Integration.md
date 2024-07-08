# 8. Git and Continuous Integration

## Setting up CI/CD 🔧🚀

Continuous Integration (CI) and Continuous Deployment (CD) are practices that help automate the process of testing and deploying your code. Setting up CI/CD ensures that your code is always in a deployable state.

### How to Set Up CI/CD

1. **Choose a CI/CD Tool:**
   - Popular tools include GitHub Actions, Travis CI, CircleCI, and Jenkins.

2. **Create a Configuration File:**
   - For GitHub Actions, create a `.github/workflows/ci.yml` file.

3. **Define Your Workflow:**
   - Specify the steps to build, test, and deploy your code.

### Example Workflow for GitHub Actions

1. **Create Workflow File:**
   ```yaml
   # .github/workflows/ci.yml
   name: CI

   on: [push, pull_request]

   jobs:
     build:
       runs-on: ubuntu-latest

       steps:
       - uses: actions/checkout@v2
       - name: Set up Node.js
         uses: actions/setup-node@v2
         with:
           node-version: '14'
       - run: npm install
       - run: npm test
       - run: npm run build
   ```

2. **Commit and Push:**
   ```sh
   git add .github/workflows/ci.yml
   git commit -m "Set up CI with GitHub Actions"
   git push origin main
   ```

### Summary Table

| Step                                    | Description                                   |
|-----------------------------------------|-----------------------------------------------|
| Choose a CI/CD Tool                     | Select a tool like GitHub Actions or Travis CI|
| Create Configuration File               | Define your workflow in a `.yml` file         |
| Commit and Push                         | Commit your configuration to the repository   |

Setting up CI/CD automates your build and test processes, ensuring that your code is always ready to be deployed.

## Automating Tests 🧪🤖

Automating tests is a crucial part of CI/CD. It ensures that your code works correctly by running tests automatically whenever you push changes to your repository.

### How to Automate Tests

1. **Write Tests:**
   - Use a testing framework like Jest for JavaScript, PyTest for Python, or JUnit for Java.

2. **Add Tests to Your CI/CD Pipeline:**
   - Include test commands in your CI/CD configuration file.

### Example Workflow for Automating Tests with GitHub Actions

1. **Write a Test:**
   - Create a test file, e.g., `test.js`, and write your tests.
   ```javascript
   // test.js
   const sum = require('./sum');
   test('adds 1 + 2 to equal 3', () => {
     expect(sum(1, 2)).toBe(3);
   });
   ```

2. **Add Test Command to Workflow:**
   ```yaml
   # .github/workflows/ci.yml
   name: CI

   on: [push, pull_request]

   jobs:
     build:
       runs-on: ubuntu-latest

       steps:
       - uses: actions/checkout@v2
       - name: Set up Node.js
         uses: actions/setup-node@v2
         with:
           node-version: '14'
       - run: npm install
       - run: npm test
   ```

3. **Commit and Push:**
   ```sh
   git add .github/workflows/ci.yml test.js
   git commit -m "Add tests and automate with CI"
   git push origin main
   ```

### Summary Table

| Step                                    | Description                                    |
|-----------------------------------------|------------------------------------------------|
| Write Tests                             | Create test files using a testing framework    |
| Add Test Command to CI/CD Workflow      | Include test commands in your `.yml` file      |
| Commit and Push                         | Commit your test and CI/CD configuration       |

Automating tests ensures that your code is always tested for errors and functionality before being merged or deployed, increasing the reliability of your software.

---
