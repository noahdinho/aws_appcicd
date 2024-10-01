pipeline {
    agent any

    environment{
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/noahdinho/aws_appcicd.git'
    }

    stages{
      stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
      }
      stage('docker build'){
        steps{
            sh 'docker build -t aws_appcicd .'
            sh 'docker images'
        }
      }
      stage('change'){
        steps{
            sh 'echo change'
        }
      } 
    }
}