pipeline {

    agent none
    parameters {
    booleanParam(name: 'SKIP_BUILD', defaultValue: false, description: 'Skip build and test stages')
    booleanParam(name: 'PROMOTE_TO_STABLE', defaultValue: false, description: 'Promote to stable')
    booleanParam(name: 'DEPLOY_TO_STABLE', defaultValue: false, description: 'Deploy to stable')
    string(name: 'TAG', defaultValue: '', description: 'Git and docker tag (for promote to stable)')
    booleanParam(name: 'PROMOTE_TO_PROD', defaultValue: false, description: 'Promote to prod')
    booleanParam(name: 'DEPLOY_TO_PROD', defaultValue: false, description: 'Deploy to prod')
    choice(name: 'PROD_COUNTRY', choices: ['us', 'cn'], description: 'Prod country')
  }
    stages {
     when { 
        beforeAgent true
        not { expression { return params.SKIP_BUILD } } 
        not { branch 'master' }
        not { tag '*' }
        not { expression { params.PROMOTE_TO_STABLE } }
      }
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
