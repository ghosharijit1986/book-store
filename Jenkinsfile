pipeline {
    agent any
    stages {
        stage('Build') {
           steps {
                bat 'mvn clean install'
                }
        }
        stage('Deploy') {
        	environment {
        		user = 'muleuser'
        		password = 'mulepwd'
        		}
            steps {
            	bat 'echo "User $user"'
                bat 'mvn deploy -Dusername=$user -Dpassword=$password -DmuleDeploy'
                }
        }
    }
}