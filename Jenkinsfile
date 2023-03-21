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
            	echo "${muleuser}"
                bat 'mvn deploy -Dusername=${muleuser} -Dpassword=${mulepwd} -DmuleDeploy'
                }
        }
    }
}