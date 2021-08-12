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
	    env.WINDOWS_VM_IP = params.WINDOWS_VM_IP
            env.WINDOWS_VM_USER = params.WINDOWS_VM_USER
	    env.WINDOWS_VM_PASSWD = params.AWS_REGION
        }
      }
    }

    stage ('Run PLaybook') {
        steps {
	    sh ('')
        }
    }
  }
}
