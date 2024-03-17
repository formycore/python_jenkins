pipeline {
    agent any
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