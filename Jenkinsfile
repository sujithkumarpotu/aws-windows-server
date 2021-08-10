pipeline {
agent any

stages {
    stage ('Git clone') {
        steps {
            git changelog: false, poll: false, url: '/var/lib/jenkins/ansible-workspace'
        }
    }
    stage ('Run PLaybook') {
        steps {
            
            sh """ansible-playbook --extra-vars '{"name":"${params.first_name}"}' deploy.yml"""
        }
    }
  }
}
