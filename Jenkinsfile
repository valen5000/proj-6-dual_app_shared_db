pipeline {
    agent {label 'agent' }
    stages {
        stage('Deploy Apps') {
            steps {
                sh 'cd Deployment && ansible-playbook -i aws_ec2.yml playbook.yml'
            }
 
        }
        success {
            echo 'Pipeline finished successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}