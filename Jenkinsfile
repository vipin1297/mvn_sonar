pipeline{
    agent any
    stages{
        stage('git checkout scm'){
            steps{
            git 'https://github.com/vipin1297/mvn_sonar.git'
            }
        }
        stage('Analysis'){
            steps{
            sh '/opt/maven/bin/mvn clean verify sonar:sonar –Dsonar.password=admin – Dsonar.login=admin'
            }
        }
        stage('Build'){
            steps{
                sh '/opt/maven/bin/mvn clean install'
                 }
        }
    }

