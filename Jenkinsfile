pipeline {
    agent {label 'JDK'}
    parameters {
        choice(name: 'Branch', choices: ['master','main'], description: 'pick')
    }
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