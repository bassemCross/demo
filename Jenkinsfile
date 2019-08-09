pipeline {
    agent any
    options {
        skipDefaultCheckout true
    }
    stages {
        stage('Checkout SCM') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: scm.branches,
                    doGenerateSubmoduleConfigurations: scm.doGenerateSubmoduleConfigurations,
                    extensions: scm.extensions + [[$class: 'GitLFSPull']],
                    userRemoteConfigs: scm.userRemoteConfigs
                ])
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew copyFiles'
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
