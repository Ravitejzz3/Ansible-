pipeline {
    agent any

    stages {
        stage('Do a dry-run') {
            steps {
                sh "env" 
                sh "ansible-playbook robo-dryrun.yml -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW} -e COMPONENT=${params.COMPONENT} -e ENV=${params.ENV}"
            }
        }
    }
}