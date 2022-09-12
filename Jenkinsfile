pipeline {
    agent any

    stages {
        stage('Do a dry-run') {
            sh "ansible-playbook robo-dryrun.yml -e ansible_user=centos -e ansible_password=DevOps321 -e COMPONENT=mongodb -e ENV=dev"

        }
    }
}