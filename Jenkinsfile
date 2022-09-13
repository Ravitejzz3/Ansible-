pipeline {
    agent any
    parameters {
          string(name: 'COMPONENT', defaultValue: '', description: 'Enter the name of the component')
          choice(name: 'ENV', choices: ['dev', 'prod'], description: 'Chose the environment')
    }
    environment { 
        SSH_CRED = credentials('SSH-Cenos7')
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
    
