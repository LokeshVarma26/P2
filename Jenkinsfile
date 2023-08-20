pipeline {
    agent {label 'JDK'}
    parameters {
        choice(name: 'Branch', choices: ['master','main'], description: 'pick')
    }
    Stages {
        stage('GIT') {
            steps{
            git url: 'https://github.com/spring-projects/spring-petclinic.git'
            branch: 'main'
            }
            }
        stage('build') {
            steps{
            sh 'mvn package'
            }
             
        }
    }
}