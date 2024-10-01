pipeline {
    agent any

    stages{
      stage('git checkout'){
        steps{
            git branch: 'main', url: 'https://github.com/noahdinho/aws_appcicd.git'
        }
      }
      stage('test'){
        steps{
            sh 'echo test'
        }
      }
      stage('change'){
        steps{
            sh 'echo change'
        }
      } 
    }
}