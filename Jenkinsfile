pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Portfolio Website'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Portfolio Website'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker build -t my-portfolio .'
                bat 'docker run -d -p 8081:80 --name portfolio-container my-portfolio'
            }
        }
    }
}