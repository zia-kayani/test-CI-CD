pipeline {
    agent any

    tools {
        maven 'my-maven'   // name you configured in Jenkins tools
        jdk 'jdk-21'       // name you configured in Jenkins tools
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/zia-kayani/test-CI-CD.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
