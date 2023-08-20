pipeline {
    agent {label 'JDK'}
    parameters {
        choice(name: 'Branch', choices: ['master','main'], description: 'pick')
    }
    stages {
        stage('GIT') {
            steps {
               git url: 'https://github.com/spring-projects/spring-petclinic.git',
                   branch: "${prams.branch}"
            }
            }
        stage('build') {
            steps {
              sh 'mvn package'
            }
             
        }
    }
}