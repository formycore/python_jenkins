pipeline {
    agent any
    environment {
        PYTHON_VERSION = '3.6.10'
        PIP_VERSION = '21.3.1'
    }
    stages {
        stage('Git clone'){
            steps {
                git 'https://github.com/formycore/python_jenkins.git'
            }
        }
        stage('Checking the pip version'){
            steps {
                sh ' python3 -m pip --version'
            }
        }
    }
}