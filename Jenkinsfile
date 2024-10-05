pipeline {
    agent any


    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/noahdinho/aws_appcicd.git'
        IMAGE_TAG = 'noahdinho/aws_appcicd'
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }
    


    stages{
      stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
      }
      stage('docker build'){
        steps{
            sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
            sh 'docker images'
        }
      }
      stage('change'){
        steps{
            sh 'echo change'
        }
      } 
      stage('build stage'){
        steps{
           ('echo build stage')
        }
      }
    }
}