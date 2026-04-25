DevOps Problem Statement:
CI/CD Pipeline with Dev → Test → Prod using GitHub Actions
 Scenario
You are a DevOps Engineer responsible for automating the deployment of a simple static 

website (HTML page) using:
GitHub Actions
GitHub Pages
The organization follows a 3-stage deployment model:
 Dev → Test → Prod

 Objective:
Build a CI/CD pipeline that automatically:
 Builds and deploys a simple HTML page
run shell commands in each stage(dev -> test -> prod)
 Uses GitHub-native tools only
 

>> solution:
1. index. html -> sample code
2. 3 branches -> dev, test , prod
3. yaml file:
	static html -
  3 jobs: <> 3 stages
  	1. dev -> bash "hello dev"
    2. test -> bash "hello test"
    3. prod -> bash "hello prod" -> branch link -> github Actions -> Pages {deployment}
4. URL -> production branch -> production job -> GitHub Pages (deployment platform)


'''

sample script:

jobs:
  bash-example:
    runs-on: ubuntu-latest
    steps:
      - name: Run a single-line script
        run: echo "Hello from GitHub Actions!"

      - name: Run a multi-line script
        run: |
          echo "Current directory: $(pwd)"
          USER_NAME="GitHub Runner"
          echo "Hello, $USER_NAME"
        shell: bash

'''

===
