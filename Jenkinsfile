pipeline {
agent any

stages {
    stage('start') {
      steps {
          echo 'Starting Pipeline'
        }
    }

    stage('Job Parameters') {
      steps {
        script {
	    env.AWS_ACCESS_KEY_ID = params.AWS_ACCESS_KEY_ID
            env.AWS_SECRET_ACCESS_KEY = params.AWS_SECRET_ACCESS_KEY
	    env.AWS_REGION = params.AWS_REGION
        }
      }
    }
    stage ('Run PLaybook') {
        steps {
	    sh ('echo "hello World!"')
            
        }
    }
  }
}
