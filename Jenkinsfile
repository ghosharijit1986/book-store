pipeline {
    agent any
    environment {
        		SECRET_FILE_ID = credentials('mule-sec')
        		muleuser = credentials('user')
        		mulepwd = credentials('password')
        	}
    stages {
    	
        stage('Build') {
           steps {
                bat 'mvn clean install'
                }
        }
        stage('Deploy') {
        	
        	
            steps {
            	echo "${SECRET_FILE_ID}"
            	echo "${muleuser}"
                bat "mvn deploy -Dusername=${muleuser} -Dpassword=${mulepwd} -DmuleDeploy"
                }
        }
    }
}