pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Move to the 'main' directory

                    sh 'g++ ./main/hello.cpp -o hello'

            }
        }
        stage('Test') {
            steps {
                // Move to the 'main' directory
  
                    sh './main/hello' 
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
