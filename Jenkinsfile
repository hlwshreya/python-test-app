pipeline {
    agent any
    triggers {
        pollSCM('H/2 * * * *')  // Poll THIS app repo
    }
    stages {
        stage('Trigger Ansible Deploy') {
            steps {
                build job: 'Python-App-Deploy/main', 
                      wait: false,
                      propagate: false
            }
        }
    }
}
