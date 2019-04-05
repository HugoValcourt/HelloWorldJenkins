pipeline {

    agent none
    stages {

        stage('TEST MASTER'){
            agent { label 'master'}
            steps {
		    sh "ls -al"
	            sh "javac HelloWorld.java"
	            sh "java HelloWorld"
            }
        }
    }
}
