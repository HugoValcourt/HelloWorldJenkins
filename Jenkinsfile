pipeline {

    agent none
    stages {

        stage('RUN MASTER'){
            agent { label 'master'}
            steps {
		    sh "echo TEST"
	            sh "javac HelloWorld.java"
	            sh "java HelloWorld"
            }
        }
    }
}
