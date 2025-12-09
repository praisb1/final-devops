pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'git@github.com:praisb1/final-devops.git'
            }
        }

        stage('Build and Deploy to Nexus') {
            steps {
                sh 'chmod +x mvnw'
                sh './mvnw -s settings.xml clean deploy -DskipTests'
            }
        }
    }
}
