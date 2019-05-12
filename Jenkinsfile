pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                git url: 'https://github.com/kishorgithub1/maven-project.git'
            }
        }
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('My SonarQube Server') {
                    
                    withMaven(maven:'maven') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
        }
    }
}
