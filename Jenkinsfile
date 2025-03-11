pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS158-1 prg.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS158-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    echo 'completed'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
