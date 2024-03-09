pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o output PES1UG21CS295-1.cpp'
                }
            }
            post {
                failure {
                    echo 'Pipeline failed'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using shell script
                    sh './output'
                }
            }
            post {
                failure {
                    echo 'Pipeline failed'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Your deployment steps here
            }
            post {
                failure {
                    echo 'Pipeline failed'
                }
            }
        }
    }
}
