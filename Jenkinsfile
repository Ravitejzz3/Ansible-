pipeline {
    agent any

    stages {
        stage('Do a dry-run') {
            steps {
                sh "env" 
                sh "ansible-playbook robo-dryrun.yml -e ansible_user=centos -e ansible_password=DevOps321 -e COMPONENT=mongobd -e ENV=dev"
            }
        }
    }
}