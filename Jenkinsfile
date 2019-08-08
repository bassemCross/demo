pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                gradle copyFiles
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
