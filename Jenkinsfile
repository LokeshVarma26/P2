pipeline {
    agent {label 'JDK'}
    Stages {
        stage('GIT') {
            git url: 'https://github.com/spring-projects/spring-petclinic.git'
            branch: 'main'
            }
        stage('build') {
            sh 'mvn package'
             
        }
    }
}