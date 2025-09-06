pipeline {
    agent any
    tools {
        maven 'my-maven'   // Jenkins tool config name
        jdk 'JDK-17'      // Jenkins tool config name
    }
    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/zia-kayani/test-CI-CD.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
