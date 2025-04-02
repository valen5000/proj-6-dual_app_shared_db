pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/valen5000/proj-6-dual_app_shared_db.git'
            }
        }
        stage('Deploy Apps') {
            steps {
                sh 'ansible-playbook -i inventory ansible/deploy.yml'
            }
        }
    }
}