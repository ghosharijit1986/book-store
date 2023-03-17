pipeline {
    agent any
    stages {
        stage('build') {
           steps {
                bat 'mvn clean install'
                }
        }
        stage('deploy') {
            steps {
                bat 'mvn deploy -Dusername=ghosh_arijit86 -Dpassword=Hello@123 -DmuleDeploy'
                }
        }
    }
}