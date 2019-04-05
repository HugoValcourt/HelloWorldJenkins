pipeline {

    agent none
    stages {

        stage('TEST MASTER'){
            agent { label 'master'}
            steps {
		    sh "ls -al"
	            javac HelloWorld.java
	            java HelloWorld
            }
        }
    }
}
