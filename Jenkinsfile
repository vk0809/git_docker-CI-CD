pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/vk0809/git_docker-CI-CD.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t git_docker-CI-CD .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop git_docker-CI-CD || true
                docker rm git_docker-CI-CD || true
                docker run -d -p 5000:5000 --name git_docker-CI-CD git_docker-CI-CD-app
                '''
            }
        }
    }
}

