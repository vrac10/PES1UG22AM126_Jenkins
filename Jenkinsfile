pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22AM126-1 main.cpp' // Compile .cpp file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22AM126-1' // Run the compiled executable
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    sh 'git add main.cpp'
                    sh 'git commit -m "Adding working C++ file"'
                    sh 'git push origin main' // Push to repository
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
