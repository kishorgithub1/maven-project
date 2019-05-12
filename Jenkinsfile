pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/kishorgithub1/maven-project.git'
        }
  }
    
        stage('create package before sonarqube'){
        steps{
              withSonarQubeEnv('sonar'){
                  withMaven(maven : 'maven'){
              sh 'clean package sonar: sonar'
              }
             }
            }
           }
          }
