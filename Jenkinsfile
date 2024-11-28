pipeline {
    agent any
    tools {
        maven "Maven"
    }
    parameters {
        string(name: 'VMVERSION', defaultValue: 'defaultValue', description: 'Version to deploy on prod')
        choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3'], description: 'Select version to deploy')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests?')
    }
    environment {
        NEW_VERSION = '1.3.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Building version ${NEW_VERSION}"
                bat "nvm install"
                // Here you can define commands for your build
            }
        }
        stage('Test') {
            when {
                expression { params.executeTests }
            }
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
}
