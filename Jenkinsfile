pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/kishorgithub1/maven-project.git'
        }
  }
    {
        stage('create package before sonarqube'){
        steps{
              withSonarQubeEnv(My sonar){
    
              sh 'sonar'
              }
             }
            }
           }
          }
