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
	    env.WINDOWS_VM_PASSWD = params.WINDOWS_VM_PASSWD
        }
      }
    }

    stage ('Run PLaybook') {
        steps {
	    sh ('ansible-playbook -i WINDOWS_VM_IP, ./playbooks/connect-windows-server.yml -e ansible-user=WINDOWS_VM_USER -e ansible-password=WINDOWS_VM_PASSWD -vvv')
        }
    }
  }
 
  post {
    success {
      echo "success"
    }
    failure {
      echo "failure"
    }
  }
}
