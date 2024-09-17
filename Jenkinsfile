pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/CrimsonFellow/healthcare-angular-frontend'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'npm run build --prod'
            }
        }
        stage('Archive Artifacts') {
            steps {
                archiveArtifacts 'dist/**'
            }
        }
    }
}
