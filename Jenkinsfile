pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS709-1'
                sh 'g++ main/hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') 
            steps {
                ech 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
