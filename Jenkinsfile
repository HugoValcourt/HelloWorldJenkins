pipeline {

    agent none
    stages {

        stage('TEST MASTER'){
            agent { label 'master'}
            steps {
	            javac HelloWorld.java
	            java HelloWorld
            }
        }
    }
}
