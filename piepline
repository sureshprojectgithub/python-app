pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '39ae3a88-5dbc-4f95-be61-97152b403021', url: 'https://github.com/sureshprojectgithub/python-app.git']])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', credentialsId: '39ae3a88-5dbc-4f95-be61-97152b403021', url: 'https://github.com/sureshprojectgithub/python-app.git'
                sh 'python suresh.py'
            }
        }
        stage ('Test') {
            steps {
                echo 'the job has been tested'
            }
        }
    }
}
