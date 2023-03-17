pipeline {
    agent any
    stages {
        stage('Build') {
           steps {
                bat 'mvn clean install'
                }
        }
        stage('Deploy') {
            steps {
                bat 'mvn deploy -Dusername=ghosh_arijit86 -Dpassword=Hello@123 -DmuleDeploy'
                }
        }
    }
}