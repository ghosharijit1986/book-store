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
        		user = 'ghosh_arijit86'
        		password = 'Hello@123'
        		}
            steps {
            	echo "${env.user}"
                bat 'mvn deploy -Dusername=$user -Dpassword=$password -DmuleDeploy'
                }
        }
    }
}