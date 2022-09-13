pipeline {
    agent any
    parameters {
        choice(name: 'ENV', choices: ['dev', 'prod'], description: 'Chose the environment')
        string(name: 'COMPONENT', defaultValue: 'mongodb', description: 'Enter the name of the component')
          
    }
    environment { 
        SSH_CRED = credentials('SSH-Centos7')
    }
    stages {
        stage('Do a dry-run') {
            steps {
                sh "env" 
                sh "ansible-playbook robo-dryrun.yml -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW} -e COMPONENT=${params.COMPONENT} -e ENV=${params.ENV}"
            }
        }
    }
}
    
