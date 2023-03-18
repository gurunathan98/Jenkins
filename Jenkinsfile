pipeline{
    agent any
    stages{
        stage('Checkout'){
           steps{
            checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/gurunathan98/Jenkins']])
           } 
        }
        stage('Build'){
            steps{
                git branch: 'main', url: 'https://github.com/gurunathan98/Jenkins'
                bat 'python app.py'
            }
        }
    }
}