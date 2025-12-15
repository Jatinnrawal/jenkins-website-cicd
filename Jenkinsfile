pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build: validating source'
            }
        }

        stage('Test') {
            steps {
                bat 'if not exist index.html exit 1'
                echo 'Test: index.html exists'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                if not exist C:\\website-deploy mkdir C:\\website-deploy
                copy index.html C:\\website-deploy /Y
                '''
                echo 'Deploy: website deployed'
            }
        }
    }
}
