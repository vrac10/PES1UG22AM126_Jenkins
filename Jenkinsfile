pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Buiding the script'
                    sh 'g++ -o PES1UG22AM126-1 main.cpp' // Compile .cpp file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    echo 'Testing the script'
                    sh './PES1UG22AM126-2' // Run the compiled executable
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment Stage'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
