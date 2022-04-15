# ansible-config-mgt

Ansible project 10

To test the setup by making some change in README.MD file in master branch

More learning

More

Refactoring

Refactoring again for confirmation

Working on Jenkins pipeline

### Demo for Jenkinsfile Quick Start
======================================

...
pipeline {
    agent any

  stages {
    stage("Initial cleanup") {
      steps {
        dir("${WORKSPACE}") {
          deleteDir()
        }
      }
    }

    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }
    
    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }

    stage('Package') {
      steps {
        script {
          sh 'echo "Packaging App"'
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          sh 'echo "Dev"'
        }
      }
    }

    stage('CleanUp') {
      steps {
        dir("${WORKSPACE}") {
          cleanWs()
        }
      }
    }
  }
}
.....

