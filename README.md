# CI/CD Pipeline using Jenkins

## 1. About the Project
This project implements a basic Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins.  
The pipeline automatically pulls code from GitHub, runs a build stage, executes test scripts, and performs a simulated deployment.  
It demonstrates the essential workflow used in real DevOps environments.

---

## 2. Tech Stack Used
- Jenkins (Declarative Pipeline)
- Git & GitHub
- Python (for sample application and tests)
- Linux (Ubuntu VM)
- Shell scripting (used within Jenkins stages)

---

## 3. Project Overview
The CI/CD pipeline has three key stages:

### Build
Validates the environment and ensures the application is ready for testing.

### Test
Runs a Python test script (`test.py`) to simulate automated testing.

### Deploy
Simulates deployment through a scripted step.

The pipeline is defined through a `Jenkinsfile`, following Pipeline-as-Code principles.  
The Jenkins job is connected to GitHub using the SCM configuration.

---

## 4. Project Structure
jenkins-ci-cd-demo/<br>
│<br>
├── app.py # Simple Python application<br>
├── test.py # Test script executed during CI<br>
└── Jenkinsfile # Jenkins CI/CD pipeline definition<br>

### Jenkinsfile (Reference)
```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'python3 test.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
```
## 5. Sample Output (Console Log)
```groovy
Building the application...
Running tests...
Tests passed successfully!
Deploying application...
Finished: SUCCESS
```

## 6. Learning Outcomes
<ul>
<li>Understood the basic structure of CI/CD pipelines</li>
<li>Learned how to configure Jenkins on a Linux environment</li>
<li>Gained hands-on experience with Jenkins declarative pipelines</li>
<li>Integrated GitHub with Jenkins using SCM</li>
<li>Executed automated build, test, and deployment stages</li>
<li>Learned how Python scripts and Jenkins pipelines interact in automation workflows</li>
</ul>
