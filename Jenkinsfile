pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
              git branch: 'main', url: 'https://github.com/akhila1402/DevopsLab.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-node-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 my-node-app'
            }
        }
    }
}
