pipeline {
    agent {
        label 'test'
    }
       stages {
        stage('Git clone'){
            steps {
                git 'https://github.com/formycore/python_jenkins.git'
            }
        }
        stage('Checking the pip version'){
            steps {
                sh 'whoami'
                sh ' python3 -m pip --version'
            }
        }
        stage ('Install Make'){
            steps {
                sh 'sudo yum install make -y'
                sh 'sudo yum groupinstall "Development Tools" -y'
                
            }
        }
        stage('Docker Build'){
            steps {
                sh 'make image'
            }
        }
        stage('Docker push'){
            steps {
                withDockerRegistry(credentialsId: 'docker_token') {
                sh 'make push'
                sh 'docker run -d -p 5000:5000 --name python_jenkins formycore/python-demoapp'
            }
            }
        }
    }
}